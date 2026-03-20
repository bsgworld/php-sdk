# BSG\Api\V2\CampaignDetailsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**campaignDetails()**](CampaignDetailsApi.md#campaignDetails) | **GET** /api/campaigns/{id}/detail | Get campaign details |


## `campaignDetails()`

```php
campaignDetails($id): \BSG\Api\V2\Model\CampaignDetails200Response
```

Get campaign details

Campaign detail information and delivery statistics

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignDetailsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 53651994; // int

try {
    $result = $apiInstance->campaignDetails($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignDetailsApi->campaignDetails: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** |  | |

### Return type

[**\BSG\Api\V2\Model\CampaignDetails200Response**](../Model/CampaignDetails200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
