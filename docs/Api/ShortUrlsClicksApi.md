# BSG\Api\V2\ShortUrlsClicksApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsClicks()**](ShortUrlsClicksApi.md#shortUrlsClicks) | **GET** /api/short-url/clicks | List of clicks |


## `shortUrlsClicks()`

```php
shortUrlsClicks($from, $to, $page, $per_page, $campaign): \BSG\Api\V2\Model\ShortUrlsClicks200Response
```

List of clicks

List of all clicks for selected period *from* - *to* with pagination by *per_page*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsClicksApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$from = '2022-04-28'; //  string | From date
$to = '2022-04-28'; //  string | To date
$page = 1; // int | Get items starting from this page.
$per_page = 20; // int | The number of items in the page. Possible values are from 10 to 500.
$campaign = 56; // int | Campaign id to get only clicks on short link sent as part on [sms campaign](#tag/Campaign-SMS)

try {
    $result = $apiInstance->shortUrlsClicks($from, $to, $page, $per_page, $campaign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsClicksApi->shortUrlsClicks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **from** | **string** | From date | |
| **to** | **string** | To date | |
| **page** | **int** | Get items starting from this page. | [optional] [default to 1] |
| **per_page** | **int** | The number of items in the page. Possible values are from 10 to 500. | [optional] [default to 20] |
| **campaign** | **int** | Campaign id to get only clicks on short link sent as part on [sms campaign](#tag/Campaign-SMS) | [optional] |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsClicks200Response**](../Model/ShortUrlsClicks200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
