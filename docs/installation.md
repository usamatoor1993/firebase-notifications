# Installation

Install via Composer:

```
composer require usamatoor/firebase-notifications
```


# 🔥 Firebase Notifications for Laravel

A lightweight Laravel package to send Firebase Cloud Messaging (FCM) notifications using OAuth2 — with no Firebase Admin SDK required.

> ⚡ Built for Laravel 10/11/12+ — Ideal for secure token-based FCM delivery in PHP.

---

## 📦 Installation

Install the package via [Packagist](https://packagist.org/packages/usamatoor/firebase-notifications):

```bash
composer require usamatoor/firebase-notifications


If you're developing locally:

```json
"repositories": [
  {
    "type": "path",
    "url": "packages/Usamatoor/firebase-notifications"
  }
]

```

Then run:

```
composer require usamatoor/firebase-notifications:dev-main


```
Configuration:
```php artisan vendor:publish --tag=firebase-notifications-config```

This will create config/firebase-notifications.php


Now, update your .env:

``` 
FIREBASE_CLIENT_ID=your-client-id
FIREBASE_CLIENT_SECRET=your-client-secret
FIREBASE_REFRESH_TOKEN=your-refresh-token
FIREBASE_PROJECT_ID=your-firebase-project-id
FIREBASE_NOTIFICATIONS_ENDPOINT=https://fcm.googleapis.com/v1/projects/:project_id/messages:send 
```


# 🔐 Firebase Notifications - OAuth2 Setup Guide

This guide explains how to configure Firebase Cloud Messaging (FCM) to work with the `usama/firebase-notifications` Laravel package using OAuth2.

---

## ⚙️ Required Credentials

You’ll need the following:

- `client_id`
- `client_secret`
- `refresh_token`
- `project_id`

---

## 1. Enable Firebase Cloud Messaging API

1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create or select an existing project.
3. Navigate to **APIs & Services > Library**.
4. Search for **"Firebase Cloud Messaging API"** and click **Enable**.

---

## 2. Create OAuth 2.0 Credentials

1. Go to **APIs & Services > Credentials**.
2. Click **Create Credentials > OAuth client ID**.
3. Choose **Web application**.
4. Enter any name (e.g., `Laravel FCM`), and leave redirect URIs empty.
5. Click **Create**.
6. Copy the `client_id` and `client_secret`.

---

## 3. Get `refresh_token` from OAuth2 Playground

1. Go to [OAuth 2.0 Playground](https://developers.google.com/oauthplayground).
2. Click the ⚙️ **gear icon (Settings)**.
3. Enable: **Use your own OAuth credentials** and enter your `client_id` and `client_secret`.
4. In **Step 1**, enter this scope:
https://www.googleapis.com/auth/firebase.messaging

5. Click **Authorize APIs** and sign in.
6. Click **Exchange authorization code for tokens**.
7. Copy the `refresh_token`.

---

