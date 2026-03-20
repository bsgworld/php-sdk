# BSG\Api\V2\ContactsSearchApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactsSearch()**](ContactsSearchApi.md#contactsSearch) | **GET** /api/contacts/search | Search contacts |


## `contactsSearch()`

```php
contactsSearch($page_offset, $page_limit, $sort, $way, $search_field, $search_operator, $search_value, $search_fields_0_field, $search_fields_0_operator, $search_fields_0_value): \BSG\Api\V2\Model\ContactsSearch200Response
```

Search contacts

Method for searching contacts in the Contact Book. In the search, it is possible to use operations: like, =, >, >=, <, <=.  Search is possible by the following fields:   - id:  =, >, >=, <, <= - phone: like, = - {field_id}:   - for field with \"Text\" type: like, =   - for field with \"Number\" type:  =, >, >=, <, <=   - for field with \"Date\" type: =, >, >=, <, <=  It’s possible to pass multiple criteria by pass `search_fields` array instead of `search`

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactsSearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 50; // int | The number of items in the response
$sort = 'id'; // string | Sort by conditions: id, phone
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*
$search_field = 'search_field_example'; // string
$search_operator = \BSG\Api\V2\Model\SearchOperator::LIKE; // string, one of \BSG\Api\V2\Model\SearchOperator::*
$search_value = 'search_value_example'; // string
$search_fields_0_field = 'search_fields_0_field_example'; // string
$search_fields_0_operator = \BSG\Api\V2\Model\SearchOperator::LIKE; // string, one of \BSG\Api\V2\Model\SearchOperator::*
$search_fields_0_value = 'search_fields_0_value_example'; // string

try {
    $result = $apiInstance->contactsSearch($page_offset, $page_limit, $sort, $way, $search_field, $search_operator, $search_value, $search_fields_0_field, $search_fields_0_operator, $search_fields_0_value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactsSearchApi->contactsSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **string** | Sort by conditions: id, phone | [optional] [default to &#39;id&#39;] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |
| **search_field** | **string** |  | [optional] |
| **search_operator** | [**\BSG\Api\V2\Model\SearchOperator**](../Model/.md) |  | [optional] |
| **search_value** | **string** |  | [optional] |
| **search_fields_0_field** | **string** |  | [optional] |
| **search_fields_0_operator** | [**\BSG\Api\V2\Model\SearchOperator**](../Model/.md) |  | [optional] |
| **search_fields_0_value** | **string** |  | [optional] |

### Return type

[**\BSG\Api\V2\Model\ContactsSearch200Response**](../Model/ContactsSearch200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
