# BSG\Api\V2\CampaignWhatsAppApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postCampaignsWhatsappSend()**](CampaignWhatsAppApi.md#postCampaignsWhatsappSend) | **POST** /api/campaigns/whatsapp/send | Send WhatsApp campaign |


## `postCampaignsWhatsappSend()`

```php
postCampaignsWhatsappSend($send_whats_app_campaign): \BSG\Api\V2\Model\CampaignSchema
```

Send WhatsApp campaign

This method allows you to send a whatsapp. The same message will be sent to list of phones

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignWhatsAppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$send_whats_app_campaign = new \BSG\Api\V2\Model\SendWhatsAppCampaign(); // \BSG\Api\V2\Model\SendWhatsAppCampaign

try {
    $result = $apiInstance->postCampaignsWhatsappSend($send_whats_app_campaign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignWhatsAppApi->postCampaignsWhatsappSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_whats_app_campaign** | [**\BSG\Api\V2\Model\SendWhatsAppCampaign**](../Model/SendWhatsAppCampaign.md) |  | |

### Return type

[**\BSG\Api\V2\Model\CampaignSchema**](../Model/CampaignSchema.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
