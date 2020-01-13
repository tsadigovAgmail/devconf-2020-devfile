## Architecture

```
      + - - - - - +
      |  BROWSER  |
      + - - - - - +
            |
            |
            | - - - - - - - - - - >|
            |                      |
            |                      |                                public
  -------------------------------------------------------------------------
           /\                      /\                                  k8s
           ||                      ||
           ||                      ||
           ||                      ||
           ||                      ||
         (4100)            (web-backend:8080)
    +--------------+       +-----------------+             +-----------+
    |              |       |                 |             |           |
    |   FRONTEND   |       |     BACKEND     |-------(3600)|     DB    |
    |  (js-react)  |       |  (java-spring)  |             |  (mysql)  |
    |              |       |                 |             |           |
    +--------------+       +-----------------+             +-----------+
```

### db
```
# build.gradle
runtime('mysql:mysql-connector-java')
```

```
# application.properties
database=mysql
spring.datasource.url=jdbc:mysql://db:3306/demo
spring.datasource.username=demo
spring.datasource.password=demo
```

## resources
 - https://www.eclipse.org/che/docs/che-7/making-a-workspace-portable-using-a-devfile/
 - https://github.com/redhat-developer/devfile
   - https://redhat-developer.github.io/devfile/
   - https://redhat-developer.github.io/devfile/devfile
