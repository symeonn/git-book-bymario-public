# config server

### OVERRIDES

there is a .yml file in configuration files \(hosted from Git\):

![](../../../.gitbook/assets/image%20%288%29.png)

and during config-server deployment it can be also set as \(using overrides\):

![](../../../.gitbook/assets/image%20%2812%29.png)

this corresponds to settings in application.yml:

```text
spring:
  cloud:
    config:
      server:
        overrides:
          foo: bar
```

