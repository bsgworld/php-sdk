# BSG\Api\V2\CampaignTagApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**campaign()**](CampaignTagApi.md#campaign) | **GET** /api/campaigns/{id} | Get campaign info |


## `campaign()`

```php
campaign($id): \BSG\Api\V2\Model\CampaignResponse
```

Get campaign info

Retrieve campaign with all it’s properties

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignTagApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 53651994; // int

try {
    $result = $apiInstance->campaign($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignTagApi->campaign: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** |  | |

### Return type

[**\BSG\Api\V2\Model\CampaignResponse**](../Model/CampaignResponse.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
