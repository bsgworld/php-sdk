# BSG\Api\V2\OtpTemplateDeleteApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpTemplateDelete()**](OtpTemplateDeleteApi.md#otpTemplateDelete) | **DELETE** /api/2fa/authentications/templates/{templateId} | Delete a message template |


## `otpTemplateDelete()`

```php
otpTemplateDelete($template_id): \BSG\Api\V2\Model\OtpTemplateDelete200Response
```

Delete a message template

This method deletes the message template for sending the OTP code based on its unique identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\OtpTemplateDeleteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 56; // int | The ID of the message template that you want to delete. From 1 to 9 digits.

try {
    $result = $apiInstance->otpTemplateDelete($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OtpTemplateDeleteApi->otpTemplateDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **int** | The ID of the message template that you want to delete. From 1 to 9 digits. | |

### Return type

[**\BSG\Api\V2\Model\OtpTemplateDelete200Response**](../Model/OtpTemplateDelete200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
