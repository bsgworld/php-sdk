# BSG\Api\V2\ResendOtpApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**resendOtp()**](ResendOtpApi.md#resendOtp) | **POST** /api/2fa/authentications/otp/{id}/resend | Resend the one-time code |


## `resendOtp()`

```php
resendOtp($id): \BSG\Api\V2\Model\ResendOtp200Response
```

Resend the one-time code

sed to resend the one-time password to the recipient: a new one-time password is generated and sent in the message, and the previous one becomes invalid. When resending, already saved data is used to generate the OTP from the request [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp).  *This API call is available only if the current authentication is not completed before its expiration date (the authentication validity period is specified in each TwoFA API response).*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ResendOtpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'ea5db413-e368-4952-b745-cc2030210c49'; //  string | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

try {
    $result = $apiInstance->resendOtp($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ResendOtpApi->resendOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. | |

### Return type

[**\BSG\Api\V2\Model\ResendOtp200Response**](../Model/ResendOtp200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
