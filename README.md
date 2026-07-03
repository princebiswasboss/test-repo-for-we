# MikroTik Hotspot File Manager

A simple file management system for **MikroTik Hotspot** users. This project allows hotspot users to securely upload, download, and manage files through a web interface integrated with a MikroTik Hotspot login system.

## Features

* User authentication with MikroTik Hotspot
* Upload files
* Download files
* Delete files (with permission)
* User-specific storage
* File size restrictions
* Search and filter files
* Responsive web interface
* Admin dashboard
* Upload progress bar
* File type validation
* Activity logs

## Requirements

* MikroTik RouterOS (Hotspot Enabled)
* Web Server (Apache or Nginx)
* PHP 8.1+
* MySQL / MariaDB
* RouterOS API (optional for advanced integration)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/mikrotik-hotspot-file-manager.git
cd mikrotik-hotspot-file-manager
```

### 2. Configure the Web Server

Move the project to your web server directory.

Example:

```
/var/www/html/filemanager
```

or

```
C:\xampp\htdocs\filemanager
```

### 3. Import Database

Import the SQL file.

```
database/database.sql
```

### 4. Configure Database

Edit:

```
config/database.php
```

Example:

```php
$db_host = "localhost";
$db_name = "hotspot";
$db_user = "root";
$db_pass = "";
```

### 5. Configure Upload Directory

Create:

```
uploads/
```

Grant write permission.

Linux:

```bash
chmod -R 775 uploads
```

## MikroTik Configuration

### Enable Hotspot

```
IP → Hotspot
```

Create your hotspot server.

### Configure Login Page

Replace the default hotspot login page with:

```
hotspot/login.html
```

or redirect users to

```
http://yourserver/filemanager/login.php
```

### (Optional) RouterOS API

Enable API:

```
IP → Services
```

Enable:

```
api
```

Default Port:

```
8728
```

Configure credentials in:

```
config/router.php
```

Example:

```php
$router_ip = "192.168.88.1";
$username = "admin";
$password = "password";
```

## Folder Structure

```
project/
│
├── admin/
├── uploads/
├── users/
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
├── config/
├── database/
├── api/
├── login.php
├── dashboard.php
├── upload.php
├── download.php
├── delete.php
└── README.md
```

## Screenshots

* Login Page
* Dashboard
* Upload Files
* File List
* Admin Panel

(Add screenshots here.)

## Security

* Password hashing
* Session authentication
* File type validation
* Maximum upload size
* CSRF protection
* SQL Injection protection using prepared statements
* XSS filtering

## Future Features

* Folder support
* Drag & Drop upload
* File sharing links
* QR Code download
* Multiple file upload
* Cloud backup
* Email notifications
* User storage quota
* Image preview
* File version history

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push the branch.
5. Open a Pull Request.

## License

This project is licensed under the MIT License.

## Author

**Prince Biswas**

* GitHub: https://github.com/yourusername
* Email: [your@email.com](mailto:your@email.com)

---

If you find this project useful, please give it a ⭐ on GitHub.
****
