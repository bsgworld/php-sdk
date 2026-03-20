# BSG\Api\V2\ShortUrlsLinkUpdateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsLinkUpdate()**](ShortUrlsLinkUpdateApi.md#shortUrlsLinkUpdate) | **PUT** /api/short-url/links/{uuid} | Update short link |


## `shortUrlsLinkUpdate()`

```php
shortUrlsLinkUpdate($uuid, $link_update_request): \BSG\Api\V2\Model\ShortUrlsLinkUpdate200Response
```

Update short link

You can update short link name, slug or original link  **Please note:** If you change the original link to new one that hasn't been ever used before it may requires moderation and short link status may be changed to *blocked*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsLinkUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'uuid_example'; // string | Uuid of entity
$link_update_request = new \BSG\Api\V2\Model\LinkUpdateRequest([
    'name' => 'New name',
]);
try {
    $result = $apiInstance->shortUrlsLinkUpdate($uuid, $link_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsLinkUpdateApi->shortUrlsLinkUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string** | Uuid of entity | |
| **link_update_request** | [**\BSG\Api\V2\Model\LinkUpdateRequest**](../Model/LinkUpdateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsLinkUpdate200Response**](../Model/ShortUrlsLinkUpdate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
