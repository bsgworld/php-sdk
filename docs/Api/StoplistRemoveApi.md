# BSG\Api\V2\StoplistRemoveApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**stoplistRemove()**](StoplistRemoveApi.md#stoplistRemove) | **POST** /api/stoplist/detach | Remove contacts from stop list |


## `stoplistRemove()`

```php
stoplistRemove($stoplist_remove_request): object
```

Remove contacts from stop list

Performs the removal of one or more contacts from the stop list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StoplistRemoveApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stoplist_remove_request = new \BSG\Api\V2\Model\StoplistRemoveRequest(); // \BSG\Api\V2\Model\StoplistRemoveRequest

try {
    $result = $apiInstance->stoplistRemove($stoplist_remove_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoplistRemoveApi->stoplistRemove: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stoplist_remove_request** | [**\BSG\Api\V2\Model\StoplistRemoveRequest**](../Model/StoplistRemoveRequest.md) |  | |

### Return type

**object**

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
