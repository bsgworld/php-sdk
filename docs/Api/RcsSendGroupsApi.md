# BSG\Api\V2\RcsSendGroupsApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**rcsSend()**](RcsSendGroupsApi.md#rcsSend) | **POST** /api/campaigns/rcs/send | Send RCS message |


## `rcsSend()`

```php
rcsSend($send_rcs_campaign): \BSG\Api\V2\Model\RcsSend200Response
```

Send RCS message

This method provides the ability to send a single rcs message or to send a mass rcs message. It also supports sending messages via an alternative SMS channel if the rcs can’t be delivered

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\RcsSendGroupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$send_rcs_campaign = new \BSG\Api\V2\Model\SendRcsCampaign([
    'phones' => [
        0 => [
            'number' => '380661231231',
        ],
    ],
    'sender' => 'rcs_sender',
    'options' => [
        'text' => 'Hello! ☺️',
    ],
]);
try {
    $result = $apiInstance->rcsSend($send_rcs_campaign);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RcsSendGroupsApi->rcsSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_rcs_campaign** | [**\BSG\Api\V2\Model\SendRcsCampaign**](../Model/SendRcsCampaign.md) |  | |

### Return type

[**\BSG\Api\V2\Model\RcsSend200Response**](../Model/RcsSend200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
