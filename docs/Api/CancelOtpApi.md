# BSG\Api\V2\CancelOtpApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelOtp()**](CancelOtpApi.md#cancelOtp) | **POST** /api/2fa/authentications/{id}/cancel | Cancel the authentication session |


## `cancelOtp()`

```php
cancelOtp($id): \BSG\Api\V2\Model\CancelOtp200Response
```

Cancel the authentication session

Used to cancel the authentication process. In this case, authentication must be in the Pending status.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\CancelOtpApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'ea5db413-e368-4952-b745-cc2030210c49'; //  string | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters.

try {
    $result = $apiInstance->cancelOtp($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CancelOtpApi->cancelOtp: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string** | Authentication ID received in response to [POST /api/2fa/authentications/otp](#tag/TwoFA/operation/send_otp) The maximum length is 36 characters. | |

### Return type

[**\BSG\Api\V2\Model\CancelOtp200Response**](../Model/CancelOtp200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
