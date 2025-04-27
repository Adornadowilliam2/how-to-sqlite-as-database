
#  Steps to use database.sqlite in Laravel on Windows:

### 1. Create the SQLite database file
In Command Prompt, PowerShell, or your terminal inside VS Code, run:

```php
type nul > database\database.sqlite
```

### 2. Update .env
Open your .env file and change the database settings like this:

```php
DB_CONNECTION=sqlite
DB_DATABASE=database/database.sqlite

```
-  Important: Use forward slashes (/) even on Windows — Laravel handles them fine.

Also, remove or comment out these lines (they're not used for SQLite):

```php
# DB_HOST=127.0.0.1
# DB_PORT=3306
# DB_USERNAME=root
# DB_PASSWORD=
```

### 3. Run Migrations
Now you're ready:
```php
php artisan migrate
```

