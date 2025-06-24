# Usage

```php
use Usama\FirebaseNotifications\FirebaseNotifications;

$notifier = new FirebaseNotifications();

$response = $notifier->send(
    $firebaseToken,
    'Test Title',
    'This is the body message',
    ['data' => ['customKey' => 'value']]
);
```

Optional payload can include `data`, `android`, `apns`, etc.
#Handling Errors
```php
use Usama\FirebaseNotifications\Exceptions\NotificationSendException;

try {
    $notifier = new FirebaseNotifications();
    $notifier->send($token, $title, $body);
} catch (NotificationSendException $e) {
    \Log::error('FCM error: ' . $e->getMessage());
}
```
