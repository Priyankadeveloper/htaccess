
php_value upload_max_filesize 64M
php_value post_max_size 64M
php_value max_execution_time 300
php_value max_input_time 300
# BEGIN WordPress
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /parentchild/
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /parentchild/index.php [L]
</IfModule>

# END WordPress
