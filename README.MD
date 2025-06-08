tests/ - папка с файлами тестов

tests/test_forgot_password_page.py - тесты функциональности Восстановление пароля
tests/test_profile_page.py - тесты функциональности Личный кабинет
tests/test_constructor_page.py - тесты основного функционала (Главная страница)
tests/test_feed_page.py - тесты раздела «Лента заказов»
pages/ - папка page object (классы страниц РОМ):

pages/base_page - класс базового класса для классов страниц, общие методы
pages/main_page - класс Главной страницы
pages/login_page - класс страницы авторизации
pages/forgot_password_page - класс страницы восстановления пароля
pages/reset_password_page - класс страницы сброса пароля
pages/profile_page - класс страницы Личного кабинета
pages/constructor_page - класс раздела Конструктор на Главной страницы
pages/feed_page - класс раздела Лента заказов на Главной странице
helpers/ - папка вспомогательных функций:

helpers/common_helpers.py - общие функции
helpers/helpers_on_requests.py - функции для выполнения запросов к API (создание и удаление пользователя)
helpers/helpers_on_register_user.py - функции для работы с пользователями
conftest.py - функции-фикстуры

locators.py - файл классов локаторов для страниц

data.py - константы, URL-адреса и данные для тестов

.gitignore - файл для проекта в Git/GinHub

requirements.txt - файл внешних зависимостей

README.md - файл с описанием проекта (этот файл)

Для запуска тестов должны быть установлены пакеты:
pytest
requests
selenium
allure-pytest
allure-python-commons
Для генерации отчетов необходимо дополнительно установить:
фреймворк JDK
пакет Allure
Запуск всех тестов выполняется командой:

$ pytest -v ./tests

Запуск тестов с генерацией отчета Allure выполняется командой:

$ pytest -v ./tests  --alluredir=allure_results

Генерация отчета выполняется командой:

$ allure serve allure_results

Генерация файла внешних зависимостей requirements.txt выполняется командой:

$ pip freeze > requirements.txt

Установка зависимостей из файла requirements.txt выполняется командой:

$ pip install -r requirements.txt