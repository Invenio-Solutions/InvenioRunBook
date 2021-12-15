# Logging in Mule

Logging is an important part of an application. It ensures and eases troubleshooting and provides visibilty and tracebility on the functioning of the components. It helps in analyzing and debugging an application.

Mule provisions logging through **Runtime Logs** and **Application Logs**. It supports Apache log4j2.xml level
There are certain standards that is required to follow as a best practices in logging.

- Standardizing the logging format. for example: JSON
- Logging must be clear, concise and relevant without adding much overhead.
- The logging message must be informative and must provide visibility in tracing and debugging.
- It is important that the logs are persisted and maintained
- It is preffered to provide log category to the logging component in order to determine if that particular log is important for production level or not.


### Documentation
1. [Configure Logging](https://docs.mulesoft.com/mule-runtime/4.3/logging-in-mule)
2. [Logging Best Practices](https://www.whishworks.com/blog/mulesoft/logging-best-practice-in-mule-esb-using-logger-component/)
3. [Guidelines on Logging in AnyPoint Platform](https://medium.com/the-mule-blog/guidelines-on-mulesoft-logging-alerting-visualizer-monitoring-b2a1bcf25b39)
4. [Video Tutorial on Logging Best Practices](https://www.youtube.com/watch?v=tj0K3ZhKCeg)