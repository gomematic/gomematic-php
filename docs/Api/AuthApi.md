# Gomematic\AuthApi

All URIs are relative to *http://http:/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**loginUser**](AuthApi.md#loginUser) | **POST** /auth/login | Authenticate an user by credentials
[**refreshAuth**](AuthApi.md#refreshAuth) | **GET** /auth/refresh | Refresh an auth token before it expires
[**verifyAuth**](AuthApi.md#verifyAuth) | **GET** /auth/verify/{token} | Verify validity for an authentication token



## loginUser

> \Gomematic\Model\AuthToken loginUser($auth)

Authenticate an user by credentials

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth = new \Gomematic\Model\InlineObject(); // \Gomematic\Model\InlineObject | 

try {
    $result = $apiInstance->loginUser($auth);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->loginUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth** | [**\Gomematic\Model\InlineObject**](../Model/InlineObject.md)|  |

### Return type

[**\Gomematic\Model\AuthToken**](../Model/AuthToken.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## refreshAuth

> \Gomematic\Model\AuthToken refreshAuth()

Refresh an auth token before it expires

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->refreshAuth();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->refreshAuth: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gomematic\Model\AuthToken**](../Model/AuthToken.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## verifyAuth

> \Gomematic\Model\AuthVerify verifyAuth($token)

Verify validity for an authentication token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$token = 'token_example'; // string | A token that have to be checked

try {
    $result = $apiInstance->verifyAuth($token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->verifyAuth: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **string**| A token that have to be checked |

### Return type

[**\Gomematic\Model\AuthVerify**](../Model/AuthVerify.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)
