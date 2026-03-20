# BSG\Api\V2\StoplistAddApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**stoplistAdd()**](StoplistAddApi.md#stoplistAdd) | **POST** /api/stoplist/attach | Add contacts to stop list |


## `stoplistAdd()`

```php
stoplistAdd($stoplist_add_request): \BSG\Api\V2\Model\StoplistAdd200Response
```

Add contacts to stop list

Performs adding one or more contacts to the stop list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StoplistAddApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stoplist_add_request = new \BSG\Api\V2\Model\StoplistAddRequest(); // \BSG\Api\V2\Model\StoplistAddRequest

try {
    $result = $apiInstance->stoplistAdd($stoplist_add_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoplistAddApi->stoplistAdd: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stoplist_add_request** | [**\BSG\Api\V2\Model\StoplistAddRequest**](../Model/StoplistAddRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\StoplistAdd200Response**](../Model/StoplistAdd200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
