# BSG\Api\V2\StatisticApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**statJobsCreate()**](StatisticApi.md#statJobsCreate) | **POST** /api/stat/jobs | Create new job |
| [**statJobsDelete()**](StatisticApi.md#statJobsDelete) | **DELETE** /api/stat/jobs/{id} | Delete job result |
| [**statJobsList()**](StatisticApi.md#statJobsList) | **GET** /api/stat/jobs | List statistic jobs |
| [**statJobsShow()**](StatisticApi.md#statJobsShow) | **GET** /api/stat/jobs/{id} | Load job result |


## `statJobsCreate()`

```php
statJobsCreate($stat_jobs_create_request): \BSG\Api\V2\Model\StatJobsCreate200Response
```

Create new job

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StatisticApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stat_jobs_create_request = new \BSG\Api\V2\Model\StatJobsCreateRequest(); // \BSG\Api\V2\Model\StatJobsCreateRequest

try {
    $result = $apiInstance->statJobsCreate($stat_jobs_create_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatisticApi->statJobsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stat_jobs_create_request** | [**\BSG\Api\V2\Model\StatJobsCreateRequest**](../Model/StatJobsCreateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\StatJobsCreate200Response**](../Model/StatJobsCreate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `statJobsDelete()`

```php
statJobsDelete($id): \BSG\Api\V2\Model\StatJobsDelete200Response
```

Delete job result

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StatisticApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = '3941ffacdd698b404e'; //  string | Job identifier

try {
    $result = $apiInstance->statJobsDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatisticApi->statJobsDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string** | Job identifier | |

### Return type

[**\BSG\Api\V2\Model\StatJobsDelete200Response**](../Model/StatJobsDelete200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `statJobsList()`

```php
statJobsList(): object
```

List statistic jobs

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StatisticApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->statJobsList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatisticApi->statJobsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `statJobsShow()`

```php
statJobsShow($id): object
```

Load job result

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\StatisticApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = '3941ffacdd698b404e'; //  string | Job identifier

try {
    $result = $apiInstance->statJobsShow($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatisticApi->statJobsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string** | Job identifier | |

### Return type

**object**

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
