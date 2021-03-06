#Setting up PHP

For **[Windows users](http://windows.php.net/download#php-5.6)**, just download PHP as the zip folder and unzip it wherever you want your PHP directory. This will only include a standard set-up, and more advanced aspects will require custom compilation or finding a pre-configured version that suits your needs.

Once you have PHP available on your computer, you will need to [set the path environment variables](http://www.computerhope.com/issues/ch000549.htm) on your OS to point to the PHP folder, or you will need to store all your PHP projects in a folder within your PHP folder.

For **Mac users**, PHP is bundled with your operating system and should be accessible. However, it's recommended that you  update to the latest version. More information for Mac users can be found [here](http://www.phptherightway.com/#mac_setup). The easiest looking way seems to be using [Homebrew](http://brew.sh/). However, you may find it difficult to understand. I would recommend taking a look and seeing whether you can get it running. If you succeed, add any useful information to this file. If you can't get it working, please let me know and I'll see if I can get it running.

PHP, as of version 5.4, comes with an inbuilt web server. This means that you can test PHP code on a website without running additional software such as Apache.

To run the web server, open command line on your computer. For **Windows users** press ctrl+r and type cmd. For **Mac users** running OS X, open your Applications folder, then open the Utilities folder. Open the Terminal application.

The command to run the web server is: `php -S localhost:8000`

*Please ensure you include a capital S in the -S argument.*

To access the web server, open your browser and type localhost:8000. You should recieve the message "The requested resource `/` was not found on this server." If this is not working, navigate to the php directory in command line using cd [directory name] to change directories.

The next step is to specify a root directory/folder for the web server. Include the path information for the root folder after the localhost:8000 argument in your command. Your default root folder is the folder command line is currently pointing to.

`php -S localhost:8000 -t test`

The next step, is to include a php file for the server to read when someone enters the server address. My file test.php contains the following code:

```
<?php
echo "Welcome to PHP";
?>
```

With the root directory test selected and the php web server, entering the address http://localhost:8000/test.php into my browsers displays the message Welcome to PHP.
