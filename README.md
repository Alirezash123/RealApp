RewriteEngine On

# هر درخواست برای register.php رو به myCloud/register.php بفرست
RewriteRule ^register\.php$ myCloud/register.php [L]

# هر درخواست برای home.php رو به myCloud/home.php بفرست
RewriteRule ^home\.php$ myCloud/home.php [L]

# درخواست خالی (root) رو به home.php بفرست
RewriteRule ^$ myCloud/home.php [L]