# BSG\Api\V2\InternalWstPriceApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInternalWstPrices()**](InternalWstPriceApi.md#getInternalWstPrices) | **GET** /api/internal/wst/prices | Get price list for each country |
| [**getInternalWstPricesByCountryCode()**](InternalWstPriceApi.md#getInternalWstPricesByCountryCode) | **GET** /api/internal/wst/prices/{countryCode} | Get prices for country |


## `getInternalWstPrices()`

```php
getInternalWstPrices($product): \BSG\Api\V2\Model\GetInternalWstPrices200Response
```

Get price list for each country

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: InternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\InternalWstPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product = 'product_example'; // string | Product value

try {
    $result = $apiInstance->getInternalWstPrices($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalWstPriceApi->getInternalWstPrices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product** | **string** | Product value | |

### Return type

[**\BSG\Api\V2\Model\GetInternalWstPrices200Response**](../Model/GetInternalWstPrices200Response.md)

### Authorization

[InternalAuth](../../README.md#InternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInternalWstPricesByCountryCode()`

```php
getInternalWstPricesByCountryCode($country_code, $product): \BSG\Api\V2\Model\GetInternalWstPricesByCountryCode200Response
```

Get prices for country

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: InternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\InternalWstPriceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$country_code = 'AB'; //  string | Country ISO Code
$product = 'product_example'; // string | Product value

try {
    $result = $apiInstance->getInternalWstPricesByCountryCode($country_code, $product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InternalWstPriceApi->getInternalWstPricesByCountryCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **country_code** | **string** | Country ISO Code | |
| **product** | **string** | Product value | |

### Return type

[**\BSG\Api\V2\Model\GetInternalWstPricesByCountryCode200Response**](../Model/GetInternalWstPricesByCountryCode200Response.md)

### Authorization

[InternalAuth](../../README.md#InternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
