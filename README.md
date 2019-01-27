# Laravel Injection Cheat Sheet
A cheat-sheet for those who want to disband the practice of using facades and global helpers.

## Facades
|Facade   |Actual   |
|---|---|
|`App`   |`\Illuminate\Contracts\Foundation\Application`   |
|`Artisan`   |`\Illuminate\Contracts\Console\Kernel`   |
|`Auth`   |`\Illuminate\Contracts\Auth\Factory` \ `\Illuminate\Contracts\Auth\Guard` \ `\Illuminate\Contracts\Auth\StatefulGuard`   |
|`Blade`   |`\Illuminate\View\Compilers\BladeCompiler`   |
|`Broadcast`   |`\Illuminate\Contracts\Broadcasting\Factory`   |
|`Bus`   |`\Illuminate\Contracts\Bus\Dispatcher`   |
|`Cache`   |`\Illuminate\Contracts\Cache\Factory` \ `\Illuminate\Contracts\Cache\Repository`   |
|`Config`   |`\Illuminate\Contracts\Config\Repository`   |
|`Cookie`   |`\Illuminate\Contracts\Cookie\QueueingFactory`   |
|`Crypt`   |`\Illuminate\Contracts\Encryption\Encrypter`   |
|`DB`   |`\Illuminate\Database\Connectors\ConnectionFactory` \ `\Illuminate\Database\ConnectionInterface`   |
|`Event`   |`\Illuminate\Contracts\Events\Dispatcher`   |
|`File`   |`\Illuminate\Contracts\Filesystem\Filesystem`   |
|`Gate`   |`\Illuminate\Contracts\Auth\Access\Gate`   |
|`Hash`   |`\Illuminate\Contracts\Hashing\Hasher`   |
|`Input`   |`\Illuminate\Http\Request`   |
|`Lang`   |`Illuminate\Contracts\Translation\Translator`   |
|`Log`   |`\Psr\Log\LoggerInterface`   |
|`Mail`   |`\Illuminate\Contracts\Mail\Mailer`   |
|`Notification`   |`\Illuminate\Contracts\Notifications\Dispatcher`   |
|`Password`   |`\Illuminate\Contracts\Auth\PasswordBroker`   |
|`Queue`   |`\Illuminate\Contracts\Queue\Factory` \ `\Illuminate\Queue\Queue`   |
|`Redirect`   |`\Illuminate\Routing\Redirector`   |
|`Redis`   |`\Illuminate\Contracts\Redis\Factory`   |
|`Request`   |`\Illuminate\Http\Request`   |
|`Response`   |`\Illuminate\Contracts\Routing\ResponseFactory`   |
|`Route`   |`\Illuminate\Contracts\Routing\Registrar` \ `\Illuminate\Contracts\Routing\BindingRegistrar`   |
|`Schema`   |`\Illuminate\Database\Schema\Builder`   |
|`Session`   |`\Illuminate\Contracts\Session\Session`   |
|`Storage`   |`\Illuminate\Contracts\Filesystem\Factory`   |
|`URL`   |`\Illuminate\Contracts\Routing\UrlGenerator`   |
|`Validator`   |`\Illuminate\Contracts\Validation\Factory`   |
|`View`   |`\Illuminate\Contracts\View\Factory`   |

## Helpers
Some of these call a specific method on a specific contract, those will have a `@method()` syntax added behind the class.

|Helper   |Actual   |
|---|---|
|`action()`   |`\Illuminate\Contracts\Routing\UrlGenerator@action()`   |
|`app()`   |`\Illuminate\Contracts\Foundation\Application`   |
|`asset()`   |`\Illuminate\Contracts\Routing\UrlGenerator@asset()`   |
|``   |``   |
|``   |``   |
|``   |``   |
|``   |``   |
|``   |``   |
|``   |``   |