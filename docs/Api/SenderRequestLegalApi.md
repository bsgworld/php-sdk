# BSG\Api\V2\SenderRequestLegalApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**senderRequestLegal()**](SenderRequestLegalApi.md#senderRequestLegal) | **POST** /api/senders/requests/legal | Sender registration by a legal entity |


## `senderRequestLegal()`

```php
senderRequestLegal($sender_request_legal_request): \BSG\Api\V2\Model\SenderRequestLegal201Response
```

Sender registration by a legal entity

Method for submitting an application for registration of the SMS Sender’s name (Alpha-name) with a mobile operator by a subject legal entity.  **Please note:** that Sender registration is not available in Demo and Test account modes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SenderRequestLegalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sender_request_legal_request = new \BSG\Api\V2\Model\SenderRequestLegalRequest(); // \BSG\Api\V2\Model\SenderRequestLegalRequest

try {
    $result = $apiInstance->senderRequestLegal($sender_request_legal_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderRequestLegalApi->senderRequestLegal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sender_request_legal_request** | [**\BSG\Api\V2\Model\SenderRequestLegalRequest**](../Model/SenderRequestLegalRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\SenderRequestLegal201Response**](../Model/SenderRequestLegal201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
