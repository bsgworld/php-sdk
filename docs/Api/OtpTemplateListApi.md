# BSG\Api\V2\OtpTemplateListApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpTemplateList()**](OtpTemplateListApi.md#otpTemplateList) | **GET** /api/2fa/authentications/templates | List of message templates |


## `otpTemplateList()`

```php
otpTemplateList($page_offset, $page_limit, $filter_ids, $filter_status, $sort, $way): \BSG\Api\V2\Model\OtpTemplateList200Response
```

List of message templates

This method returns a list of message templates for sending OTR code, allowing you to filter them by various parameters.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\OtpTemplateListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_offset = 0; // int
$page_limit = 10; // int
$filter_ids = array(56); // int[]
$filter_status = 'filter_status_example'; // string
$sort = 'template_id'; // string | Sorting by
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*

try {
    $result = $apiInstance->otpTemplateList($page_offset, $page_limit, $filter_ids, $filter_status, $sort, $way);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OtpTemplateListApi->otpTemplateList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** |  | [optional] [default to 10] |
| **filter_ids** | [**int[]**](../Model/int.md) |  | [optional] |
| **filter_status** | **string** |  | [optional] |
| **sort** | **string** | Sorting by | [optional] [default to &#39;template_id&#39;] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |

### Return type

[**\BSG\Api\V2\Model\OtpTemplateList200Response**](../Model/OtpTemplateList200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
