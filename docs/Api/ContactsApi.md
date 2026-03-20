# BSG\Api\V2\ContactsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contacts()**](ContactsApi.md#contacts) | **GET** /api/contacts | List of contacts |


## `contacts()`

```php
contacts($page_offset, $page_limit, $groups): \BSG\Api\V2\Model\Contacts200Response
```

List of contacts

Get a list of existing contacts in the Contact Book of your account with detailed information on each of them. The method also allows you to get contacts from the certain lists that you specified in the query parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 50; // int | The number of items in the response
$groups = [1864618]; // int[] | Index of IDs of the lists for which you want to display contacts

try {
    $result = $apiInstance->contacts($page_offset, $page_limit, $groups);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsApi->contacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 20] |
| **groups** | [**int[]**](../Model/int.md) | Index of IDs of the lists for which you want to display contacts | [optional] |

### Return type

[**\BSG\Api\V2\Model\Contacts200Response**](../Model/Contacts200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
