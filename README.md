## Дипломный проект по профессии "Тестировщик"
---------------------------------------------



### Предусловия работы
Для запуска проекта на ПК должны быть установлены:
- Intellej IDEA Ultimate
- Java 11
- Docker
- Git

### Запуск приложения
Открыть проект в IntelliJ IDEA Ultimate.
Запустить Docker на ПК.

В терминале IDEA выполнить команду
`docker-compose up`

В другой вкладке терминала выполнить команду для запуска приложения на СУБД MySQL
`java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar`

В другой вкладке теринала выполнить команду для запуска тестов
`.\gradlew test "-Ddb.url=jdbc:mysql://localhost:3306/app"`

затем
`.\gradlew allureServe `
Для запуска приложения на СУБД PostgreSQL
`java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar`
Тесты запускаются командой в другой вкладке терминала
`.\gradlew test "-Ddb.url=jdbc:postgresql://localhost:5432/app"`
