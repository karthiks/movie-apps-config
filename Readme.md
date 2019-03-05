# movie-apps-config

This directory holds config files for all apps in the project [java-microservices-bootcamp](https://github.com/karthiks/java-microservices-bootcamp). These files are referenced by the config server.



## Lessons Learnt

* You get an error like `Cannot clone or checkout repository: https://github.com/karthiks/movie-apps-config/tree/org-by-dir` if you try to configure checking out a particular branch as default. In such cases your `application.properties` of your spring-config-server should be like below:

  ```properties
  server.port=8888
  spring.cloud.config.server.git.uri=https://github.com/karthiks/movie-apps-config
  spring.cloud.config.server.git.default-label=org-by-dir
  ```

  