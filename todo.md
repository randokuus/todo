#juurkaustas, loome uue projekti kausta
composer create-project --prefer-dist laravel/laravel todo

#muuda .env faili (pane andmebaasi kastuaja ja andmebaasi nim paika)

#loome "tasks" tabeli loomiseks "migratsiooni" faili
php artisan make:migration create_tasks_table --create=tasks
#lisasisme "tasks" tabeli up funktsiooni $table->string('name');

#mariaDB-d kasutades tuleb muuta app->providers->AppServiceProvider.php faili
php artisan migrate

#loob Task mudeli app kausta
php artisan make:model Task