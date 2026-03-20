# BSG\Api\V2\CampaignPriceApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**campaignPrice()**](CampaignPriceApi.md#campaignPrice) | **POST** /api/campaigns/price | Calculate campaign price |


## `campaignPrice()`

```php
campaignPrice($campaign_price_request): \BSG\Api\V2\Model\CampaignPrice200Response
```

Calculate campaign price

Calculate campaign estimated price before actually [send it](#operation/sms_send)  **Please note:** Method suitable only for SMS campaigns

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$campaign_price_request = new \BSG\Api\V2\Model\CampaignPriceRequest([
    'sender' => 'Vet klinika',
    'text' => 'hello!',
    'messages' => [
        0 => [
            'phone' => 38267161234,
        ],
    ],
]);
try {
    $result = $apiInstance->campaignPrice($campaign_price_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignPriceApi->campaignPrice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **campaign_price_request** | [**\BSG\Api\V2\Model\CampaignPriceRequest**](../Model/CampaignPriceRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\CampaignPrice200Response**](../Model/CampaignPrice200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
