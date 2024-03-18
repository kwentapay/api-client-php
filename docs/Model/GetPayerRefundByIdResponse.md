# # GetPayerRefundByIdResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Universally unique identifier (UUID) v4 |
**amount** | **int** |  |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**createdAt** | **\DateTime** | The date and time when the entity was created |
**status** | [**\OpenAPI\Client\Model\PayerRefundStatus**](PayerRefundStatus.md) |  |
**refundedAt** | **\DateTime** |  | [optional]
**seller** | [**\OpenAPI\Client\Model\GetPayerRefundByIdResponseSeller**](GetPayerRefundByIdResponseSeller.md) |  |
**order** | [**\OpenAPI\Client\Model\GetPayerRefundByIdResponseOrder**](GetPayerRefundByIdResponseOrder.md) |  |
**payments** | [**\OpenAPI\Client\Model\GetPayerRefundByIdResponsePayment[]**](GetPayerRefundByIdResponsePayment.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
