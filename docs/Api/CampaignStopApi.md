# BSG\Api\V2\CampaignStopApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**campaignStop()**](CampaignStopApi.md#campaignStop) | **PATCH** /api/campaigns/{id}/stop | Cancel campaign |


## `campaignStop()`

```php
campaignStop($id): \BSG\Api\V2\Model\CampaignStop200Response
```

Cancel campaign

Abort the campaign and move it to finally status stopped

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignStopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int

try {
    $result = $apiInstance->campaignStop($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignStopApi->campaignStop: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** |  | |

### Return type

[**\BSG\Api\V2\Model\CampaignStop200Response**](../Model/CampaignStop200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
