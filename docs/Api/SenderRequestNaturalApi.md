# BSG\Api\V2\SenderRequestNaturalApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**senderRequestNatural()**](SenderRequestNaturalApi.md#senderRequestNatural) | **POST** /api/senders/requests/natural | Sender registration by an individual |


## `senderRequestNatural()`

```php
senderRequestNatural($sender_request_natural_request): \BSG\Api\V2\Model\SenderRequestNatural201Response
```

Sender registration by an individual

Method for submitting an application for registration of the SMS Sender’s name (Alpha-name) with a mobile operator by a subject individual.  **Please note:** that Sender registration is not available in Demo and Test account modes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SenderRequestNaturalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sender_request_natural_request = new \BSG\Api\V2\Model\SenderRequestNaturalRequest(); // \BSG\Api\V2\Model\SenderRequestNaturalRequest

try {
    $result = $apiInstance->senderRequestNatural($sender_request_natural_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderRequestNaturalApi->senderRequestNatural: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sender_request_natural_request** | [**\BSG\Api\V2\Model\SenderRequestNaturalRequest**](../Model/SenderRequestNaturalRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\SenderRequestNatural201Response**](../Model/SenderRequestNatural201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
