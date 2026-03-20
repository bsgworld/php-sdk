# BSG\Api\V2\ContactUpdateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**contactUpdate()**](ContactUpdateApi.md#contactUpdate) | **PUT** /api/contacts/{id} | Update contact |


## `contactUpdate()`

```php
contactUpdate($id, $contact_update_request): \BSG\Api\V2\Model\ContactUpdate200Response
```

Update contact

The method allows you to make changes to an existing contact: change the phone number, data in the contact’s custom fields, and add the contact to the list.  **Please note:** that in the TEST account mode there is a restriction for performing this method: you can only change the contact’s phone number to a verified number (number verification is performed in the personal account at the platform)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ContactUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Contact id
$contact_update_request = new \BSG\Api\V2\Model\ContactUpdateRequest([
    'phone' => 61401629754,
    'fields' => [
        0 => [
            'id' => 387714,
            'value' => 'Ilya Muromets',
        ],
    ],
    'groups' => [
        0 => 1864618,
    ],
]);
try {
    $result = $apiInstance->contactUpdate($id, $contact_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContactUpdateApi->contactUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int** | Contact id | |
| **contact_update_request** | [**\BSG\Api\V2\Model\ContactUpdateRequest**](../Model/ContactUpdateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ContactUpdate200Response**](../Model/ContactUpdate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
