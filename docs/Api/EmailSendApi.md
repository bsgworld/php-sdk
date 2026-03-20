# BSG\Api\V2\EmailSendApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**emailSend()**](EmailSendApi.md#emailSend) | **POST** /api/email/send-emails | Send Email |


## `emailSend()`

```php
emailSend($send_email): \BSG\Api\V2\Model\EmailResponse
```

Send Email

Method is designed for sending single email with optional parameters.    This request allows you to send emails with both text and HTML content, and optionally include inline media, such as images or other files, which are embedded directly in the email body for a richer user experience

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\EmailSendApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$send_email = new \BSG\Api\V2\Model\SendEmail([
    'to' => [
        0 => 'user@test.com',
    ],
    'from' => 'Test.email 11_22 <user@test1.email.bsg.world>',
    'subject' => 'test1',
    'htmlbody' => '<html lang="en"><head><title>link to Symbl.cc</title></head><body><h1>Visit site</h1>Visit site <a href="https://symbl.cc">Symbl.cc</a> for additional information.</body></html>',
]);
try {
    $result = $apiInstance->emailSend($send_email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailSendApi->emailSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_email** | [**\BSG\Api\V2\Model\SendEmail**](../Model/SendEmail.md) |  | |

### Return type

[**\BSG\Api\V2\Model\EmailResponse**](../Model/EmailResponse.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
