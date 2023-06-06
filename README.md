# План автоматизации тестирования возможности записаться на обучение профессии «Тестировщик ПО».
*[www.netology.ru](https://netology.ru/)*


## 1. Перечень автоматизируемых сценариев
*Первый способ (через меню "Каталог курсов"):*
- Перейти на сайт [Нетология](https://netology.ru/)
- На главной странице выбрать меню "Каталог курсов"
- В разделе "Направления обучения" выбрать "Программирование"
- В списке выбрать "Тестировщик ПО"
- Нажать кнопку "Записаться" на странице профессии или пролистать всю страницу вниз до формы записи. 

*Второй способ (через раздел "Направления обучения"):*
- Перейти на сайт [Нетология](https://netology.ru/)
- На главной странице сайта в разделе "Направления обучения" выбрать "Программирование"
- Из списка профессий выбрать "Тестировщик ПО"
- Нажать кнопку "Записаться" на странице профессии или пролистать всю страницу вниз до формы записи.


### Позитивные сценарии:
***Ввод валидных значений на кириллице:***
- Ввести имя на кириллице
- Ввести номер телефона в формате +7 состоящий из 11 цифр
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма отправляется и появляется информация о записи

***Ввод валидных значений на латинице:***
- Ввести имя на латинице
- Ввести номер телефона в формате +7 состоящий из 11 цифр
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма отправляется и появляется информация о записи

***Ввод валидного номера телефона***
- Ввести имя на кириллице
- Ввести номер телефона в формате +7 состоящий из 11 цифр
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма отправляется и появляется информация о записи

### Негативные сценарии:

***Ввод невалидного имени(спец.символы):***
- Ввести в поле "Имя" спец.символы
- Ввести номер телефона в формате +7 состоящий из 11 цифр
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма не отправляется и появляется сообщение "Должно состоять из букв"

***Ввод невалидного имени(цифры):***
- Ввести в поле "Имя" любые цифры
- Ввести номер телефона в формате +7 состоящий из 11 цифр
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма не отправляется и появляется сообщение "Должно состоять из букв"

***Ввод невалидного номера телефона:***
- Ввести имя на кириллице
- Ввести в поле "Телефон" номер в формате: 9999999
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма не отправляется и появляется сообщение "Номер в формате +9 (999) 999-99-99"

***Отправка пустой формы***
- Оставить все поля пустыми
- Нажать кнопку "Записаться"  
**Ожидаемый результат:** Форма не отправляется и под полями появляются сообщения "Обязательное поле"

## 2. Перечень используемых инструментов с обоснованием выбора
**IntelliJ IDEA 2022.3.2 (Community Edition)** - написание кода. Удобство использования  
**Git** - система контроля версий. Удобство использования  
**Gradle** - система автоматической сборки  
**Lombok** - плагин для создания аннотаций. Создаст необходимые конструкторы, getters-setters и тд  
**Selenide** - фреймворк для написания удобных для чтения и обслуживания автоматизированных тестов на Java  
**JUnit 5** - библиотека для тестирования  
**Faker** - получение сгенерированных данных пользователя  
**Allure** - удобная система отчетов с получением необходимых скринов.  

## 3.Перечень необходимых разрешений/данных/доступов
- Данные будут генерироваться при помощи faker
- Требуется разрешение от сайта [Нетология](https://netology.ru/)
- Доступы к базе данных и API сайта.

## 4.Перечень и описание возможных рисков при автоматизации
- Нагрузка на сайт
- Появление большого количества тестов, модификация и поддержка становится сложнее
- Или наоборот малое количество тестов, тем самым малая часть покрытия функционала
- Медленные и устаревшие тесты
- Увеличение расходов на автоматизацию
- В ходе выполнения проекта может измениться структура сайта и локаторы придётся уточнять. Из-за этих изменений кода возникнут проблемы с тестами.


## 5.Перечень необходимых специалистов для автоматизации
Инженер по тестированию (QA-engineer). Возможно на начальном этапе будет достаточно тестировщика с гибридной ролью (ручное тестирование + автоматизация).

## 6.Интервальная оценка с учётом рисков (в часах)
- Получение(согласование) доступа к сайту - 10 часов
- Подготовка инструментов - 2-3 часа
- Генерация данных - 1 час
- Написание кода автотестов - 4-5 часов
- Отчетность - 3-5 часов.


