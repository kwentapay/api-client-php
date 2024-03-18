# OpenAPI\Client\OrderApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cancelOrder()**](OrderApi.md#cancelOrder) | **POST** /orders/{orderId}/cancel | Cancel order |
| [**createAccountingExport()**](OrderApi.md#createAccountingExport) | **POST** /accounting-exports | Create accounting export |
| [**createOrder()**](OrderApi.md#createOrder) | **POST** /orders | Create order |
| [**createPayers()**](OrderApi.md#createPayers) | **POST** /orders/{orderId}/payers | Create payers |
| [**downloadAccountingExport()**](OrderApi.md#downloadAccountingExport) | **POST** /accounting-exports/{accountingExportId}/download | Download accounting export |
| [**getAccountingExportById()**](OrderApi.md#getAccountingExportById) | **GET** /accounting-exports/{accountingExportId} | Get accounting export by ID |
| [**getAccountingExportDownloadUrl()**](OrderApi.md#getAccountingExportDownloadUrl) | **GET** /accounting-exports/{accountingExportId}/download-url | Get accounting export download URL |
| [**getOrderById()**](OrderApi.md#getOrderById) | **GET** /orders/{orderId} | Get order by ID |
| [**getOrders()**](OrderApi.md#getOrders) | **GET** /orders | Get orders |
| [**getPayerById()**](OrderApi.md#getPayerById) | **GET** /orders/{orderId}/payers/{payerId} | Get payer by ID |
| [**shareOrderByEmail()**](OrderApi.md#shareOrderByEmail) | **POST** /orders/{orderId}/payers/{payerId}/share/email | Share order by email |
| [**shareOrderBySms()**](OrderApi.md#shareOrderBySms) | **POST** /orders/{orderId}/payers/{payerId}/share/sms | Share order by SMS |
| [**updatePayer()**](OrderApi.md#updatePayer) | **PATCH** /payers/{payerId} | Update payer. |
| [**updatePaymentAmount()**](OrderApi.md#updatePaymentAmount) | **PATCH** /payments/{paymentId} | Update payment amount |


## `cancelOrder()`

```php
cancelOrder($orderId)
```

Cancel order

Cancel an existing order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$orderId = 'orderId_example'; // string

try {
    $apiInstance->cancelOrder($orderId);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->cancelOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |

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

## `createAccountingExport()`

```php
createAccountingExport($createAccountingExportBody): \OpenAPI\Client\Model\CreateAccountingExportResponse
```

Create accounting export

Creates a new accounting export job.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createAccountingExportBody = new \OpenAPI\Client\Model\CreateAccountingExportBody(); // \OpenAPI\Client\Model\CreateAccountingExportBody

try {
    $result = $apiInstance->createAccountingExport($createAccountingExportBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->createAccountingExport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createAccountingExportBody** | [**\OpenAPI\Client\Model\CreateAccountingExportBody**](../Model/CreateAccountingExportBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateAccountingExportResponse**](../Model/CreateAccountingExportResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createOrder()`

```php
createOrder($createOrderBody): \OpenAPI\Client\Model\CreateOrderResponse
```

Create order

Creates a new order associated with the seller who owns the API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createOrderBody = new \OpenAPI\Client\Model\CreateOrderBody(); // \OpenAPI\Client\Model\CreateOrderBody

try {
    $result = $apiInstance->createOrder($createOrderBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->createOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createOrderBody** | [**\OpenAPI\Client\Model\CreateOrderBody**](../Model/CreateOrderBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CreateOrderResponse**](../Model/CreateOrderResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createPayers()`

```php
createPayers($orderId, $createPayersBody): string[]
```

Create payers

Splits an order into multiple payers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderId = 'orderId_example'; // string
$createPayersBody = new \OpenAPI\Client\Model\CreatePayersBody(); // \OpenAPI\Client\Model\CreatePayersBody

try {
    $result = $apiInstance->createPayers($orderId, $createPayersBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->createPayers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |
| **createPayersBody** | [**\OpenAPI\Client\Model\CreatePayersBody**](../Model/CreatePayersBody.md)|  | |

### Return type

**string[]**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `downloadAccountingExport()`

```php
downloadAccountingExport($accountingExportId)
```

Download accounting export

Download a finished accounting export.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountingExportId = 'accountingExportId_example'; // string

try {
    $apiInstance->downloadAccountingExport($accountingExportId);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->downloadAccountingExport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountingExportId** | **string**|  | |

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

## `getAccountingExportById()`

```php
getAccountingExportById($accountingExportId): \OpenAPI\Client\Model\GetAccountingExportByIdResponse
```

Get accounting export by ID

Get an accounting export from its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountingExportId = 'accountingExportId_example'; // string

try {
    $result = $apiInstance->getAccountingExportById($accountingExportId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getAccountingExportById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountingExportId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetAccountingExportByIdResponse**](../Model/GetAccountingExportByIdResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAccountingExportDownloadUrl()`

```php
getAccountingExportDownloadUrl($accountingExportId): \OpenAPI\Client\Model\GetAccountingExportDownloadUrlResponse
```

Get accounting export download URL

Get a signed accounting export download URL from its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$accountingExportId = 'accountingExportId_example'; // string

try {
    $result = $apiInstance->getAccountingExportDownloadUrl($accountingExportId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getAccountingExportDownloadUrl: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accountingExportId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetAccountingExportDownloadUrlResponse**](../Model/GetAccountingExportDownloadUrlResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderById()`

```php
getOrderById($orderId): \OpenAPI\Client\Model\GetOrderByIdResponse
```

Get order by ID

Gets an order by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderId = 'orderId_example'; // string

try {
    $result = $apiInstance->getOrderById($orderId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getOrderById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetOrderByIdResponse**](../Model/GetOrderByIdResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrders()`

```php
getOrders($limit, $startingAfter, $endingBefore): \OpenAPI\Client\Model\GetOrdersApiResponse
```

Get orders

Get all orders of a given seller

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 10; // int
$startingAfter = 483884f7-eb24-4798-b135-b7d7c381ebae; // string | Universally unique identifier (UUID) v4
$endingBefore = 483884f7-eb24-4798-b135-b7d7c381ebae; // string | Universally unique identifier (UUID) v4

try {
    $result = $apiInstance->getOrders($limit, $startingAfter, $endingBefore);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 10] |
| **startingAfter** | **string**| Universally unique identifier (UUID) v4 | [optional] |
| **endingBefore** | **string**| Universally unique identifier (UUID) v4 | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOrdersApiResponse**](../Model/GetOrdersApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPayerById()`

```php
getPayerById($orderId, $payerId): \OpenAPI\Client\Model\GetPayerByIdResponse
```

Get payer by ID

Get an payer from its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderId = 'orderId_example'; // string
$payerId = 'payerId_example'; // string

try {
    $result = $apiInstance->getPayerById($orderId, $payerId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getPayerById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |
| **payerId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetPayerByIdResponse**](../Model/GetPayerByIdResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shareOrderByEmail()`

```php
shareOrderByEmail($orderId, $payerId, $shareOrderByEmailBody)
```

Share order by email

Share and order to a payer by email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderId = 'orderId_example'; // string
$payerId = 'payerId_example'; // string
$shareOrderByEmailBody = new \OpenAPI\Client\Model\ShareOrderByEmailBody(); // \OpenAPI\Client\Model\ShareOrderByEmailBody

try {
    $apiInstance->shareOrderByEmail($orderId, $payerId, $shareOrderByEmailBody);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->shareOrderByEmail: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |
| **payerId** | **string**|  | |
| **shareOrderByEmailBody** | [**\OpenAPI\Client\Model\ShareOrderByEmailBody**](../Model/ShareOrderByEmailBody.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shareOrderBySms()`

```php
shareOrderBySms($orderId, $payerId, $shareOrderBySmsBody)
```

Share order by SMS

Share and order to a payer by SMS.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderId = 'orderId_example'; // string
$payerId = 'payerId_example'; // string
$shareOrderBySmsBody = new \OpenAPI\Client\Model\ShareOrderBySmsBody(); // \OpenAPI\Client\Model\ShareOrderBySmsBody

try {
    $apiInstance->shareOrderBySms($orderId, $payerId, $shareOrderBySmsBody);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->shareOrderBySms: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |
| **payerId** | **string**|  | |
| **shareOrderBySmsBody** | [**\OpenAPI\Client\Model\ShareOrderBySmsBody**](../Model/ShareOrderBySmsBody.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePayer()`

```php
updatePayer($payerId, $updatePayerBody)
```

Update payer.

Update a payer.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$payerId = 'payerId_example'; // string
$updatePayerBody = new \OpenAPI\Client\Model\UpdatePayerBody(); // \OpenAPI\Client\Model\UpdatePayerBody

try {
    $apiInstance->updatePayer($payerId, $updatePayerBody);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->updatePayer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payerId** | **string**|  | |
| **updatePayerBody** | [**\OpenAPI\Client\Model\UpdatePayerBody**](../Model/UpdatePayerBody.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePaymentAmount()`

```php
updatePaymentAmount($paymentId, $updatePaymentAmountBody)
```

Update payment amount

Update the amount of a payment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$paymentId = 'paymentId_example'; // string
$updatePaymentAmountBody = new \OpenAPI\Client\Model\UpdatePaymentAmountBody(); // \OpenAPI\Client\Model\UpdatePaymentAmountBody

try {
    $apiInstance->updatePaymentAmount($paymentId, $updatePaymentAmountBody);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->updatePaymentAmount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **paymentId** | **string**|  | |
| **updatePaymentAmountBody** | [**\OpenAPI\Client\Model\UpdatePaymentAmountBody**](../Model/UpdatePaymentAmountBody.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
