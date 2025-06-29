Course Learning Journey
Course Information

Course Title: Spring Framework 6 and Spring Boot 3 with Spring AI
Instructor: Telusko
Status: In Progress

Learning Progress
Date: 06/28 -

Object Creation
Summary: ApplicationContext is the central interface to Spring's IoC container that automatically loads XML configuration files and creates all defined beans upon initialization. 
The workflow uses ClassPathXmlApplicationContext to create the container, then retrieves beans using getBean() method with their XML-defined IDs. 
Multiple beans of the same class can be defined with different IDs for independent object management. Retrieved bean references work like regular Java objects for method invocation.

Scopes
Summary: Spring beans have different scopes that control instance creation and sharing, with Singleton being the default scope where only one instance exists and is shared across all references. 
Prototype scope creates a new instance each time getBean() is called, while Request and Session scopes are web-specific creating instances per HTTP request or session respectively. 
Bean scope can be explicitly defined in XML using the scope attribute in the bean tag. Prototype scope is particularly useful for multi-threaded environments or when fresh instances are needed for each operation.

Setter Injection
Summary: Setter Injection is Spring's method for injecting dependencies or values into beans through setter methods using the property tag within bean configuration. 
The property tag uses name attribute to specify the class variable and value attribute to assign primitive values like int, boolean, or String. 
When ApplicationContext loads the XML configuration, it creates the bean object and automatically calls the corresponding setter methods with the specified values. 
This approach is commonly used for optional or configurable properties that can be set after object creation.

Ref Attribute
Summary: The ref attribute in Spring's property tag is used to inject reference-type values (objects of other beans) rather than primitive values, allowing one bean to reference another bean within the container. 
The ref attribute value must match the id of an existing bean defined in the configuration file, otherwise Spring throws an error during initialization. 
This enables dependency injection where one class can have objects of other classes as dependencies through setter methods. 
When multiple beans of the same class exist, Spring uses the specific id referenced in the ref attribute to determine which bean instance to inject.
