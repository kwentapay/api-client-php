# OpenAPI\Client\SettingsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createApiKey()**](SettingsApi.md#createApiKey) | **POST** /settings/api-keys | Create API key |
| [**createMembership()**](SettingsApi.md#createMembership) | **POST** /settings/members | Create membership |
| [**createSeller()**](SettingsApi.md#createSeller) | **POST** /sellers | Create seller |
| [**createStripeAccountLink()**](SettingsApi.md#createStripeAccountLink) | **POST** /settings/stripe-account-links | Create stripe account link |
| [**createWebhookEndpoint()**](SettingsApi.md#createWebhookEndpoint) | **POST** /settings/webhook-endpoints | Create webhook endpoint |
| [**deleteApiKey()**](SettingsApi.md#deleteApiKey) | **DELETE** /api-keys/{apiKeyId} | Delete API key |
| [**deleteMembership()**](SettingsApi.md#deleteMembership) | **DELETE** /settings/members/{membershipId} | Delete membership |
| [**deleteWebhookEndpoint()**](SettingsApi.md#deleteWebhookEndpoint) | **DELETE** /settings/webhook-endpoints/{webhookEndpointId} | Delete webhook endpoint |
| [**getApiKeys()**](SettingsApi.md#getApiKeys) | **GET** /settings/api-keys | Get API keys |
| [**getMembers()**](SettingsApi.md#getMembers) | **GET** /settings/members | Get members |
| [**getStripeAccount()**](SettingsApi.md#getStripeAccount) | **GET** /settings/stripe-account | Get Stripe account |
| [**getWebhookEndpointSecret()**](SettingsApi.md#getWebhookEndpointSecret) | **GET** /settings/webhook-endpoints/{endpointId}/secret | Get webhook endpoint secret |
| [**getWebhookEndpoints()**](SettingsApi.md#getWebhookEndpoints) | **GET** /settings/webhook-endpoints | Get webhook endpoints |
| [**updateApiKeyDescription()**](SettingsApi.md#updateApiKeyDescription) | **PATCH** /settings/api-keys/{apiKeyId} | Update API key description |
| [**updateSellerById()**](SettingsApi.md#updateSellerById) | **PATCH** /settings/seller | Update seller by ID |
| [**uploadLogo()**](SettingsApi.md#uploadLogo) | **PUT** /settings/logo | Upload logo |


## `createApiKey()`

```php
createApiKey($createApiKeyBody): \OpenAPI\Client\Model\CreateApiKeyResponse
```

Create API key

Creates a new  api key for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createApiKeyBody = new \OpenAPI\Client\Model\CreateApiKeyBody(); // \OpenAPI\Client\Model\CreateApiKeyBody

try {
    $result = $apiInstance->createApiKey($createApiKeyBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createApiKeyBody** | [**\OpenAPI\Client\Model\CreateApiKeyBody**](../Model/CreateApiKeyBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateApiKeyResponse**](../Model/CreateApiKeyResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createMembership()`

```php
createMembership($createMembershipApiBody): \OpenAPI\Client\Model\CreateMembershipApiResponse
```

Create membership

Creates a new  membership for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createMembershipApiBody = new \OpenAPI\Client\Model\CreateMembershipApiBody(); // \OpenAPI\Client\Model\CreateMembershipApiBody

try {
    $result = $apiInstance->createMembership($createMembershipApiBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createMembership: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createMembershipApiBody** | [**\OpenAPI\Client\Model\CreateMembershipApiBody**](../Model/CreateMembershipApiBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateMembershipApiResponse**](../Model/CreateMembershipApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createSeller()`

```php
createSeller($createSellerBody): \OpenAPI\Client\Model\CreateSellerResponse
```

Create seller

Creates a new seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createSellerBody = new \OpenAPI\Client\Model\CreateSellerBody(); // \OpenAPI\Client\Model\CreateSellerBody

try {
    $result = $apiInstance->createSeller($createSellerBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createSeller: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createSellerBody** | [**\OpenAPI\Client\Model\CreateSellerBody**](../Model/CreateSellerBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateSellerResponse**](../Model/CreateSellerResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createStripeAccountLink()`

```php
createStripeAccountLink($createSellerStripeAccountLinkApiBody): \OpenAPI\Client\Model\CreateSellerStripeAccountLinkApiResponse
```

Create stripe account link

Create a link to connect stripe account for the seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createSellerStripeAccountLinkApiBody = new \OpenAPI\Client\Model\CreateSellerStripeAccountLinkApiBody(); // \OpenAPI\Client\Model\CreateSellerStripeAccountLinkApiBody

try {
    $result = $apiInstance->createStripeAccountLink($createSellerStripeAccountLinkApiBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createStripeAccountLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createSellerStripeAccountLinkApiBody** | [**\OpenAPI\Client\Model\CreateSellerStripeAccountLinkApiBody**](../Model/CreateSellerStripeAccountLinkApiBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateSellerStripeAccountLinkApiResponse**](../Model/CreateSellerStripeAccountLinkApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createWebhookEndpoint()`

```php
createWebhookEndpoint($createSellerWebhookEndpointBody): \OpenAPI\Client\Model\CreateSellerWebhookEndpointResponse
```

Create webhook endpoint

Creates a new webhook endpoint entry in the list of event receivers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createSellerWebhookEndpointBody = new \OpenAPI\Client\Model\CreateSellerWebhookEndpointBody(); // \OpenAPI\Client\Model\CreateSellerWebhookEndpointBody

try {
    $result = $apiInstance->createWebhookEndpoint($createSellerWebhookEndpointBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->createWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createSellerWebhookEndpointBody** | [**\OpenAPI\Client\Model\CreateSellerWebhookEndpointBody**](../Model/CreateSellerWebhookEndpointBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateSellerWebhookEndpointResponse**](../Model/CreateSellerWebhookEndpointResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteApiKey()`

```php
deleteApiKey($apiKeyId)
```

Delete API key

Delete api key for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apiKeyId = 'apiKeyId_example'; // string

try {
    $apiInstance->deleteApiKey($apiKeyId);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->deleteApiKey: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apiKeyId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteMembership()`

```php
deleteMembership($membershipId)
```

Delete membership

Delete membership for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$membershipId = 'membershipId_example'; // string

try {
    $apiInstance->deleteMembership($membershipId);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->deleteMembership: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **membershipId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWebhookEndpoint()`

```php
deleteWebhookEndpoint($webhookEndpointId)
```

Delete webhook endpoint

Delete webhook endpoint for a seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhookEndpointId = 'webhookEndpointId_example'; // string

try {
    $apiInstance->deleteWebhookEndpoint($webhookEndpointId);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->deleteWebhookEndpoint: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhookEndpointId** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getApiKeys()`

```php
getApiKeys(): \OpenAPI\Client\Model\GetApiKeysApiResponse
```

Get API keys

Get api keys for a seller

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getApiKeys();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getApiKeys: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetApiKeysApiResponse**](../Model/GetApiKeysApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getMembers()`

```php
getMembers(): \OpenAPI\Client\Model\GetMembersApiResponse
```

Get members

Get members for a seller

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMembers();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getMembers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetMembersApiResponse**](../Model/GetMembersApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getStripeAccount()`

```php
getStripeAccount(): \OpenAPI\Client\Model\GetSellerStripeAccountApiResponse
```

Get Stripe account

Get a stripe account for the seller.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getStripeAccount();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getStripeAccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetSellerStripeAccountApiResponse**](../Model/GetSellerStripeAccountApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebhookEndpointSecret()`

```php
getWebhookEndpointSecret($endpointId): \OpenAPI\Client\Model\GetSellerWebhookEndpointSecretApiResponse
```

Get webhook endpoint secret

Get the secret signing key for a webhook endpoint

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$endpointId = 'endpointId_example'; // string

try {
    $result = $apiInstance->getWebhookEndpointSecret($endpointId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getWebhookEndpointSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **endpointId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetSellerWebhookEndpointSecretApiResponse**](../Model/GetSellerWebhookEndpointSecretApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getWebhookEndpoints()`

```php
getWebhookEndpoints(): \OpenAPI\Client\Model\GetSellerWebhookEndpointsApiResponse
```

Get webhook endpoints

Get the list of registered webhook endpoints

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getWebhookEndpoints();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->getWebhookEndpoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GetSellerWebhookEndpointsApiResponse**](../Model/GetSellerWebhookEndpointsApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateApiKeyDescription()`

```php
updateApiKeyDescription($apiKeyId, $updateApiKeyDescriptionBody)
```

Update API key description

Update the description of an api key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$apiKeyId = 'apiKeyId_example'; // string
$updateApiKeyDescriptionBody = new \OpenAPI\Client\Model\UpdateApiKeyDescriptionBody(); // \OpenAPI\Client\Model\UpdateApiKeyDescriptionBody

try {
    $apiInstance->updateApiKeyDescription($apiKeyId, $updateApiKeyDescriptionBody);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->updateApiKeyDescription: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **apiKeyId** | **string**|  | |
| **updateApiKeyDescriptionBody** | [**\OpenAPI\Client\Model\UpdateApiKeyDescriptionBody**](../Model/UpdateApiKeyDescriptionBody.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSellerById()`

```php
updateSellerById($updateSellerByIdApiBody)
```

Update seller by ID

Updates a specific seller information by ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$updateSellerByIdApiBody = new \OpenAPI\Client\Model\UpdateSellerByIdApiBody(); // \OpenAPI\Client\Model\UpdateSellerByIdApiBody

try {
    $apiInstance->updateSellerById($updateSellerByIdApiBody);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->updateSellerById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **updateSellerByIdApiBody** | [**\OpenAPI\Client\Model\UpdateSellerByIdApiBody**](../Model/UpdateSellerByIdApiBody.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadLogo()`

```php
uploadLogo($file): \OpenAPI\Client\Model\UploadSellerLogoResponse
```

Upload logo

Uploads a new seller logo image and replaces it if needed.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->uploadLogo($file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SettingsApi->uploadLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file** | **\SplFileObject****\SplFileObject**|  | |

### Return type

[**\OpenAPI\Client\Model\UploadSellerLogoResponse**](../Model/UploadSellerLogoResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
