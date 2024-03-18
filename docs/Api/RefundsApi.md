# OpenAPI\Client\RefundsApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**divideOrderRefund()**](RefundsApi.md#divideOrderRefund) | **POST** /refunds/order/{orderRefundId} | Divide order refund |
| [**dividePayerRefund()**](RefundsApi.md#dividePayerRefund) | **POST** /refunds/payer/{payerRefundId} | Divide payer refund |
| [**getOrderRefundById()**](RefundsApi.md#getOrderRefundById) | **GET** /refunds/order/{orderRefundId} | Get order refund by ID |
| [**getOrdersRefunds()**](RefundsApi.md#getOrdersRefunds) | **GET** /orders/refunds | Get orders refunds |
| [**getPayerRefundById()**](RefundsApi.md#getPayerRefundById) | **GET** /refunds/payer/{payerRefundId} | Get payer refund by ID |
| [**refundOrder()**](RefundsApi.md#refundOrder) | **POST** /orders/{orderId}/refunds | Refund order |


## `divideOrderRefund()`

```php
divideOrderRefund($orderRefundId, $dividePayerRefundBody)
```

Divide order refund

Divide the refund of a order to multiple payments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderRefundId = 'orderRefundId_example'; // string
$dividePayerRefundBody = new \OpenAPI\Client\Model\DividePayerRefundBody(); // \OpenAPI\Client\Model\DividePayerRefundBody

try {
    $apiInstance->divideOrderRefund($orderRefundId, $dividePayerRefundBody);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->divideOrderRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderRefundId** | **string**|  | |
| **dividePayerRefundBody** | [**\OpenAPI\Client\Model\DividePayerRefundBody**](../Model/DividePayerRefundBody.md)|  | |

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

## `dividePayerRefund()`

```php
dividePayerRefund($payerRefundId, $dividePayerRefundBody)
```

Divide payer refund

Divide the refund of a payer to multiple payments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$payerRefundId = 'payerRefundId_example'; // string
$dividePayerRefundBody = new \OpenAPI\Client\Model\DividePayerRefundBody(); // \OpenAPI\Client\Model\DividePayerRefundBody

try {
    $apiInstance->dividePayerRefund($payerRefundId, $dividePayerRefundBody);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->dividePayerRefund: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payerRefundId** | **string**|  | |
| **dividePayerRefundBody** | [**\OpenAPI\Client\Model\DividePayerRefundBody**](../Model/DividePayerRefundBody.md)|  | |

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

## `getOrderRefundById()`

```php
getOrderRefundById($orderRefundId): \OpenAPI\Client\Model\GetOrderRefundByIdResponse
```

Get order refund by ID

Gets an order refund by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderRefundId = 'orderRefundId_example'; // string

try {
    $result = $apiInstance->getOrderRefundById($orderRefundId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->getOrderRefundById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderRefundId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetOrderRefundByIdResponse**](../Model/GetOrderRefundByIdResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrdersRefunds()`

```php
getOrdersRefunds($limit, $startingAfter, $endingBefore): \OpenAPI\Client\Model\GetOrdersRefundsApiResponse
```

Get orders refunds

Get all orders refunds

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 10; // int
$startingAfter = 483884f7-eb24-4798-b135-b7d7c381ebae; // string | Universally unique identifier (UUID) v4
$endingBefore = 483884f7-eb24-4798-b135-b7d7c381ebae; // string | Universally unique identifier (UUID) v4

try {
    $result = $apiInstance->getOrdersRefunds($limit, $startingAfter, $endingBefore);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->getOrdersRefunds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**|  | [optional] [default to 10] |
| **startingAfter** | **string**| Universally unique identifier (UUID) v4 | [optional] |
| **endingBefore** | **string**| Universally unique identifier (UUID) v4 | [optional] |

### Return type

[**\OpenAPI\Client\Model\GetOrdersRefundsApiResponse**](../Model/GetOrdersRefundsApiResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPayerRefundById()`

```php
getPayerRefundById($payerRefundId): \OpenAPI\Client\Model\GetPayerRefundByIdResponse
```

Get payer refund by ID

Gets an payer refund by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$payerRefundId = 'payerRefundId_example'; // string

try {
    $result = $apiInstance->getPayerRefundById($payerRefundId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->getPayerRefundById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **payerRefundId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GetPayerRefundByIdResponse**](../Model/GetPayerRefundByIdResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `refundOrder()`

```php
refundOrder($orderId, $refundOrderApiBody): \OpenAPI\Client\Model\RefundOrderResponse
```

Refund order

Refunds an order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RefundsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$orderId = 'orderId_example'; // string
$refundOrderApiBody = new \OpenAPI\Client\Model\RefundOrderApiBody(); // \OpenAPI\Client\Model\RefundOrderApiBody

try {
    $result = $apiInstance->refundOrder($orderId, $refundOrderApiBody);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RefundsApi->refundOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderId** | **string**|  | |
| **refundOrderApiBody** | [**\OpenAPI\Client\Model\RefundOrderApiBody**](../Model/RefundOrderApiBody.md)|  | |

### Return type

[**\OpenAPI\Client\Model\RefundOrderResponse**](../Model/RefundOrderResponse.md)

### Authorization

[bearer](../../README.md#bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
