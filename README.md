## Модуль 7. Паттерны микросервисной архитектуры

---

### Задача:
Добавить к существующей системе паттерны: gateway api, service discovery, circuit breaker, external configuration - 
реализации данных паттернов можно найти в модулях spring cloud.

---

### Описание:
* Директория с [проектом](https://github.com/MikhailAkulov/springboot_user-service_micro_arch)
* Прямые ссылки: 
  * [config-server](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/tree/main/config-server):
    * [application.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/config-server/src/main/resources/application.yml)
    * [discovery-server.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/config-server/src/main/resources/config/discovery-server.yml)
    * [user-service.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/config-server/src/main/resources/config/user-service.yml)
    * [api-gateway.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/config-server/src/main/resources/config/api-gateway.yml)
    * [точка входа](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/config-server/src/main/java/com/akulov/springboot/configserver/ConfigServerApplication.java)
      * порт стандартный: 8080
  * [discovery-server](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/tree/main/discovery-server)
    * [application.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/discovery-server/src/main/resources/application.yml)
    * [точка входа](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/discovery-server/src/main/java/com/akulov/springboot/discoveryserver/DiscoveryServerApplication.java)
      * порт стандартный: 8761
  * [user-service](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/tree/main/user-service)
    * [application.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/user-service/src/main/resources/application.yml)
    * [точка входа](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/user-service/src/main/java/com/akulov/springboot/userservice/UserServiceApplication.java)
      * порт: 8081
      * swagger-ui: /swagger-ui.html
      * api-docs: v3/api-docs
  * [api-gateway](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/tree/main/api-gateway)
    * [application.yml](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/api-gateway/src/main/resources/application.yml)
    * [точка входа](https://github.com/MikhailAkulov/springboot_user-service_micro_arch/blob/main/api-gateway/src/main/java/com/akulov/springboot/apigateway/ApiGatewayApplication.java)
      * порт: 8082
    