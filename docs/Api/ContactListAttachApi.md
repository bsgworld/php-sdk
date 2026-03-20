# BSG\Api\V2\ContactListAttachApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactListAttach()**](ContactListAttachApi.md#contactListAttach) | **POST** /api/groups/attach | Add contacts to the list |


## `contactListAttach()`

```php
contactListAttach($contact_list_attach_request): object
```

Add contacts to the list

The method provides the ability to add an existing contact to the list. The action can be single or bulk.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactListAttachApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_list_attach_request = new \BSG\Api\V2\Model\ContactListAttachRequest([
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
    $result = $apiInstance->contactListAttach($contact_list_attach_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactListAttachApi->contactListAttach: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_list_attach_request** | [**\BSG\Api\V2\Model\ContactListAttachRequest**](../Model/ContactListAttachRequest.md) |  | |

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
