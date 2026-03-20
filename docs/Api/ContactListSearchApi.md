# BSG\Api\V2\ContactListSearchApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactListSearch()**](ContactListSearchApi.md#contactListSearch) | **GET** /api/groups/search | Search list |


## `contactListSearch()`

```php
contactListSearch($page_offset, $page_limit, $sort, $way, $search_field, $search_operator, $search_value, $search_fields_0_field, $search_fields_0_operator, $search_fields_0_value): \BSG\Api\V2\Model\ContactListSearch200Response
```

Search list

Method for searching the list of contacts using operations like, =, >, >=, <, <=. Search is possible by the following fields:   - name - description - date - items - phone - id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactListSearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 50; // int | The number of items in the response
$sort = 'id'; // string
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*
$search_field = \BSG\Api\V2\Model\ContactGroupSearchField::ID; // string, one of \BSG\Api\V2\Model\ContactGroupSearchField::*
$search_operator = \BSG\Api\V2\Model\SearchOperator::LIKE; // string, one of \BSG\Api\V2\Model\SearchOperator::*
$search_value = 'search_value_example'; // string
$search_fields_0_field = \BSG\Api\V2\Model\ContactGroupSearchField::ID; // string, one of \BSG\Api\V2\Model\ContactGroupSearchField::*
$search_fields_0_operator = \BSG\Api\V2\Model\SearchOperator::LIKE; // string, one of \BSG\Api\V2\Model\SearchOperator::*
$search_fields_0_value = 'search_fields_0_value_example'; // string

try {
    $result = $apiInstance->contactListSearch($page_offset, $page_limit, $sort, $way, $search_field, $search_operator, $search_value, $search_fields_0_field, $search_fields_0_operator, $search_fields_0_value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactListSearchApi->contactListSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **string** |  | [optional] [default to &#39;id&#39;] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |
| **search_field** | [**\BSG\Api\V2\Model\ContactGroupSearchField**](../Model/.md) |  | [optional] |
| **search_operator** | [**\BSG\Api\V2\Model\SearchOperator**](../Model/.md) |  | [optional] |
| **search_value** | **string** |  | [optional] |
| **search_fields_0_field** | [**\BSG\Api\V2\Model\ContactGroupSearchField**](../Model/.md) |  | [optional] |
| **search_fields_0_operator** | [**\BSG\Api\V2\Model\SearchOperator**](../Model/.md) |  | [optional] |
| **search_fields_0_value** | **string** |  | [optional] |

### Return type

[**\BSG\Api\V2\Model\ContactListSearch200Response**](../Model/ContactListSearch200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
