# BSG\Api\V2\RcsSingleApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**rcsSingle()**](RcsSingleApi.md#rcsSingle) | **POST** /api/messages/rcs/send | Send single RCS message |


## `rcsSingle()`

```php
rcsSingle($rcs_message): \BSG\Api\V2\Model\MessageResponse
```

Send single RCS message

This method allows you to send a single rcs message instantly. The message is sent without creating a campaign, provided that the client has enough funds on his/her balance. The ability to send messages via an alternative SMS channel is also supported

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\RcsSingleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rcs_message = new \BSG\Api\V2\Model\RcsMessage([
    'phone' => [
        'number' => '380661231231',
    ],
    'sender' => 'rcs_sender',
    'options' => [
        'text' => 'Hello! ☺️',
    ],
]);
try {
    $result = $apiInstance->rcsSingle($rcs_message);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RcsSingleApi->rcsSingle: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rcs_message** | [**\BSG\Api\V2\Model\RcsMessage**](../Model/RcsMessage.md) |  | |

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
