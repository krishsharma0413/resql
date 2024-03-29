# <p align="center"> resql: Database For Beginners </p>

[![Downloads](https://pepy.tech/badge/resql)](https://pepy.tech/project/resql)

## Quick Examples
<br>

imports

```
pip install resql
```



```python
import resql

database = resql.ReSql("mydb.db")
# default is in :memory:
```

<br>

## .create_table(name)

creates a database table.

```python
database.create_table("newtable")
# {'status': 'success', 'table': 'newtable'}
```

<br>


## .insert(key, value, [table])

insert into given table.

```python
database.insert("key","value")
# {'status': 'success'}
```

<br>


## .all([table])

find data from given table.

```py
database.all()
# [('key','value')]
```

<br>

## .find(key, [table]) or .get(key, [table])

find data from given table.

```py
database.find("key")
# value
```

<br>

## .wipe([table])

wipe complete table.


```py
database.wipe()
# {'status': 'success'}
```

<br>

## .run(sql)

directly run sql query.

```py
database.run("SELECT * FROM table")
# cursor
```

<br>

## .delete(key, [table])

delete key from table.

```py
database.delete("key")
# value
```


thanks to [avonryle#2022](https://github.com/avonryle) for letting me make the python version of [ByteDatabase](https://github.com/cloudteamdev/ByteDatabase)



