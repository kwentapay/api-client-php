# # GetPayerByIdResponsePayment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of the payment |
**status** | [**\OpenAPI\Client\Model\PaymentStatus**](PaymentStatus.md) |  |
**amount** | **int** | Amount of the payment expressed in the smallest unit of the order currency. |
**stripeClientSecret** | **string** |  |
**stripePaymentIntentId** | **string** |  |
**paymentMethodType** | **object** |  | [optional]
**paymentMethod** | [**\OpenAPI\Client\Model\GetCardPaymentMethodResponse**](GetCardPaymentMethodResponse.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
