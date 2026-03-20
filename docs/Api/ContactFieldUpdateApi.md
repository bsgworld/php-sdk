# BSG\Api\V2\ContactFieldUpdateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactFieldUpdate()**](ContactFieldUpdateApi.md#contactFieldUpdate) | **PATCH** /api/contacts/fields/{id} | Update contact field |


## `contactFieldUpdate()`

```php
contactFieldUpdate($id, $contact_field_update_request): \BSG\Api\V2\Model\ContactFieldUpdate200Response
```

Update contact field

Method for editing custom contact field:  - change field name - change field description

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactFieldUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Contact field id
$contact_field_update_request = new \BSG\Api\V2\Model\ContactFieldUpdateRequest(); // \BSG\Api\V2\Model\ContactFieldUpdateRequest

try {
    $result = $apiInstance->contactFieldUpdate($id, $contact_field_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactFieldUpdateApi->contactFieldUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** | Contact field id | |
| **contact_field_update_request** | [**\BSG\Api\V2\Model\ContactFieldUpdateRequest**](../Model/ContactFieldUpdateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactFieldUpdate200Response**](../Model/ContactFieldUpdate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
