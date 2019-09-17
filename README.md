##Routes
/----------------------------
Add below line to Routes
/----------------------------
Auth::routes(['verify' => true]);


##User Model
/---------------------------
Add the implements as
/---------------------------
class User extends Authenticatable implements MustVerifyEmail


##Mail Vendor Edit
/--------------------------
Run, to be able to edit the mail vendor responsible for message displayed in Gmail
/--------------------------
php artisan vendor:publish

##.Env File Edit
/--------------------------
You can use mail trap to trap all emails coming from application, very simple and straight forward
Else if you use gmail direct, all gmail to be accessed by less secure application
/--------------------------
MAIL_DRIVER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your_email_address
MAIL_PASSWORD=your_email_password
MAIL_ENCRYPTION=tls

##Config/Mail.php
/---------------------------
Edit as below
/---------------------------

'host' => env('MAIL_HOST', 'smtp.gmail.com'),

'port' => env('MAIL_PORT', 587),

'encryption' => env('MAIL_ENCRYPTION', 'tls'),


##Success
/--------------------------
Your application should be up and running
/--------------------------