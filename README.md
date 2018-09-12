# increase-file-upload-size-php
Increase file upload size in PHP using **cPanel** or **FTP** by adding/modifying  **.htaccess** , **.user.ini** and **php.ini** file.

> Here i'm increasing file upload size to 50 MB , you can increase what size you want, **Note : post_max_size is always greater than upload_max_filesize**

> Either follow bellow steps or just download bellow files and upload in Root folder of your project
- [.htaccess](https://github.com/niteshnic05/increase-file-upload-size-php/blob/master/.htaccess)
- [.user.ini](https://github.com/niteshnic05/increase-file-upload-size-php/blob/master/.user.ini)
- [.php.ini](https://github.com/niteshnic05/increase-file-upload-size-php/blob/master/php.ini)

## Step 1: Create a .htaccess file in your project root folder
> (Note : skip above step if *.htaccess* file is alreay there)
  ### Step 1.1 : Copy and Paste below code to *.htaccess* file
  ```
  <IfModule php5_module>
   php_flag asp_tags Off
   php_flag display_errors On
   php_value max_execution_time 30
   php_value max_input_time 60
   php_value max_input_vars 1000
   php_value memory_limit 600M
   php_value post_max_size 80M
   php_value session.gc_maxlifetime 1440
   php_value session.save_path "/tmp"
   php_value upload_max_filesize 50M
   php_flag zlib.output_compression Off
</IfModule>
```
## Step 2: Create a *.user.ini* file in your project root folder
> (Note : skip above step if *.user.ini* file is alreay there)
  ### Step 2.1 : Copy and Paste below code to *.user.ini* file
  
  ```
asp_tags = Off
display_errors = On
max_execution_time = 30
max_input_time = 60
max_input_vars = 1000
memory_limit = 600M
post_max_size = 80M
session.gc_maxlifetime = 1440
session.save_path = "/tmp"
upload_max_filesize = 50M
zlib.output_compression = Off

```

## Step 3: Create a *php.ini* file in your project root folder
> (Note : skip above step if *php.ini* file is alreay there)
  ### Step 3.1 : Copy and Paste below code to *php.ini* file
  
  ```
  allow_url_fopen = On
allow_url_include = Off
asp_tags = Off
display_errors = On
enable_dl = On
file_uploads = On
max_execution_time = 30
max_input_time = 60
max_input_vars = 1000
memory_limit = 600M
post_max_size = 80M
session.gc_maxlifetime = 1440
session.save_path = "/tmp"
upload_max_filesize = 50M
zlib.output_compression = Off

```

