# BSG\Api\V2\CampaignsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**campaigns()**](CampaignsApi.md#campaigns) | **GET** /api/campaigns | List of campaigns |


## `campaigns()`

```php
campaigns($page_offset, $page_limit, $sort, $way, $filter_from, $filter_to, $filter_type, $search_field, $search_value): \BSG\Api\V2\Model\SearchCampaignResource
```

List of campaigns

Get a list of campaigns based on specified criteria

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 50; // int | The number of items in the response
$sort = 'id'; // string | Sort items by
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*
$filter_from = 'new \\DateTime(\'2013-10-20T19:20:30+01:00\')'; // string | Include items from
$filter_to = 'new \\DateTime(\'2013-10-20T19:20:30+01:00\')'; // string | Include items to
$filter_type = 'filter_type_example'; // string | Filter items by type type
$search_field = 'search_field_example'; // string | Filter items by search[field]=search[value]
$search_value = 'search_value_example'; // string | Filter items by search[field]=search[value]

try {
    $result = $apiInstance->campaigns($page_offset, $page_limit, $sort, $way, $filter_from, $filter_to, $filter_type, $search_field, $search_value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignsApi->campaigns: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** | The number of items in the response | [optional] [default to 50] |
| **sort** | **string** | Sort items by | [optional] [default to &#39;id&#39;] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |
| **filter_from** | **\DateTime** | Include items from | [optional] |
| **filter_to** | **\DateTime** | Include items to | [optional] |
| **filter_type** | **string** | Filter items by type type | [optional] |
| **search_field** | **string** | Filter items by search[field]&#x3D;search[value] | [optional] |
| **search_value** | **string** | Filter items by search[field]&#x3D;search[value] | [optional] |

### Return type

[**\BSG\Api\V2\Model\SearchCampaignResource**](../Model/SearchCampaignResource.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
