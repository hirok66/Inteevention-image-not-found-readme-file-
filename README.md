# Inteevention-image-not-found-readme-file-


Step 1:
Add "intervention/image": "2.7.x-dev" to the “require” section of your composer.json file.

"require": {
"laravel/framework": "^10.10*",
"intervention/image": "2.7.x-dev"
},
Step 2:
Run CMD;
$ composer install
If you've got this warning:

Warning: The lock file is not up to date with the latest changes in composer.json. You may be getting outdated dependencies. Run update to update them.

do $ composer update and then $ composer install

Step 3:
open the config/app.php file. Add this to the $providers array.

Intervention\Image\ImageServiceProvider::class
Step 4:
Next add this to the $aliases array.

'Image' => Intervention\Image\Facades\Image::class
Step 5:
If there is an error;

php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravelRecent"

Activity

