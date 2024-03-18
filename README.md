# KwentaApiClient

Kwenta OpenAPI documentation


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/KwentaApiClient/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OrderApi* | [**cancelOrder**](docs/Api/OrderApi.md#cancelorder) | **POST** /orders/{orderId}/cancel | Cancel order
*OrderApi* | [**createAccountingExport**](docs/Api/OrderApi.md#createaccountingexport) | **POST** /accounting-exports | Create accounting export
*OrderApi* | [**createOrder**](docs/Api/OrderApi.md#createorder) | **POST** /orders | Create order
*OrderApi* | [**createPayers**](docs/Api/OrderApi.md#createpayers) | **POST** /orders/{orderId}/payers | Create payers
*OrderApi* | [**downloadAccountingExport**](docs/Api/OrderApi.md#downloadaccountingexport) | **POST** /accounting-exports/{accountingExportId}/download | Download accounting export
*OrderApi* | [**getAccountingExportById**](docs/Api/OrderApi.md#getaccountingexportbyid) | **GET** /accounting-exports/{accountingExportId} | Get accounting export by ID
*OrderApi* | [**getAccountingExportDownloadUrl**](docs/Api/OrderApi.md#getaccountingexportdownloadurl) | **GET** /accounting-exports/{accountingExportId}/download-url | Get accounting export download URL
*OrderApi* | [**getOrderById**](docs/Api/OrderApi.md#getorderbyid) | **GET** /orders/{orderId} | Get order by ID
*OrderApi* | [**getOrders**](docs/Api/OrderApi.md#getorders) | **GET** /orders | Get orders
*OrderApi* | [**getPayerById**](docs/Api/OrderApi.md#getpayerbyid) | **GET** /orders/{orderId}/payers/{payerId} | Get payer by ID
*OrderApi* | [**shareOrderByEmail**](docs/Api/OrderApi.md#shareorderbyemail) | **POST** /orders/{orderId}/payers/{payerId}/share/email | Share order by email
*OrderApi* | [**shareOrderBySms**](docs/Api/OrderApi.md#shareorderbysms) | **POST** /orders/{orderId}/payers/{payerId}/share/sms | Share order by SMS
*OrderApi* | [**updatePayer**](docs/Api/OrderApi.md#updatepayer) | **PATCH** /payers/{payerId} | Update payer.
*OrderApi* | [**updatePaymentAmount**](docs/Api/OrderApi.md#updatepaymentamount) | **PATCH** /payments/{paymentId} | Update payment amount
*RefundsApi* | [**divideOrderRefund**](docs/Api/RefundsApi.md#divideorderrefund) | **POST** /refunds/order/{orderRefundId} | Divide order refund
*RefundsApi* | [**dividePayerRefund**](docs/Api/RefundsApi.md#dividepayerrefund) | **POST** /refunds/payer/{payerRefundId} | Divide payer refund
*RefundsApi* | [**getOrderRefundById**](docs/Api/RefundsApi.md#getorderrefundbyid) | **GET** /refunds/order/{orderRefundId} | Get order refund by ID
*RefundsApi* | [**getOrdersRefunds**](docs/Api/RefundsApi.md#getordersrefunds) | **GET** /orders/refunds | Get orders refunds
*RefundsApi* | [**getPayerRefundById**](docs/Api/RefundsApi.md#getpayerrefundbyid) | **GET** /refunds/payer/{payerRefundId} | Get payer refund by ID
*RefundsApi* | [**refundOrder**](docs/Api/RefundsApi.md#refundorder) | **POST** /orders/{orderId}/refunds | Refund order
*SettingsApi* | [**createApiKey**](docs/Api/SettingsApi.md#createapikey) | **POST** /settings/api-keys | Create API key
*SettingsApi* | [**createMembership**](docs/Api/SettingsApi.md#createmembership) | **POST** /settings/members | Create membership
*SettingsApi* | [**createSeller**](docs/Api/SettingsApi.md#createseller) | **POST** /sellers | Create seller
*SettingsApi* | [**createStripeAccountLink**](docs/Api/SettingsApi.md#createstripeaccountlink) | **POST** /settings/stripe-account-links | Create stripe account link
*SettingsApi* | [**createWebhookEndpoint**](docs/Api/SettingsApi.md#createwebhookendpoint) | **POST** /settings/webhook-endpoints | Create webhook endpoint
*SettingsApi* | [**deleteApiKey**](docs/Api/SettingsApi.md#deleteapikey) | **DELETE** /api-keys/{apiKeyId} | Delete API key
*SettingsApi* | [**deleteMembership**](docs/Api/SettingsApi.md#deletemembership) | **DELETE** /settings/members/{membershipId} | Delete membership
*SettingsApi* | [**deleteWebhookEndpoint**](docs/Api/SettingsApi.md#deletewebhookendpoint) | **DELETE** /settings/webhook-endpoints/{webhookEndpointId} | Delete webhook endpoint
*SettingsApi* | [**getApiKeys**](docs/Api/SettingsApi.md#getapikeys) | **GET** /settings/api-keys | Get API keys
*SettingsApi* | [**getMembers**](docs/Api/SettingsApi.md#getmembers) | **GET** /settings/members | Get members
*SettingsApi* | [**getStripeAccount**](docs/Api/SettingsApi.md#getstripeaccount) | **GET** /settings/stripe-account | Get Stripe account
*SettingsApi* | [**getWebhookEndpointSecret**](docs/Api/SettingsApi.md#getwebhookendpointsecret) | **GET** /settings/webhook-endpoints/{endpointId}/secret | Get webhook endpoint secret
*SettingsApi* | [**getWebhookEndpoints**](docs/Api/SettingsApi.md#getwebhookendpoints) | **GET** /settings/webhook-endpoints | Get webhook endpoints
*SettingsApi* | [**updateApiKeyDescription**](docs/Api/SettingsApi.md#updateapikeydescription) | **PATCH** /settings/api-keys/{apiKeyId} | Update API key description
*SettingsApi* | [**updateSellerById**](docs/Api/SettingsApi.md#updatesellerbyid) | **PATCH** /settings/seller | Update seller by ID
*SettingsApi* | [**uploadLogo**](docs/Api/SettingsApi.md#uploadlogo) | **PUT** /settings/logo | Upload logo
*UserApi* | [**getProfile**](docs/Api/UserApi.md#getprofile) | **GET** /profile | Get profile

## Models

- [AccountingExportStatus](docs/Model/AccountingExportStatus.md)
- [CreateAccountingExportBody](docs/Model/CreateAccountingExportBody.md)
- [CreateAccountingExportResponse](docs/Model/CreateAccountingExportResponse.md)
- [CreateApiKeyBody](docs/Model/CreateApiKeyBody.md)
- [CreateApiKeyResponse](docs/Model/CreateApiKeyResponse.md)
- [CreateMembershipApiBody](docs/Model/CreateMembershipApiBody.md)
- [CreateMembershipApiResponse](docs/Model/CreateMembershipApiResponse.md)
- [CreateOrderBody](docs/Model/CreateOrderBody.md)
- [CreateOrderResponse](docs/Model/CreateOrderResponse.md)
- [CreatePayersBody](docs/Model/CreatePayersBody.md)
- [CreatePayersBodyItem](docs/Model/CreatePayersBodyItem.md)
- [CreateSellerBody](docs/Model/CreateSellerBody.md)
- [CreateSellerResponse](docs/Model/CreateSellerResponse.md)
- [CreateSellerStripeAccountLinkApiBody](docs/Model/CreateSellerStripeAccountLinkApiBody.md)
- [CreateSellerStripeAccountLinkApiResponse](docs/Model/CreateSellerStripeAccountLinkApiResponse.md)
- [CreateSellerWebhookEndpointBody](docs/Model/CreateSellerWebhookEndpointBody.md)
- [CreateSellerWebhookEndpointResponse](docs/Model/CreateSellerWebhookEndpointResponse.md)
- [Currency](docs/Model/Currency.md)
- [DividePayerRefundBody](docs/Model/DividePayerRefundBody.md)
- [GetAccountingExportByIdResponse](docs/Model/GetAccountingExportByIdResponse.md)
- [GetAccountingExportDownloadUrlResponse](docs/Model/GetAccountingExportDownloadUrlResponse.md)
- [GetApiKeysApiResponse](docs/Model/GetApiKeysApiResponse.md)
- [GetApiKeysResponseApiKey](docs/Model/GetApiKeysResponseApiKey.md)
- [GetCardPaymentMethodResponse](docs/Model/GetCardPaymentMethodResponse.md)
- [GetMembersApiResponse](docs/Model/GetMembersApiResponse.md)
- [GetMembersApiResponseMember](docs/Model/GetMembersApiResponseMember.md)
- [GetOrderByIdResponse](docs/Model/GetOrderByIdResponse.md)
- [GetOrderByIdResponseOrderRefund](docs/Model/GetOrderByIdResponseOrderRefund.md)
- [GetOrderByIdResponsePayer](docs/Model/GetOrderByIdResponsePayer.md)
- [GetOrderByIdResponsePayerRefund](docs/Model/GetOrderByIdResponsePayerRefund.md)
- [GetOrderByIdResponsePayerRefundPayer](docs/Model/GetOrderByIdResponsePayerRefundPayer.md)
- [GetOrderByIdResponsePayment](docs/Model/GetOrderByIdResponsePayment.md)
- [GetOrderByIdResponsePaymentRefund](docs/Model/GetOrderByIdResponsePaymentRefund.md)
- [GetOrderByIdResponsePaymentRefundFailure](docs/Model/GetOrderByIdResponsePaymentRefundFailure.md)
- [GetOrderByIdResponsePaymentRefundPayment](docs/Model/GetOrderByIdResponsePaymentRefundPayment.md)
- [GetOrderByIdResponsePaymentRefundPaymentCardPaymentMethod](docs/Model/GetOrderByIdResponsePaymentRefundPaymentCardPaymentMethod.md)
- [GetOrderByIdResponseSeller](docs/Model/GetOrderByIdResponseSeller.md)
- [GetOrderRefundByIdResponse](docs/Model/GetOrderRefundByIdResponse.md)
- [GetOrderRefundByIdResponseOrder](docs/Model/GetOrderRefundByIdResponseOrder.md)
- [GetOrderRefundByIdResponsePayer](docs/Model/GetOrderRefundByIdResponsePayer.md)
- [GetOrderRefundByIdResponseSeller](docs/Model/GetOrderRefundByIdResponseSeller.md)
- [GetOrdersApiResponse](docs/Model/GetOrdersApiResponse.md)
- [GetOrdersApiResponseOrder](docs/Model/GetOrdersApiResponseOrder.md)
- [GetOrdersRefundsApiResponse](docs/Model/GetOrdersRefundsApiResponse.md)
- [GetOrdersRefundsApiResponseRefund](docs/Model/GetOrdersRefundsApiResponseRefund.md)
- [GetPayerByIdResponse](docs/Model/GetPayerByIdResponse.md)
- [GetPayerByIdResponseOrder](docs/Model/GetPayerByIdResponseOrder.md)
- [GetPayerByIdResponsePayment](docs/Model/GetPayerByIdResponsePayment.md)
- [GetPayerRefundByIdResponse](docs/Model/GetPayerRefundByIdResponse.md)
- [GetPayerRefundByIdResponseOrder](docs/Model/GetPayerRefundByIdResponseOrder.md)
- [GetPayerRefundByIdResponsePayment](docs/Model/GetPayerRefundByIdResponsePayment.md)
- [GetPayerRefundByIdResponseSeller](docs/Model/GetPayerRefundByIdResponseSeller.md)
- [GetProfileResponse](docs/Model/GetProfileResponse.md)
- [GetProfileResponseSeller](docs/Model/GetProfileResponseSeller.md)
- [GetSellerStripeAccountApiResponse](docs/Model/GetSellerStripeAccountApiResponse.md)
- [GetSellerWebhookEndpointSecretApiResponse](docs/Model/GetSellerWebhookEndpointSecretApiResponse.md)
- [GetSellerWebhookEndpointsApiResponse](docs/Model/GetSellerWebhookEndpointsApiResponse.md)
- [GetSellerWebhookEndpointsApiResponseWebhookEndpoint](docs/Model/GetSellerWebhookEndpointsApiResponseWebhookEndpoint.md)
- [OrderRefundStatus](docs/Model/OrderRefundStatus.md)
- [OrderStatus](docs/Model/OrderStatus.md)
- [OrderType](docs/Model/OrderType.md)
- [PayerRefundStatus](docs/Model/PayerRefundStatus.md)
- [PayerStatus](docs/Model/PayerStatus.md)
- [PaymentMethodType](docs/Model/PaymentMethodType.md)
- [PaymentStatus](docs/Model/PaymentStatus.md)
- [RefundOrderApiBody](docs/Model/RefundOrderApiBody.md)
- [RefundOrderResponse](docs/Model/RefundOrderResponse.md)
- [RefundOrderResponsePayerRefund](docs/Model/RefundOrderResponsePayerRefund.md)
- [RefundOrderResponsePaymentRefund](docs/Model/RefundOrderResponsePaymentRefund.md)
- [RefundOrderResponsePaymentRefundFailure](docs/Model/RefundOrderResponsePaymentRefundFailure.md)
- [ShareOrderByEmailBody](docs/Model/ShareOrderByEmailBody.md)
- [ShareOrderBySmsBody](docs/Model/ShareOrderBySmsBody.md)
- [SupportedLocale](docs/Model/SupportedLocale.md)
- [UpdateApiKeyDescriptionBody](docs/Model/UpdateApiKeyDescriptionBody.md)
- [UpdatePayerBody](docs/Model/UpdatePayerBody.md)
- [UpdatePaymentAmountBody](docs/Model/UpdatePaymentAmountBody.md)
- [UpdateSellerByIdApiBody](docs/Model/UpdateSellerByIdApiBody.md)
- [UploadSellerLogoResponse](docs/Model/UploadSellerLogoResponse.md)

## Authorization

Authentication schemes defined for the API:
### bearer

- **Type**: Bearer authentication (JWT)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
