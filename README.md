# Стек технологий в проекте

* Flask
* SQLite
* Python

## Описание проекта

Проект YaCut — это сервис укорачивания ссылок. Его назначение — ассоциировать длинную пользовательскую ссылку с короткой, которую предлагает сам пользователь или предоставляет сервис.

## Запуск проекта

Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone git@github.com:Devayter/yacut.git
```

```bash
cd yacut
```

Cоздать и активировать виртуальное окружение:

```bash
python3 -m venv venv
```

* Если у вас Linux/macOS

    ```bash
    source venv/bin/activate
    ```

* Если у вас windows

    ```bash
    source venv/scripts/activate
    ```

Установить зависимости из файла requirements.txt

```bash
python3 -m pip install --upgrade pip
```

```bash
pip install -r requirements.txt
```

Запустить интерактивную оболочку Flask

```bash
Flask shell
```

Для создания БД поочередно ввести команды

```shell
>>>from opinions_app import db
```

```shell
>>> db.create_all()
```

Выйти из интерактивного режима `Ctrl + C` и запустить программу

```bash
flask run
```

## Примеры запросов

* Создание короткой ссылки

### POST

```url
http://localhost/api/id/
```

```json
{
  "url": "string",
  "custom_id": "string"
}
```

или

```json
{
  "url": "string"
}
```

* Ответ

```json
{
  "url": "string",
  "short_link": "string"
}
```

* Получение оригинальной ссылки по указанному короткому идентификатору

#### GET

```url
http://localhost/api/id/<short_id>/
```

* Ответ

```json
{
  "url": "string"
}
```

или

```json
{
  "message": "Указанный id не найден"
}
```

## Авторы

* Павел Рябов
