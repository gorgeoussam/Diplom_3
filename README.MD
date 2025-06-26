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