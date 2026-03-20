# BSG\Api\V2\ContactFieldCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactFieldCreate()**](ContactFieldCreateApi.md#contactFieldCreate) | **POST** /api/contacts/fields | Create contact field |


## `contactFieldCreate()`

```php
contactFieldCreate($contact_field_create_request): \BSG\Api\V2\Model\ContactFieldCreate201Response
```

Create contact field

The method allows the creation of additional custom fields for contacts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactFieldCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_field_create_request = new \BSG\Api\V2\Model\ContactFieldCreateRequest(); // \BSG\Api\V2\Model\ContactFieldCreateRequest

try {
    $result = $apiInstance->contactFieldCreate($contact_field_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactFieldCreateApi->contactFieldCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_field_create_request** | [**\BSG\Api\V2\Model\ContactFieldCreateRequest**](../Model/ContactFieldCreateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactFieldCreate201Response**](../Model/ContactFieldCreate201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
