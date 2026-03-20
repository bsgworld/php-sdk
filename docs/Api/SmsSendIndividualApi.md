# BSG\Api\V2\SmsSendIndividualApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**smsSendIndividual()**](SmsSendIndividualApi.md#smsSendIndividual) | **POST** /api/campaigns/sms/send-individual | Send SMS with different text |


## `smsSendIndividual()`

```php
smsSendIndividual($sms_send_individual_request): \BSG\Api\V2\Model\SmsCampaignResponse
```

Send SMS with different text

Send SMS with different text to list of phones

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SmsSendIndividualApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_send_individual_request = new \BSG\Api\V2\Model\SmsSendIndividualRequest([
    'messages' => [
        0 => [
            'phone' => 380661231231,
            'text' => 'hello Jack',
            'sender' => 'Vet klinika',
        ],
        1 => [
            'phone' => 380661231232,
            'text' => 'hello Anna',
            'sender' => 'Vet klinika',
        ],
        2 => [
            'phone' => 380661231233,
            'text' => 'Hi Hellen',
            'sender' => 'Vet klinika',
        ],
    ],
]);
try {
    $result = $apiInstance->smsSendIndividual($sms_send_individual_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsSendIndividualApi->smsSendIndividual: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_send_individual_request** | [**\BSG\Api\V2\Model\SmsSendIndividualRequest**](../Model/SmsSendIndividualRequest.md) |  | |

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
