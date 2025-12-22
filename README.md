# BSG PHP SDK (V2 - One-API)

Official PHP SDK for BSG One-API - unified messaging platform for SMS, Viber, RCS, WhatsApp, and more.

## Installation

```bash
composer require bsg/php-sdk
```

## Requirements

- PHP 7.4 or later
- Guzzle HTTP client

## Quick Start

```php
<?php
require_once __DIR__ . '/vendor/autoload.php';

use BSG\Api\V2\Configuration;
use BSG\Api\V2\Api\BalanceApi;

// Configure API with JWT token
$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_JWT_TOKEN');

// Create API instance
$balanceApi = new BalanceApi(new GuzzleHttp\Client(), $config);

// Get account balance
try {
    $result = $balanceApi->accountBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ' . $e->getMessage();
}
```

## Authentication

One-API uses JWT (Bearer) authentication. First, obtain a token:

```php
use BSG\Api\V2\Api\AuthApi;
use BSG\Api\V2\Model\Loginrequest;

$authApi = new AuthApi(new GuzzleHttp\Client());
$loginRequest = new Loginrequest([
    'email' => 'your@email.com',
    'password' => 'your-password'
]);

$token = $authApi->login($loginRequest);
$jwtToken = $token->getData()->getToken();

// Use the token for subsequent requests
$config = Configuration::getDefaultConfiguration()
    ->setAccessToken($jwtToken);
```

## Available APIs

| API | Description |
|-----|-------------|
| `AuthApi` | Authentication (login, refresh token) |
| `BalanceApi` | Account balance and tariffs |
| `CampaignSMSApi` | Send SMS campaigns |
| `CampaignRCSApi` | Send RCS messages |
| `CampaignWhatsAppApi` | Send WhatsApp messages |
| `Class2FAOTPApi` | Two-factor authentication / OTP |
| `ContactApi` | Manage contacts |
| `ContactListApi` | Manage contact lists |
| `SendersApi` | Manage sender IDs |
| `ShortLinksApi` | URL shortening |
| `StopListApi` | Manage stop lists |

## Examples

### Send SMS Campaign

```php
use BSG\Api\V2\Api\CampaignSMSApi;

$smsApi = new CampaignSMSApi(new GuzzleHttp\Client(), $config);
$result = $smsApi->smsSend([
    'sender' => 'YourSender',
    'text' => 'Hello from BSG One-API!',
    'phones' => [
        ['number' => '380501234567']
    ]
]);
```

### Send WhatsApp Message

```php
use BSG\Api\V2\Api\CampaignWhatsAppApi;

$whatsappApi = new CampaignWhatsAppApi(new GuzzleHttp\Client(), $config);
$result = $whatsappApi->whatsappSingle([
    'phone' => '380501234567',
    'template' => [
        'name' => 'your_template',
        'language' => 'en'
    ]
]);
```

### Send OTP (2FA)

```php
use BSG\Api\V2\Api\Class2FAOTPApi;

$otpApi = new Class2FAOTPApi(new GuzzleHttp\Client(), $config);

// Send OTP
$result = $otpApi->sendOtp([
    'phone' => '380501234567',
    'template_id' => 123
]);

// Verify OTP
$verification = $otpApi->verifyOtp($authId, [
    'code' => '123456'
]);
```

### Get Tariffs

```php
use BSG\Api\V2\Api\BalanceApi;

$balanceApi = new BalanceApi(new GuzzleHttp\Client(), $config);
$tariffs = $balanceApi->accountTariffs();
```

## API Documentation

- [Auth API](docs/Api/AuthApi.md)
- [Balance API](docs/Api/BalanceApi.md)
- [Campaign SMS API](docs/Api/CampaignSMSApi.md)
- [Campaign RCS API](docs/Api/CampaignRCSApi.md)
- [Campaign WhatsApp API](docs/Api/CampaignWhatsAppApi.md)
- [2FA OTP API](docs/Api/Class2FAOTPApi.md)
- [Contacts API](docs/Api/ContactApi.md)

## Configuration

### API Host

Default: `https://one-api.bsg.world`

```php
$config = Configuration::getDefaultConfiguration()
    ->setHost('https://one-api.bsg.world')
    ->setAccessToken('YOUR_JWT_TOKEN');
```

### Timeout

```php
$client = new GuzzleHttp\Client([
    'timeout' => 30,
    'connect_timeout' => 10
]);
$smsApi = new CampaignSMSApi($client, $config);
```

## Support

- Website: [bsg.world](https://bsg.world)
- Email: support@bsg.world
- Documentation: [bsg.world/developers](https://bsg.world/developers)

## License

MIT