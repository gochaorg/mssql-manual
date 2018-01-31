Создание пользователя
=====================

[Общие сведения](https://docs.microsoft.com/ru-ru/sql/relational-databases/security/authentication-access/getting-started-with-database-engine-permissions)

Создание пользователя
---------------------
![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/05.png)
1. В окне **Object Browser/Обозреватель** на ветке **../Security/Logins** правой кл мыши - выбрать **новый пользователь (New Login)**

Общие свойства
--------------
![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/06.png)
На вкладке Общие/General указать
1. Имя логина
2. Режим аунтификации: SQL - пользователь прописан в базе / Windows - в ОС/Active Directory
3. Указать пароль (для SQL пользователя)
4. Снять галку [Enfore password policy](https://docs.microsoft.com/ru-ru/sql/relational-databases/security/password-policy), чтоб не мучатся со сложностью пароля и его просрочкой
5. Указать базу по умолчанию

Роли уровня сервера
-------------------
![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/07.png)
1. На вкладке [Роли сервера / Server Roles](https://docs.microsoft.com/ru-ru/sql/relational-databases/security/authentication-access/server-level-roles) указать
2. Роль public - доступ по умолчанию

Роли уровня БД
--------------
При переходе на вкладку User Mapping  может появится след. сообщение:
![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/08.png)
т.е. Одна из баз не доступна (offline или еще чтонибудь) - Нажать ОК

![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/09.png)
1. Перейти на вкладку User Mapping
2. В списке баз выбрать интересующую базу, пользователь будет выбран автоматически
3. Указать [роли уровня баз данных](https://docs.microsoft.com/ru-ru/sql/relational-databases/security/authentication-access/database-level-roles) (public и db_owner)

Статус логина
-------------
![alt](https://github.com/gochaorg/mssql-manual/raw/master/images/create-login/10.png)
1. На вкладке **Статус/Status** указать
2. Сonnect = **Grant** (Разрешено), Login = **Enabled** (Доступно/Разрешено)
