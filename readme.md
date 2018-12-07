##   Laravel Hello World exampe by C.R.Games <cla.radu@crgames.elementfx.com>

# License
The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
Please read the license file to know the conditions in which you can use and/or modify this project.

# Info
   For this application to work as intended you will need Xampp and Composer.
I have used xampp v.3.0.12 and composer v.1.5.2 but the it should work regardless of 
the versions of these two programs. Also, it should work on Laravel 5.0 and higher.
If there are any problems please let me know on my e-mail addres provided earlier.
   
   This example adds minor alterations to a laravel default project. It modifies 
laravel's default registration procedure to make possible for a user to be registered by 
more details like: username, first and last name, phone number. Also, the home page and 
the navigation bar have suffered slight modifications.

# Setup
Xampp: https://www.apachefriends.org/download.html

Composer: https://getcomposer.org/download/

  Xampp configuration:
  
  > Open "C:\xampp\apache\conf\extra\httpd-vhosts.conf" and add at the bottom of the file the 
  code below (the paths can be changed to your respective paths):

  VirtualHost for LARAVEL.DEV
  ```
  <VirtualHost laravel.dev:80>
      DocumentRoot "C:\xampp\htdocs\laravel_h_w\public"
      ServerAdmin laravel.dev
      <Directory "C:\xampp\htdocs\laravel_h_w">
          Options Indexes FollowSymLinks
          AllowOverride All
          Require all granted
      </Directory>
  </VirtualHost>
  ```
  
  Hosts file configuration (windows):
  
  > Open "C:\WINDOWS\system32\drivers\etc\hosts" and add at the bottom of the file the 
  line below:
  
  > `127.0.0.1       laravel.dev`
  
  > * Under Vindows 7 and later, your text editor must be run as administrator before opening
  the hosts file.
  
  Laravel configuration:
  
  * This project just replaces some of the files of a standard Laravel project so you first 
  need to create one: *
  
  > With 'Command Prompt' navigate to where you want to install to, so "xampp\htdocs\", and write 
  the following command:
  
  `"composer create-project laravel/laravel laravel_h_w" ( you can choose another name for 
  the project ) and hit enter.`

  > After the laravel project is installed download my example via Git, anywhere you want on your 
  hard drive, and just copy the files from it ( or the whole folder if the name is the same ) to 
  the newly created laravel project. You will be prompted to replace the old files, so click yes.
  
  > To download my project via Git open `Command Prompt`, then navigate to where you want to 
  download the files and write the following command:
    
  `git clone https://github.com/ClaRadu/laravel_h_w.git`
	
  > This example will require a database to be created with a tabble called `users` in it.
  Because you've been using Xampp you can use "phpmyadmin" to create the database.
  Go to "SQL" and under 'Run SQL query/queries on server "localhost":' write the following command:
  
  `create schema [database_name]`
  
  > for me it's `create schema usr_db`. Now open the ".env" file in the root folder of your 
  Laravel project. For me it's `":\xampp\htdocs\laravel_h_w\` and modify lines 5 to 8 like below:
  ```
    DB_HOST=localhost
    DB_DATABASE=usr_db ( your database name here )
    DB_USERNAME=root
    DB_PASSWORD=
  ```
  
  > Laravel offers the possibility to automatically migrate a table structure with data as well,
  but we'll migrate just the structure for now. Everything is allready set so you just need to 
  write in "Command Prompt" the following line: `php artisan migrate`.
  
Now that everything is set, open your internet browser and type `laravel.dev` in the address 
bar and you're good to go.

# Credits

A big thank you to Jeff Davis for his work on the laracasts forum (
https://laracasts.com/@jeffdavis ).

https://laracasts.com/discuss/channels/laravel/how-can-i-modify-laravel-5-login-system-and-add-on-registration-a-username-or-another-field?page=1

and to Marc Garcia on codementor.io (
https://www.codementor.io/magarrent ).

C.R.G. 2017
