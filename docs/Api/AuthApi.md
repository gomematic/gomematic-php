# Gomematic\AuthApi

All URIs are relative to *http://try.gomematic.tech/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**loginUser**](AuthApi.md#loginUser) | **POST** /auth/login | Authenticate an user by credentials
[**refreshAuth**](AuthApi.md#refreshAuth) | **GET** /auth/refresh | Refresh an auth token before it expires
[**verifyAuth**](AuthApi.md#verifyAuth) | **GET** /auth/verify | Verify validity for an authentication token



## loginUser

> \Gomematic\Model\AuthToken loginUser($authLogin)

Authenticate an user by credentials

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = Gomematic\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: Header
$config = Gomematic\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gomematic\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authLogin = new \Gomematic\Model\AuthLogin(); // \Gomematic\Model\AuthLogin | The credentials to authenticate

try {
    $result = $apiInstance->loginUser($authLogin);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->loginUser: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authLogin** | [**\Gomematic\Model\AuthLogin**](../Model/AuthLogin.md)| The credentials to authenticate |

### Return type

[**\Gomematic\Model\AuthToken**](../Model/AuthToken.md)

### Authorization

[Basic](../../README.md#Basic), [Header](../../README.md#Header)

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


// Configure HTTP basic authorization: Basic
$config = Gomematic\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: Header
$config = Gomematic\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gomematic\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
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

[Basic](../../README.md#Basic), [Header](../../README.md#Header)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## verifyAuth

> \Gomematic\Model\AuthVerify verifyAuth()

Verify validity for an authentication token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: Basic
$config = Gomematic\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure API key authorization: Header
$config = Gomematic\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Gomematic\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');


$apiInstance = new Gomematic\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->verifyAuth();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->verifyAuth: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Gomematic\Model\AuthVerify**](../Model/AuthVerify.md)

### Authorization

[Basic](../../README.md#Basic), [Header](../../README.md#Header)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

