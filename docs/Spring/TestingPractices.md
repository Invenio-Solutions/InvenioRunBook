---
sidebar_position: 3
---
# Spring Testing Practices

Spring Boot provides a `@SpringBootTest` which works by creating the `ApplicationContext` used in the tests through SpringApplication. In addition to `@SpringBootTest` a number of other annotations are also provided for testing more specific slices of an application.

## Isolating the Functionality to be Tested

 Isolate the functionality by limiting the context of loaded frameworks/components is important. JUnit testing framework can be leveraged here. It is important to annotate the class with @Test to accomplish this.

## @SpringBootTest Annotation

When testing spring boot applications, the `@SpringBootTest` annotation loads the whole application, but it is often better to limit the application context to just the set of Spring components that participate in the test scenario. This is accomplished by listing them in the annotation declaration.

```
@RunWith(SpringRunner.class)
@SpringBootTest(classes = {MapRepository.class, CarService.class})
public class CarServiceWithRepoTest {

	@Autowired
	private CarService carService;

	@Test
	public void shouldReturnValidDateInTheFuture() {
    	Date date = carService.schedulePickup(new Date(), new Route());
    	assertTrue(date.getTime() > new Date().getTime());
	}
}
```

## @DataJpaTest Annotation

Using `@DataJpaTest` only loads `@Repository` spring components, and will greatly improve performance by not loading `@Service`, `@Controller`, etc.

```
@RunWith(SpringRunner.class)
@DataJpaTest
public class MapTests {

	@Autowired
	private MapRepository repository;

	@Test
	public void findByUsernameShouldReturnUser() {
    	final String expected = "NJ";
    	String actual = repository.findByZip("07677")

    	assertThat(expected).isEqualTo(actual);
	}
}
```

## Test the Web Layer

Using `@WebMvcTest` will enable to test only the  REST APIs exposed through Controllers without the server part running.

```
@RunWith(SpringRunner.class)
@WebMvcTest(CarServiceController.class)
public class CarServiceControllerTests {

	@Autowired
	private MockMvc mvc;

	@MockBean
	private CarService carService;

	@Test
	public void getCarShouldReturnCarDetails() {
    	given(this.carService.schedulePickup(new Date(), new Route());)
        	.willReturn(new Date());

    	this.mvc.perform(get("/schedulePickup")
        	.accept(MediaType.JSON)
        	.andExpect(status().isOk());
	}
}
```

### Reference:

 [Spring Boot Testing Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.testing.spring-boot-applications) has provided a detailed explaination and Best Practices for Spring Testing.