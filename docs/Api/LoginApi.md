# BSG\Api\V2\LoginApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**login()**](LoginApi.md#login) | **POST** /api/auth/login | Receive JWT token |


## `login()`

```php
login($login_request): \BSG\Api\V2\Model\TokenSchema
```

Receive JWT token

Receive JWT token to use with other method. Use live/test api-key to login. JWT-token has limited lifetime and have to be refreshed before become expired

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new BSG\Api\V2\Api\LoginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$login_request = new \BSG\Api\V2\Model\LoginRequest([
    'api_key' => 'live_XXXXXXXXXXXXXXXXXXXX',
]);
try {
    $result = $apiInstance->login($login_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoginApi->login: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **login_request** | [**\BSG\Api\V2\Model\LoginRequest**](../Model/LoginRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\TokenSchema**](../Model/TokenSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
