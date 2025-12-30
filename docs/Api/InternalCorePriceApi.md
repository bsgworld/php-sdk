# BSG\Api\V2\InternalCorePriceApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInternalCorePrices()**](InternalCorePriceApi.md#getInternalCorePrices) | **GET** /api/internal/core/prices | Get price list for each country |
| [**getInternalCorePricesByCountryCode()**](InternalCorePriceApi.md#getInternalCorePricesByCountryCode) | **GET** /api/internal/core/prices/{countryCode} | Get prices for country |


## `getInternalCorePrices()`

```php
getInternalCorePrices($product): \BSG\Api\V2\Model\GetInternalCorePrices200Response
```

Get price list for each country

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: InternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\InternalCorePriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product = 'product_example'; // string | Product value

try {
    $result = $apiInstance->getInternalCorePrices($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalCorePriceApi->getInternalCorePrices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product** | **string** | Product value | |

### Return type

[**\BSG\Api\V2\Model\GetInternalCorePrices200Response**](../Model/GetInternalCorePrices200Response.md)

### Authorization

[InternalAuth](../../README.md#InternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInternalCorePricesByCountryCode()`

```php
getInternalCorePricesByCountryCode($country_code, $product): \BSG\Api\V2\Model\GetInternalCorePricesByCountryCode200Response
```

Get prices for country

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: InternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\InternalCorePriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = 'AB'; //  string | Country ISO Code
$product = 'product_example'; // string | Product value

try {
    $result = $apiInstance->getInternalCorePricesByCountryCode($country_code, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalCorePriceApi->getInternalCorePricesByCountryCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country_code** | **string** | Country ISO Code | |
| **product** | **string** | Product value | |

### Return type

[**\BSG\Api\V2\Model\GetInternalCorePricesByCountryCode200Response**](../Model/GetInternalCorePricesByCountryCode200Response.md)

### Authorization

[InternalAuth](../../README.md#InternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
