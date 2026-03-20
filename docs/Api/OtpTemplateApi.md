# BSG\Api\V2\OtpTemplateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**otpTemplate()**](OtpTemplateApi.md#otpTemplate) | **GET** /api/2fa/authentications/templates/{templateId} | Get message template |


## `otpTemplate()`

```php
otpTemplate($template_id): \BSG\Api\V2\Model\OtpTemplate200Response
```

Get message template

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\OtpTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$template_id = 56; // int | Template id

try {
    $result = $apiInstance->otpTemplate($template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OtpTemplateApi->otpTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **template_id** | **int** | Template id | |

### Return type

[**\BSG\Api\V2\Model\OtpTemplate200Response**](../Model/OtpTemplate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
