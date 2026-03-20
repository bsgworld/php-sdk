# BSG\Api\V2\ContactTagApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contact()**](ContactTagApi.md#contact) | **GET** /api/contacts/{id} | Get contact by ID |


## `contact()`

```php
contact($id): \BSG\Api\V2\Model\Contact200Response
```

Get contact by ID

The method allows you to receive detailed information about an existing contact, which is contained in the system, and user fields of the contact

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactTagApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 248452739; // int | Contact id

try {
    $result = $apiInstance->contact($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactTagApi->contact: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** | Contact id | |

### Return type

[**\BSG\Api\V2\Model\Contact200Response**](../Model/Contact200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
