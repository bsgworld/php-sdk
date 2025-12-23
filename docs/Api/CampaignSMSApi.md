# BSG\Api\V2\CampaignSMSApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**smsSend()**](CampaignSMSApi.md#smsSend) | **POST** /api/campaigns/sms/send | Send SMS campaign |
| [**smsSendGroups()**](CampaignSMSApi.md#smsSendGroups) | **POST** /api/campaigns/sms/send-groups | Send SMS to contact list |
| [**smsSendIndividual()**](CampaignSMSApi.md#smsSendIndividual) | **POST** /api/campaigns/sms/send-individual | Send SMS with different text |


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


$apiInstance = new BSG\Api\V2\Api\CampaignSMSApi(
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
    echo 'Exception when calling CampaignSMSApi->smsSend: ', $e->getMessage(), PHP_EOL;
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

## `smsSendGroups()`

```php
smsSendGroups($sms_send_groups_request): \BSG\Api\V2\Model\SmsCampaignResponse
```

Send SMS to contact list

The method allows sending an SMS to the contacts list from the Contact Book. The campaign can contain personalized data from the contact fields in the text of the message for each contact.   It is possible to specify no more than 10 000 contacts for one campaign.  **Limitation:**   - In the DEMO account mode, creating a campaign via API is not available. - In the TEST platform mode, creating a campaign is possible only for the verified numbers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CampaignSMSApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_send_groups_request = new \BSG\Api\V2\Model\SmsSendGroupsRequest([
    'groups' => [
        0 => 1864275,
    ],
    'text' => 'hello!',
    'sender' => 'Vet klinika',
]);
try {
    $result = $apiInstance->smsSendGroups($sms_send_groups_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CampaignSMSApi->smsSendGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sms_send_groups_request** | [**\BSG\Api\V2\Model\SmsSendGroupsRequest**](../Model/SmsSendGroupsRequest.md) |  | |

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


$apiInstance = new BSG\Api\V2\Api\CampaignSMSApi(
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
    echo 'Exception when calling CampaignSMSApi->smsSendIndividual: ', $e->getMessage(), PHP_EOL;
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
