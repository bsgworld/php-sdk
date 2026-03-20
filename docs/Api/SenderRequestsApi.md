# BSG\Api\V2\SenderRequestsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**senderRequests()**](SenderRequestsApi.md#senderRequests) | **GET** /api/senders/requests/sms | List of Sender Requests |


## `senderRequests()`

```php
senderRequests($page_limit, $page_offset, $sort, $way, $filter_status, $filter_id, $filter_country_code, $filter_sender, $filter_created_at): \BSG\Api\V2\Model\SenderRequests200Response
```

List of Sender Requests

Get SMS Senders request status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SenderRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_limit = 50; // int
$page_offset = 0; // int
$sort = 'id'; // string
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*
$filter_status = \BSG\Api\V2\Model\SenderRequestStatus::_NEW; // string, one of \BSG\Api\V2\Model\SenderRequestStatus::*
$filter_id = 56; // int
$filter_country_code = 'filter_country_code_example'; // string
$filter_sender = 'filter_sender_example'; // string
$filter_created_at = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime

try {
    $result = $apiInstance->senderRequests($page_limit, $page_offset, $sort, $way, $filter_status, $filter_id, $filter_country_code, $filter_sender, $filter_created_at);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderRequestsApi->senderRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_limit** | **int** |  | [optional] [default to 50] |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **sort** | **string** |  | [optional] [default to &#39;id&#39;] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |
| **filter_status** | [**\BSG\Api\V2\Model\SenderRequestStatus**](../Model/.md) |  | [optional] |
| **filter_id** | **int** |  | [optional] |
| **filter_country_code** | **string** |  | [optional] |
| **filter_sender** | **string** |  | [optional] |
| **filter_created_at** | **\DateTime** |  | [optional] |

### Return type

[**\BSG\Api\V2\Model\SenderRequests200Response**](../Model/SenderRequests200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
