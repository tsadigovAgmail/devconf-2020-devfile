how to devfile: https://docs.google.com/document/d/1CEgtZVd5Y1P4IKutpxiHkrgUS3258xZY0Yp0PZs950M/edit#

projects in devfile: https://github.com/eclipse/che-docs/blob/master/src/main/pages/che-7/end-user-guide/proc_writing-a-devfile-for-your-project.adoc#specifying-multiple-projects-in-a-devfile


## Architecture

```
      + - - - - - +
      |  BROWSER  |
      + - - - - - +
            |
            |
            | - - - - - - - - - - >|
            |                      |
            |                      |
  ------------------------------------------------------ ==vv== k8s ==vv==
           /\                      /\
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

## db
`runtime('mysql:mysql-connector-java')`

```
database=mysql
spring.datasource.url=jdbc:mysql://db:3306/demo
spring.datasource.username=demo
spring.datasource.password=demo
```

## `metadata`
### `name`
### `generateName`

## `projects`

## `attributes`

## `components`

## `commands`
