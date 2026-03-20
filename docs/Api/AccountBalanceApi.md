# BSG\Api\V2\AccountBalanceApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**accountBalance()**](AccountBalanceApi.md#accountBalance) | **GET** /api/accounts/balance | Get balance |


## `accountBalance()`

```php
accountBalance(): \BSG\Api\V2\Model\AccountBalance200Response
```

Get balance

Platform provides an API to get information about your account balance. The request allows you to obtain information about the current balance of your account, including the credit limit

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\AccountBalanceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountBalanceApi->accountBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\BSG\Api\V2\Model\AccountBalance200Response**](../Model/AccountBalance200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
