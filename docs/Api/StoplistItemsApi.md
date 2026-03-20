# BSG\Api\V2\StoplistItemsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**stoplistItems()**](StoplistItemsApi.md#stoplistItems) | **GET** /api/stoplist | List the contacts of stop lists |


## `stoplistItems()`

```php
stoplistItems($page_offset, $page_limit, $type): \BSG\Api\V2\Model\StoplistItems200Response
```

List the contacts of stop lists

The method allows getting a list of contacts that were added to the SMS and/or Viber stop list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StoplistItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 50; // int | The number of items in the response
$type = 'type_example'; // string | Specify the type of the stop list for which we need to return the contact list. If the stop list type is not specified, the method will return data for all the stop list types

try {
    $result = $apiInstance->stoplistItems($page_offset, $page_limit, $type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StoplistItemsApi->stoplistItems: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 20] |
| **type** | **string** | Specify the type of the stop list for which we need to return the contact list. If the stop list type is not specified, the method will return data for all the stop list types | [optional] |

### Return type

[**\BSG\Api\V2\Model\StoplistItems200Response**](../Model/StoplistItems200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
