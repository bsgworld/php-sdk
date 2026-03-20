# BSG\Api\V2\ContactListUpdateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactListUpdate()**](ContactListUpdateApi.md#contactListUpdate) | **PUT** /api/groups/{id} | Update list |


## `contactListUpdate()`

```php
contactListUpdate($id, $contact_list_update_request): \BSG\Api\V2\Model\ContactListUpdate200Response
```

Update list

Performs editing of the selected contacts list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactListUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int
$contact_list_update_request = new \BSG\Api\V2\Model\ContactListUpdateRequest(); // \BSG\Api\V2\Model\ContactListUpdateRequest

try {
    $result = $apiInstance->contactListUpdate($id, $contact_list_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactListUpdateApi->contactListUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** |  | |
| **contact_list_update_request** | [**\BSG\Api\V2\Model\ContactListUpdateRequest**](../Model/ContactListUpdateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactListUpdate200Response**](../Model/ContactListUpdate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
