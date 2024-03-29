# Дипломный проект по курсу «Тестировщик программного обеспечения»
[Задание на дипломную работу](https://github.com/netology-code/qa-diploma/blob/master/README.md) 

## Документация

- [План](https://github.com/Maxon1975/Diploma-Annenkov/blob/master/documents/Plan.md)
- [Отчет по результатам тестирования](https://github.com/Maxon1975/Diploma-Annenkov/blob/master/documents/Peport.md)
- [Отчет по итогам автоматизации](https://github.com/Maxon1975/Diploma-Annenkov/blob/master/documents/Summary.md)

## Запуск приложения и тестов

Для запуска приложения и тестов  должен быть установлен Docker или Docker Toolbox.
Для загрузки репозитория используется команда: `git clone https://github.com/Maxon1975/Diploma-Annenkov-Maksim.git`

Для запуска docker-контейнера с СУБД PostgreSQL и MySQL, а также Node.js необходимо открыть терминал в папке проекта и ввести команду `docker-compose up -d`

### Для запуска приложения и тестов с MySQL используются команды:

- Запуск приложения `java -jar aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app`. Дождаться появления строки `ru.netology.shop.ShopApplication : Started ShopApplication ...`
- Запуск автотестов `./gradlew clean test -Ddb.url=jdbc:mysql://localhost:3306/app allureReport`

### Для запуска приложения и тестов с PostgreSQL используются команды:

- Запуск приложения `java -jar aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app`. Дождаться появления строки `ru.netology.shop.ShopApplication : Started ShopApplication ...`
- Запуск автотестов `./gradlew clean test -Ddb.url=jdbc:postgresql://localhost:5432/app allureReport`

## Отчёты

Для того, чтобы посмотреть результаты прогона автотестов, нужно  запустить в терминале команду: `./gradlew allureServe`, результаты будут доступны по адресу: `http://localhost:37653/index.html`

## Остановка сервисов

Для остановки AllureServe и приложения используется сочетание клавиш **CRTL + C**
