# Парсер PEP на BS4

[![py-doc-parser workflow](https://github.com/alex-zharinov/py_doc_parser/actions/workflows/main.yml/badge.svg)](https://github.com/alex-zharinov/py_doc_parser/actions/workflows/main.yml)

## Парсинг документов PEP
> Парсер собирает данные обо всех PEP документах, сравнивает статусы и записывает их в файл,
также реализованы сбор информации о статусе версий, скачивание архива с документацией и сбор ссылок о новостях в Python.

## Технологии проекта
- Python — высокоуровневый язык программирования;
- BeautifulSoup4 — библиотека для парсинга;
- tqdm — это библиотека Python, которая позволяет выводить интеллектуальный индикатор выполнения, оборачивая любую итерацию;
- argparse — парсер параметров командной строки;
- Prettytable — библиотека для удобного отображения табличных данных.

### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/alex-zharinov/py_doc_parcer.git
```
```
cd py_doc_parcer
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv
```
* Если у вас Linux/macOS
    ```
    source venv/bin/activate
    ```
* Если у вас windows
    ```
    source venv/scripts/activate
    ```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```

## Работа с парсером:
### Режимы работы
Сброр ссылок на статьи о нововведениях в Python:
```bash
python main.py whats-new
```
Сброр информации о версиях Python:
```bash
python main.py latest-versions
```
Скачивание архива с актуальной документацией:
```bash
python main.py download
```
Сброр статусов документов PEP и подсчёт статусов:
```bash
python main.py pep
```

### Аргументы командной строки
Полный список аргументов:
```bash
python main.py -h
```
```bash
usage: main.py [-h] [-c] [-o {pretty,file}] {whats-new,latest-versions,download,pep}

Парсер документации Python

positional arguments:
  {whats-new,latest-versions,download,pep}
                        Режимы работы парсера

optional arguments:
  -h, --help            show this help message and exit
  -c, --clear-cache     Очистка кеша
  -o {pretty,file}, --output {pretty,file}
                        Дополнительные способы вывода данных
```

## Автор
[Жаринов Алексей](https://github.com/alex-zharinov)
