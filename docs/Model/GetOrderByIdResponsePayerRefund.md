# # GetOrderByIdResponsePayerRefund

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of the payer |
**status** | [**\OpenAPI\Client\Model\PayerRefundStatus**](PayerRefundStatus.md) |  |
**amount** | **int** | Amount due by the payer expressed in the smallest unit of the currency. |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**payer** | [**\OpenAPI\Client\Model\GetOrderByIdResponsePayerRefundPayer**](GetOrderByIdResponsePayerRefundPayer.md) |  |
**paymentRefunds** | [**\OpenAPI\Client\Model\GetOrderByIdResponsePaymentRefund[]**](GetOrderByIdResponsePaymentRefund.md) |  |
**paymentRefundFailures** | [**\OpenAPI\Client\Model\GetOrderByIdResponsePaymentRefundFailure[]**](GetOrderByIdResponsePaymentRefundFailure.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
