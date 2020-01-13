# config server

## OVERRIDES

there is a .yml file in configuration files \(hosted from Git\):

![](../../../.gitbook/assets/image-8.png)

and during config-server deployment it can be also set as \(using overrides\):

![](../../../.gitbook/assets/image-12.png)

this corresponds to settings in application.yml:

```text
spring:
  cloud:
    config:
      server:
        overrides:
          foo: bar
```

