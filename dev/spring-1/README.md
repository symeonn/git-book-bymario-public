# SPRING

## Basics

spring framework provides structure and patterns to make developing process easier

#### Context

Inverse of Control - framework manages all the dependencies and puts your application in this \(instead i have to include libraries into my app\) \(Hollywood principle\)  
it utilizes Dependency Inversion from SOLID which leads to loosly coupled, flexibility and plugability

Dependency Injection - Spring creates objects and put them in context, then Spring inject these objects as dependencies when needed - decouples my class's construction from the construction of their dependencies

#### DB access

repository, query methods

#### Spring MVC

dynamic web page, REST API

### Bean scopes

* singleton
* prototype
* request\*
* session\*

#### Bean annotations

**@Component** - during ComponentScan Spring automatically detects beans with this annotation  
**@Repository** - data access layer class \(translates persistence framework exeptions to DataAccessExeptions\)  
**@Service** - business logic class  
**@Controller** - MVC  
**@Configuration** - contains bean definition methods 

####  S**coped bean injection problem**

When have prototype bean \(B\) in singleton bean \(A\), the B is initialized only once when A is initialized.  
Solutions:

* Injecting _ApplicationContext -_ so we can initialize each time we do getBean
* use @Lookup - 

