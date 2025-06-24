## 📚 Full Documentation
<h1 align="center" style="color:#ff6f61;">🔥 Laravel Firebase Notifications (OAuth2)</h1>

<p align="center">
  <strong style="color:#2e86de;">Send Firebase Cloud Messaging (FCM) notifications securely using OAuth2 in Laravel.</strong>
</p>

<hr />

<h2 style="color:#28a745;">📦 Installation</h2>

<pre><code>composer require usamatoor/firebase-notifications</code></pre>

<h3>If you're developing locally:</h3>

<pre><code>
"repositories": [
  {
    "type": "path",
    "url": "packages/Usama/firebase-notifications"
  }
]
</code></pre>

Then run:

<pre><code>composer require usamatoor/firebase-notifications:dev-main</code></pre>

<hr />

<h2 style="color:#17a2b8;">🔧 Configuration</h2>

Add the following to your <code>.env</code> file:

<pre><code>
FIREBASE_CLIENT_ID=your-client-id
FIREBASE_CLIENT_SECRET=your-client-secret
FIREBASE_REFRESH_TOKEN=your-refresh-token
FIREBASE_PROJECT_ID=your-project-id

</code></pre>

<hr />

<h2 style="color:#ffc107;">🚀 Usage</h2>

<pre><code>
use Usama\FirebaseNotifications\FirebaseNotifications;

$firebase = new FirebaseNotifications();

$firebase->send(
    $firebaseToken,
    'Welcome!',
    'Thank you for signing up.',
    ['data' => ['custom' => 'payload']]
);
</code></pre>

<hr />

<h2 style="color:#e83e8c;">📘 Documentation</h2>

- Full guide available in the <code>/docs</code> directory.
- Includes advanced usage, exception handling, and token refresh logic.

<hr />

<h2 style="color:#6f42c1;">🙌 Contributing</h2>

Pull requests are welcome! For major changes, please open an issue first.

<hr />



- [Installation](docs/installation.md)
- [Configuration](docs/configuration.md)
- [Usage](docs/usage.md)
- [Exceptions](docs/exceptions.md)
- [Advanced Features](docs/advanced.md)
- [Contributing](docs/contributing.md)


<p align="center" style="color:#20c997;"><strong>Created with ❤️ by Usama Toor</strong></p>
