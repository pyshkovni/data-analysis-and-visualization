# Начало работы с блокнотом Jupyter

План

* Проект Jupyter и Anaconda
* Создание блокнота и особенности работы
* Git
* Задание: Подготовка к проекту и подключение к данным

Код для вставки

```Python
# импорт клиента базы данных и 
# импорт библиотеки для работы с датасетами
import psycopg2
import pandas as pd

# подключение к базе данных
conn = psycopg2.connect("""
    host=rc1a-6m93avglbdi9qbfw.mdb.yandexcloud.net,rc1b-7qb273fd9rgaw8me.mdb.yandexcloud.net
    port=6432
    dbname=designer_store
    user=student
    password=n123456789
    target_session_attrs=read-write
""")

# запрос данных из базы данных
# нужен SQL-синтаксис
pd.read_sql_query("SELECT * FROM designer_store.customers LIMIT 10", con=conn)
```
