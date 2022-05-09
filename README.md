# pyodbc-sqlite-orm

基于pyodc和model连接sqlserver，实现无需编写sql语句即可进行数据库操作

## How to use it

```python
class DBModel(Model):
    name = StringField('name')
    date = StringField('date')
    age = IntegerField('age')
    table_name = 'DB_TABLE_NAME'


a_model = DBModel(
    sqlserver_db_driver_info='sqlserver::<server_ip>::<port>::<database_name>::<user>::<password>',
    sqlite_db_file_path='./test.db',
    name='zhangsan',
    date='2022-05-09',
    age=15
)

a_model.save_of_sqlserver()

```
