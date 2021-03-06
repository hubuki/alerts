> fork from socieboy/alerts

## Laravel 5 Alerts

### Installation

Add to your composer.json file the package.

```
"hubuki/laravel-sweetalert" : "dev-master"
```

Update your dependencies

```
composer update
```

After install this package you have to set the service provider on your config/app.php file

```
Hubuki\LaravelSweetAlert\LaravelSweetAlertServiceProvider::class
```

[//]: # (Copy the required assets of SweetAlert to your public folder.)
[//]: # (Those assets would be place in the css and js respective directory.)

[//]: # (```)
[//]: # (php artisan vendor:publish --tag=alerts)
[//]: # (```)


[//]: # (Then in your master view add those styles and scripts.)
[//]: # (Put this style between the \<head\> \</head\> tags)
[//]: # (```)
[//]: # (<link rel="stylesheet" type="text/css" href="css/sweetalert.css">)
[//]: # (```)
Add the JS script before close your \</body\> tag.
```
<script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js"></script>
```

Include the alerts view to your master view.
Add this code right after set the JS script file.
```
@include('LaravelSweetAlert::show')
```


### Usage

On your controllers is a perfect place to use it, any way you can fire the alerts from jobs or events.

```
alert('Title', 'Message')

alert()->error('Title', 'Message')

alert()->success('Title', 'Message')

alert()->overlay('Title', 'Message')
```

Override the type of overlay

```
alert()->overlay('Title', 'Message', 'error')
// success (default)
// error
// info
```


#### SweetAlerts website

https://sweetalert.js.org/


