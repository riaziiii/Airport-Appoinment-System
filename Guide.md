composer create-project Laravel/Laravel airport-appointment
cd airport-appointment

xammp- mysql>data copy>rename data_old>data>delete except ibdata1>backup mysql>copy except ibdata1>paste data folder

php artisan serve(for run php)
php artisan migrate(for update the database)
npm install
npm run dev(for run tailwindcss or live update)

--

guide
php artisan make:model Product -mcr --requests 

-m: creates migration
-c: resource controller
-r: generates all resource methods (index, create, store, show, edit, update, destroy)
--requests: auto-generates form request validation classes


php guide(for backup)
Xampp mysql database>backup>export


php artisan migrate:refresh(refreshing database system)

Two way Create Routes

(First way of route)
Route::get('/', function () {
    return view('welcome');
})->name('welcome');

Example of routing:
 <a href="{{ route('dashboard') }}">dashboard</a>	

 (2nd way of route web php)
  use App\Http\Controllers\ProductController;
  Route::resource('products', ProductController::class);     

  
  (for Controller)
  public function index()
    {
        return view('products/index');
    }  
  
     