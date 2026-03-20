# BSG\Api\V2\SmsSendApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**smsSend()**](SmsSendApi.md#smsSend) | **POST** /api/campaigns/sms/send | Send SMS campaign |


## `smsSend()`

```php
smsSend($sms_send_request): \BSG\Api\V2\Model\SmsCampaignResponse
```

Send SMS campaign

The method allows sending an SMS. The same text to list of phones will sent as single campaign

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SmsSendApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_send_request = new \BSG\Api\V2\Model\SmsSendRequest([
    'phones' => [
        0 => [
            'number' => 380661231231,
        ],
    ],
    'sender' => 'Vet klinika',
    'text' => 'test',
]);
try {
    $result = $apiInstance->smsSend($sms_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsSendApi->smsSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_send_request** | [**\BSG\Api\V2\Model\SmsSendRequest**](../Model/SmsSendRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\SmsCampaignResponse**](../Model/SmsCampaignResponse.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
