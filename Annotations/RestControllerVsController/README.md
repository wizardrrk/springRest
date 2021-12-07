# springRest
## Question
Difference between @RestController and @Controller Annotation in Spring MVC and REST
## Answer
###1
The @Controller is a common annotation which is used to mark a class as Spring MVC Controller while the @RestController is a special controller used in RESTFul web services and the equivalent of @Controller + @ResponseBody.
###2
The @Controller is a specialization of @Component annotation while @RestController is a specialization of @Controller annotation. It is actually a convenience controller annotated with @Controller and @ResponseBody as shown below.

@Target(value=TYPE)
@Retention(value=RUNTIME)
@Documented
@Controller
@ResponseBody
public @interface RestController


and here is how the declaration of @Controller looks like:
@Target(value=TYPE)
@Retention(value=RUNTIME)
@Documented
@Component
public @interface Controller
