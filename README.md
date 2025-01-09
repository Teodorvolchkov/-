Практический Блок
Первая Часть
Задание 1 - Тестирование функциональности веб-приложения
Твоя задача — протестировать функциональность «Сделать заказ». Тесты на вёрстку напиши только для одного экрана. Подготовь их в виде чек-листа. Не забудь про кроссбраузерное тестирование. Баг-репорты оформи в YouTrack.

Технические примечания:

Тестовый стенд веб-приложения: https://{id}.serverhub.praktikum-services.ru/.
Работа сервера описана в специальной методичке.
Задание 2 - Ретест багов в мобильном приложении
Теперь возьмись за мобильное приложение. Разработчики исправили баги и отдали в тестирование. Тебе нужно провести ретест.

Технические примечания:

Чтобы авторизоваться в мобильном приложении, нужно создать курьера. Чтобы создать курьера, изучи документацию к API. Не забудь, что параметры для метода POST передаются в body запроса с типом JSON.
Чтобы настроить мобильное приложение на взаимодействие с бэкендом, кликни по значку «?» на главном экране в правом нижнем углу. Появится окно ввода. Укажи адрес подключения к API: https://{id}.serverhub.praktikum-services.ru и нажми «Ок».
Документация API: https://{id}.serverhub.praktikum-services.ru/docs/.
URL, который нужно использовать в запросах к API: https://{id}.serverhub.praktikum-services.ru.
Баг-репорты находятся здесь. Импортируй их в своё пространство.
Задание 3 - Регрессионное тестирование мобильного приложения по готовым тест-кейсам
Разработчики подготовили новую версию мобильного приложения. Перед релизом нужно провести регрессионное тестирование.

Подробнее:

Создай проект в Qase. Вспомни, как создать проект в этом уроке.
Загрузки в проект тесты. Файл для загрузки — здесь. Вспомни, как это сделать из этой инструкции.
Загрузи тест-кейсы для регрессионного тестирования в свой проект в Qase.
Вторая Часть
Задание 1 - Работа с базой данных
Представь: тебе нужно проверить, отображается ли созданный заказ в базе данных.

Для этого: выведи список логинов курьеров с количеством их заказов в статусе «В доставке» (поле inDelivery = true).

Задание 2 - Работа с базой данных
Ты тестируешь статусы заказов. Нужно убедиться, что в базе данных они записываются корректно.

Для этого: выведи все трекеры заказов и их статусы.

Правила определения статусов:

Если поле finished == true, то вывести статус 2.
Если поле cancelled == true, то вывести статус -1.
Если поле inDelivery == true, то вывести статус 1.
Для остальных случаев вывести 0.
Задание 3 - Автоматизация теста к API
Теперь автоматизируй сценарий, который подготовили коллеги-тестировщики:

Клиент создает заказ.
Проверяется, что по треку заказа можно получить данные о заказе.
Шаги автотеста:

Выполнить запрос на создание заказа.
Сохранить номер трека заказа.
Выполнить запрос на получение заказа по треку заказа.
Проверить, что код ответа равен 200.
