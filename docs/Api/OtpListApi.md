# BSG\Api\V2\OtpListApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpList()**](OtpListApi.md#otpList) | **GET** /api/2fa/authentications | List of authentication sessions |


## `otpList()`

```php
otpList($filter_from, $filter_to, $page_offset, $page_limit, $filter_ids, $filter_status, $filter_channel, $filter_recipient, $filter_country_code, $way, $sort): \BSG\Api\V2\Model\OtpList200Response
```

List of authentication sessions

Use to get a list of authentications for a period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\OtpListApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$filter_from = 'Thu Dec 01 00:00:00 UTC 2022'; // string | Period start date (date and time when the authentication session was created) in ISO 8601 format.
$filter_to = 'Sat Dec 31 00:00:00 UTC 2022'; // string | End date of the period (date and time when the authentication was created) in ISO 8601 format.
$page_offset = 0; // int
$page_limit = 10; // int
$filter_ids = 'array(\'filter_ids_example\')'; //  string[] | Authentication ID. The maximum number is 3.
$filter_status = \BSG\Api\V2\Model\OtpStatus::PENDING; // string, one of \BSG\Api\V2\Model\OtpStatus::*
$filter_channel = \BSG\Api\V2\Model\OtpChannel::SMS; // string, one of \BSG\Api\V2\Model\OtpChannel::*
$filter_recipient = 'filter_recipient_example'; // string
$filter_country_code = 'filter_country_code_example'; // string
$way = \BSG\Api\V2\Model\SortWay::ASC; // string, one of \BSG\Api\V2\Model\SortWay::*
$sort = 'id'; // string | Sort by

try {
    $result = $apiInstance->otpList($filter_from, $filter_to, $page_offset, $page_limit, $filter_ids, $filter_status, $filter_channel, $filter_recipient, $filter_country_code, $way, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OtpListApi->otpList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_from** | **\DateTime** | Period start date (date and time when the authentication session was created) in ISO 8601 format. | |
| **filter_to** | **\DateTime** | End date of the period (date and time when the authentication was created) in ISO 8601 format. | |
| **page_offset** | **int** |  | [optional] [default to 0] |
| **page_limit** | **int** |  | [optional] [default to 10] |
| **filter_ids** | [**string[]**](../Model/string.md) | Authentication ID. The maximum number is 3. | [optional] |
| **filter_status** | [**\BSG\Api\V2\Model\OtpStatus**](../Model/.md) |  | [optional] |
| **filter_channel** | [**\BSG\Api\V2\Model\OtpChannel**](../Model/.md) |  | [optional] |
| **filter_recipient** | **string** |  | [optional] |
| **filter_country_code** | **string** |  | [optional] |
| **way** | [**\BSG\Api\V2\Model\SortWay**](../Model/.md) |  | [optional] |
| **sort** | **string** | Sort by | [optional] [default to &#39;id&#39;] |

### Return type

[**\BSG\Api\V2\Model\OtpList200Response**](../Model/OtpList200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
