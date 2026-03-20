# BSG\Api\V2\ContactsDeleteApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactsDelete()**](ContactsDeleteApi.md#contactsDelete) | **POST** /api/contacts/delete | Delete multiple contacts |


## `contactsDelete()`

```php
contactsDelete($contact_ids, $group_ids): object
```

Delete multiple contacts

Method allow to delete multiple contacts (up to 5000) for a single request  It may be list of contact ids to delete or list of contact lists ids to delete **contacts** included into these lists.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactsDeleteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_ids = array(56); // int[] | Contact ids to delete
$group_ids = array(56); // int[] | Contact lists ids to delete **contacts** included into these lists

try {
    $result = $apiInstance->contactsDelete($contact_ids, $group_ids);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsDeleteApi->contactsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_ids** | [**int[]**](../Model/int.md) | Contact ids to delete | [optional] |
| **group_ids** | [**int[]**](../Model/int.md) | Contact lists ids to delete **contacts** included into these lists | [optional] |

### Return type

**object**

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
