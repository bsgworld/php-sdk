# BSG\Api\V2\ContactListCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactListCreate()**](ContactListCreateApi.md#contactListCreate) | **POST** /api/groups | Create list |


## `contactListCreate()`

```php
contactListCreate($contact_list_create_request): \BSG\Api\V2\Model\ContactListCreate201Response
```

Create list

Create a contact list to group contacts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactListCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_list_create_request = new \BSG\Api\V2\Model\ContactListCreateRequest([
    'name' => 'new list 123',
]);
try {
    $result = $apiInstance->contactListCreate($contact_list_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactListCreateApi->contactListCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_list_create_request** | [**\BSG\Api\V2\Model\ContactListCreateRequest**](../Model/ContactListCreateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactListCreate201Response**](../Model/ContactListCreate201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
