# BSG\Api\V2\SendOtpApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**sendOtp()**](SendOtpApi.md#sendOtp) | **POST** /api/2fa/authentications/otp | Send One-time password |


## `sendOtp()`

```php
sendOtp($send_otp_request): \BSG\Api\V2\Model\SendOtp201Response
```

Send One-time password

This API call is used to generate and send a one-time password to a user in an SMS or Viber message. **Please note:** authentication of recipients who are in the SMS or Viber stop list in your contact book is not possible using the corresponding method. (That is, if the recipient is in the SMS stop list, then when requesting authentication using the SMS method, the one-time password will not be sent, and you will receive an error in response).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\SendOtpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$send_otp_request = new \BSG\Api\V2\Model\SendOtpRequest([
    'recipient' => '61401629754',
    'channel' => 'sms',
    'sender' => 'SENDER',
    'template_id' => '12',
    'code_lifetime' => 300,
    'code_max_tries' => 3,
    'code_digits' => 5,
]);
try {
    $result = $apiInstance->sendOtp($send_otp_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SendOtpApi->sendOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_otp_request** | [**\BSG\Api\V2\Model\SendOtpRequest**](../Model/SendOtpRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\SendOtp201Response**](../Model/SendOtp201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
