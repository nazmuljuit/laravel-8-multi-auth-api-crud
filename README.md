#After fress laravel installation ,laravel multi auth has been created.

#Install Sanctum

composer require laravel/sanctum

#Next, we have to publish the sanctum configuration

php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"

#Add Sanctum Middleware

We have to add sanctum middleware to api middleware group inside app/Http/Kernel.php file:-

 \Laravel\Sanctum\Http\Middleware\EnsureFrontendRequestsAreStateful::class,


 #Create Model & Migration


 php artisan make:model Program -m


 #Create API Resource

 php artisan make:resource ProgramResource

 #Create Controller

php artisan make:controller API/ProgramController
