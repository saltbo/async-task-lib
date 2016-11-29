# async-task-lib
An event based asynchronous task processing library

## Setup ##

 Add a `composer.json` file to your project:

```javascript
{
  "require": {
      "luojilab/php-async-lib": "1.0.*"
  }
}
```

Then provided you have [composer](http://getcomposer.org) installed, you can run the following command:

```bash
$ composer.phar install
```

That will fetch the library and its dependencies inside your vendor folder.


## Usage ##

With Message mode running open two Terminals and on the first one execute the following commands to start the worker:

```bash
$ cd php-async-lib/demo
$ php Worker.php
```

Then on the other Terminal do:

```bash
$ cd php-async-lib/demo
$ php Publish.php some text to publish
```

You should see the message arriving to the process on the other Terminal


With Event mode running open three Terminals and on the first one execute the following commands to start the worker:

```bash
$ cd php-async-lib/demo
$ php event/scheduler.php
```

Then on the second Terminal do:

```bash
$ cd php-async-lib/demo
$ php event/worker.php
```

Then on the last Terminal do:

```bash
$ cd php-async-lib/demo
$ php event/event.php
```

You should see the message arriving to the process on the second Terminal


## Authors && Contributors

- [Monky](https://github.com/boboyan)

## License

licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html)