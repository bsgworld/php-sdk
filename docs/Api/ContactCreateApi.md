# BSG\Api\V2\ContactCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactCreate()**](ContactCreateApi.md#contactCreate) | **POST** /api/contacts | Create a contact |


## `contactCreate()`

```php
contactCreate($store_contact): \BSG\Api\V2\Model\ContactCreate201Response
```

Create a contact

The method allows adding new contacts to your Contact Book.   **Please note:** that in the TEST account mode there is a restriction for performing this method: it is possible to create a contact only for a verified phone number (number verification is performed in the personal account of the platform).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$store_contact = new \BSG\Api\V2\Model\StoreContact([
    'phone' => 61401629754,
]);
try {
    $result = $apiInstance->contactCreate($store_contact);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactCreateApi->contactCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **store_contact** | [**\BSG\Api\V2\Model\StoreContact**](../Model/StoreContact.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactCreate201Response**](../Model/ContactCreate201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
