# Spring Testing Practices

Spring Boot provides a `@SpringBootTest` annotation, which can be used as an alternative to the standard spring-test `@ContextConfiguration` annotation when you need Spring Boot features. The annotation works by creating the `ApplicationContext` used in your tests through SpringApplication. In addition to `@SpringBootTest` a number of other annotations are also provided for testing more specific slices of an application.

## Isolate the Functionality to be Tested

 Isolate the functionality you want to test by limiting the context of loaded frameworks/components. Often, it is sufficient to use the JUnit unit testing framework. without loading any additional frameworks. To accomplish this, you only need to annotate your test with `@Test`.

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

Use `@WebMvcTest` to test REST APIs exposed through Controllers without the server part running. Only list Controllers that are being tested.

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

Refer to [Spring Boot Testing Documentation](https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.testing.spring-boot-applications) documentation for detailed explaination and Best Practices for Spring Testing.