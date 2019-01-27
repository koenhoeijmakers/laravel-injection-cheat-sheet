# Laravel Injection Cheat Sheet
A cheat-sheet for those who want to disband the practice of using facades and global helpers.

- [Facades](#facades)
- [Helpers](#helpers)

## Facades
|Facade   |Actual   |
|---|---|
|`App`   |`\Illuminate\Contracts\Foundation\Application`   |
|`Artisan`   |`\Illuminate\Contracts\Console\Kernel`   |
|`Auth`   |`\Illuminate\Contracts\Auth\Factory` \ `\Illuminate\Contracts\Auth\Guard`   |
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
|`Lang`   |`\Illuminate\Contracts\Translation\Translator`   |
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
Helpers may call specific methods depending on the parameters, if that is the case only the implementation is shown in _Actual_.

|Helper   |Actual   |
|---|---|
|`action()`   |`\Illuminate\Contracts\Routing\UrlGenerator@action()`   |
|`app()`   |`\Illuminate\Contracts\Foundation\Application`   |
|`asset()`   |`\Illuminate\Contracts\Routing\UrlGenerator@asset()`   |
|`auth()`   |`\Illuminate\Contracts\Auth\Factory` \ `\Illuminate\Contracts\Auth\Guard`   |
|`back()`   |`\Illuminate\Routing\Redirector@back()`   |
|`bcrypt()`   |`\Illuminate\Contracts\Hashing\Hasher@make()`   |
|`broadcast()`   |`\Illuminate\Contracts\Broadcasting\Factory@event()`   |
|`cache()`   |`\Illuminate\Contracts\Cache\Factory`   |
|`config()`   |`\Illuminate\Contracts\Config\Repository`   |
|`cookie()`   |`\Illuminate\Contracts\Cookie\QueueingFactory`   |
|`decrypt()`   |`\Illuminate\Contracts\Encryption\Encrypter@decrypt()`   |
|`dispatch()`   |`\Illuminate\Contracts\Bus\Dispatcher@dispatch()`   |
|`dispatch_now()`   |`\Illuminate\Contracts\Bus\Dispatcher@dispatchNow()`   |
|`decrypt()`   |`\Illuminate\Contracts\Encryption\Encrypter@encrypt()`   |
|`event()`   |`\Illuminate\Contracts\Events\Dispatcher@dispatch()`   |
|`factory()`   |`\Illuminate\Database\Eloquent\FactoryBuilder`   |
|`info()`   |`\Psr\Log\LoggerInterface@info()`   |
|`logger()`   |`\Psr\Log\LoggerInterface`   |
|`logs()`   |`\Psr\Log\LoggerInterface`   |
|`old()`   |`\Illuminate\Http\Request@old()`   |
|`policy()`   |`\Illuminate\Contracts\Auth\Access\Gate@getPolicyFor()`   |
|`redirect()`   |`\Illuminate\Routing\Redirector`   |
|`report()`   |`\Illuminate\Contracts\Debug\ExceptionHandler`   |
|`request()`   |`\Illuminate\Http\Request`   |
|`resolve()`   |`\Illuminate\Contracts\Foundation\Application`   |
|`response()`   |`\Illuminate\Contracts\Routing\ResponseFactory`   |
|`route()`   |`\Illuminate\Contracts\Routing\UrlGenerator@route()`   |
|`session()`   |`\Illuminate\Contracts\Session\Session`   |
|`trans()`   |`\Illuminate\Contracts\Translation\Translator`   |
|`trans_choice()`   |`\Illuminate\Contracts\Translation\Translator@transChoice()`   |
|`__()`   |`\Illuminate\Contracts\Translation\Translator@getFromJson()`   |
|`url()`   |`\Illuminate\Contracts\Routing\UrlGenerator`   |
|`validator()`   |`\Illuminate\Contracts\Validation\Factory`   |
|`view()`   |`\Illuminate\Contracts\View\Factory`   |
