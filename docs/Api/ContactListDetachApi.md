# BSG\Api\V2\ContactListDetachApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactListDetach()**](ContactListDetachApi.md#contactListDetach) | **POST** /api/groups/detach | Remove contacts from the list |


## `contactListDetach()`

```php
contactListDetach($contact_list_detach_request): object
```

Remove contacts from the list

Performs the removal of contact from the list. The action can be single (string) or bulk (array)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactListDetachApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_list_detach_request = new \BSG\Api\V2\Model\ContactListDetachRequest([
    'contacts' => [
        0 => 248452959,
        1 => 248452739,
        2 => 248452740,
    ],
    'groups' => [
        0 => 1864623,
        1 => 1864621,
    ],
]);
try {
    $result = $apiInstance->contactListDetach($contact_list_detach_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactListDetachApi->contactListDetach: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_list_detach_request** | [**\BSG\Api\V2\Model\ContactListDetachRequest**](../Model/ContactListDetachRequest.md) |  | |

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
