# Add Custom Helper Laravel 9
To add a custom helper function in Laravel 9, you can follow these steps:

1. Create a new PHP file in the app/Helpers directory. This is the recommended location for custom helpers in Laravel.

2. In the PHP file, define your helper function. For example:
```
<?php

if (! function_exists('exampleHelper')) {
    function exampleHelper()
    {
        return 'This is an example helper function';
    }
}
```
3. In your composer.json file, add the app/Helpers directory to the autoload section:
```
"autoload": {
    "classmap": [
        "database/seeds",
        "database/factories"
    ],
    "psr-4": {
        "App\\": "app/"
    },
    "files": [
        "app/Helpers/helpers.php"
    ]
},
```
4. Run the composer dump-autoload command to regenerate the autoloader.

5. You can now use the helper function in your application by calling it like any other PHP function:
```
echo exampleHelper();
```

Note that you can also define multiple helper functions in the same file, or create separate files for different groups of helpers. Just make sure to add each file to the **autoload** section of your **composer.json** file as shown above.
