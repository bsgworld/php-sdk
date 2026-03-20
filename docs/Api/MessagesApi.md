# BSG\Api\V2\MessagesApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**sendMessage()**](MessagesApi.md#sendMessage) | **POST** /api/messages/send | Send single message |


## `sendMessage()`

```php
sendMessage($message_universal): \BSG\Api\V2\Model\MessageResponse
```

Send single message

This method allows you to send a single message of any type instantly. The message may be one of: sms, rcs, whatsapp. The message is sent without creating a campaign, provided that the client has enough funds on his/her balance. The ability to send messages via an alternative SMS channel is also supported

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\MessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_universal = new \BSG\Api\V2\Model\MessageUniversal([
    'channels' => [
        0 => 'sms',
    ],
    'phone' => [
        'number' => '380661231231',
    ],
    'sms' => [
        'sender' => 'test',
        'text' => 'Hello!',
    ],
]);
try {
    $result = $apiInstance->sendMessage($message_universal);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessagesApi->sendMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_universal** | [**\BSG\Api\V2\Model\MessageUniversal**](../Model/MessageUniversal.md) |  | |

### Return type

[**\BSG\Api\V2\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
