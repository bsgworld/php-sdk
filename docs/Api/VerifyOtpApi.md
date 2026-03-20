# BSG\Api\V2\VerifyOtpApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**verifyOtp()**](VerifyOtpApi.md#verifyOtp) | **POST** /api/2fa/authentications/otp/{id}/verify | Check one-time Code |


## `verifyOtp()`

```php
verifyOtp($id, $verify_otp_request): \BSG\Api\V2\Model\VerifyOtp200Response
```

Check one-time Code

The API call is used to verify that the one-time password you received from the user matches the one sent by BSG

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\VerifyOtpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'ea5db413-e368-4952-b745-cc2030210c49'; //  string | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.
$verify_otp_request = new \BSG\Api\V2\Model\VerifyOtpRequest(); // \BSG\Api\V2\Model\VerifyOtpRequest

try {
    $result = $apiInstance->verifyOtp($id, $verify_otp_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VerifyOtpApi->verifyOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. | |
| **verify_otp_request** | [**\BSG\Api\V2\Model\VerifyOtpRequest**](../Model/VerifyOtpRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\VerifyOtp200Response**](../Model/VerifyOtp200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
