# BSG\Api\V2\CampaignViberApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**viberSend()**](CampaignViberApi.md#viberSend) | **POST** /api/campaigns/viber/send | Send Viber campaign |


## `viberSend()`

```php
viberSend($send_viber_campaign): \BSG\Api\V2\Model\ViberCampaignResponse
```

Send Viber campaign

This method provides the ability to send a viber campaign.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignViberApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$send_viber_campaign = new \BSG\Api\V2\Model\SendViberCampaign([
    'phones' => [
        0 => [
            'number' => '380971123456',
        ],
    ],
    'text' => 'some viber text',
    'sender' => 'Notify',
]);
try {
    $result = $apiInstance->viberSend($send_viber_campaign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignViberApi->viberSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_viber_campaign** | [**\BSG\Api\V2\Model\SendViberCampaign**](../Model/SendViberCampaign.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ViberCampaignResponse**](../Model/ViberCampaignResponse.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
