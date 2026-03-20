# BSG\Api\V2\PostContactsFieldsDeleteApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postContactsFieldsDelete()**](PostContactsFieldsDeleteApi.md#postContactsFieldsDelete) | **POST** /api/contacts/fields/delete | Delete contact fields by ids |


## `postContactsFieldsDelete()`

```php
postContactsFieldsDelete($post_contacts_fields_delete_request): object
```

Delete contact fields by ids

Delete multiple (up to 30) contact fields

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\PostContactsFieldsDeleteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$post_contacts_fields_delete_request = new \BSG\Api\V2\Model\PostContactsFieldsDeleteRequest(); // \BSG\Api\V2\Model\PostContactsFieldsDeleteRequest

try {
    $result = $apiInstance->postContactsFieldsDelete($post_contacts_fields_delete_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PostContactsFieldsDeleteApi->postContactsFieldsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **post_contacts_fields_delete_request** | [**\BSG\Api\V2\Model\PostContactsFieldsDeleteRequest**](../Model/PostContactsFieldsDeleteRequest.md) |  | |

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
