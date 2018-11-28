# JAQ Blog
A producttion ready blog portal built with HTML, Angular and Java.

![jaqblog-home](https://user-images.githubusercontent.com/902972/49127173-f0417e00-f28b-11e8-92b0-c3e4b22a37d9.png)

## Demo
* **[View live demo here](https://jaqtomcat8.azurewebsites.net/jaqblog/initializr)**
* Demo runs on Apache Tomcat 8.5.24 [Azure WebApp](https://azure.microsoft.com/en-us/services/app-service/web/)
* Register to add new blogs

# Build and Deployment
System requirements
* [Java 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Angular CLI - Optional](https://cli.angular.io/)
* [NodeJS ](https://nodejs.org/en/download/)
* [Apache Maven 3.x](https://maven.apache.org/download.cgi)

PreRequisites
* An account with [CosmicJS](https://cosmicjs.com/)
* All the content will be stored and managed in Cosmic JS CMS


## Test environment settings
* Java 1.8.0_162
* Angular CLI 1.6.8
* NodeJS 10.5.0
* NPM 6.1.0
* Yarn 1.7.0
* Apache Maven 3.3.9
* Apache Tomcat 8.5.27

# ComicJS Setup
JAQ blog uses CosmisJS as the backend to hold the content (Users and Blog). The following are required
* Create a free account with [CosmicJS](https://cosmicjs.com/)
* `Add New Bucket` and name it (say) 'myblog'
* Select `Apps` from the left nav, and install `Angular Blog`
* Select `Basic Settings` and note the below 3 properites.
  * Bucket id
  * API Read Access Key
  * API Write Access Key  
![jaqblog-cosmisjs-settings](https://user-images.githubusercontent.com/902972/49109993-d5eaae80-f251-11e8-9c7c-6b3584836a19.png) 
* Enter the above 3 values in the file `/ui.resources/src/config/cosmo.config.ts` 

# How to Build
JAQ Blog is built as primary Java application with Angular embedded within it. Maven is used to build the project.
* Fork and Clone the project to your local machine
* Open the file 
* From the folder, use the command `mvn clean package` to build JAQBlog's WAR file.

# How to Deploy/Run

Using Tomcat as an example:
* Open tomcat's admin console like `http://sampleserver.com:8080/manager/html` 
* Choose `Select WAR file to upload` , uplaod the `jaqblog.war`
* If the deployment is successful, you can see `/jaqblog` in the deployed applications.
* Open a new browser and use this url `http://samplesever.com:8080/jaqblog` . You should see `Java Hello World!`
* To run the blog, use the url `http://samplesever.com:8080/jaqblog/initializr` . You should see the blog home page loaded

# Features of the application
* View blog posts
* Register to the blog
* Login
* Add a new blog

# Architecture

### JAQ Blog Application Stack
![jaqblog-stack](https://user-images.githubusercontent.com/902972/49113401-16025f00-f25b-11e8-8d49-394d8580e37f.png)

### JAQ Blog with CosmicJS Process Flow
![jaqblogcosmis-processflow](https://user-images.githubusercontent.com/902972/49113399-16025f00-f25b-11e8-9764-30ea92aec82a.png)

### JAQ Stack Flow (JAQ Blog is built using JAQ Stack)
![jaqstack-process-flow](https://user-images.githubusercontent.com/902972/49113397-1569c880-f25b-11e8-9674-24f92b2f25fa.png)

# Extend
JAQ blog has been built as Java first web application with all of front-end managed using Angular.

This can be extendable to use Java to make REST calls to any CMS (or any service) and have Angular consume the return data and act accordingly.  

* Java
  * Sample Java servlets are defined at `/Users/konathal/Personal/SurenProjects/suren-blog/git/jaqblog/src/main/java/com/jaqstack/servlet`
* MongoDB
  * Sample Java class to connect to MongoDB `/Users/konathal/Personal/SurenProjects/suren-blog/git/jaqblog/src/main/java/com/jaqstack/data/MongoExample.java`  

For more examples on the above, you may see JAQ Stack's [examples on Github](https://github.com/ksurendra/jaqstack/tree/master/examples)

## Credits
* The core of the blog was forked from [Angular Blog](https://github.com/cosmicjs/angular-blog)
* Designed, developed and architected by [Suren Konathala](https://surenkonathala.com/) Contact/Tweet @surenkonathala
