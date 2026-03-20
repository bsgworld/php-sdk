# BSG\Api\V2\OtpTemplateCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpTemplateCreate()**](OtpTemplateCreateApi.md#otpTemplateCreate) | **POST** /api/2fa/authentications/templates | Create a message template |


## `otpTemplateCreate()`

```php
otpTemplateCreate($otp_template_create_request): \BSG\Api\V2\Model\OtpTemplateCreate200Response
```

Create a message template

This method creates a new message template used for sending the OTP code.    **Please note** *that after creating the template, it is moderated. This template will be available for sending messages with the OTP code only after moderation. Once it’s ready, its status will be changed from Requested to Approved.*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\OtpTemplateCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$otp_template_create_request = new \BSG\Api\V2\Model\OtpTemplateCreateRequest(); // \BSG\Api\V2\Model\OtpTemplateCreateRequest

try {
    $result = $apiInstance->otpTemplateCreate($otp_template_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OtpTemplateCreateApi->otpTemplateCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **otp_template_create_request** | [**\BSG\Api\V2\Model\OtpTemplateCreateRequest**](../Model/OtpTemplateCreateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\OtpTemplateCreate200Response**](../Model/OtpTemplateCreate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
