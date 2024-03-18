# # GetOrderRefundByIdResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Universally unique identifier (UUID) v4 |
**amount** | **int** |  |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**createdAt** | **\DateTime** | The date and time when the entity was created |
**status** | [**\OpenAPI\Client\Model\OrderRefundStatus**](OrderRefundStatus.md) |  |
**refundedAt** | **\DateTime** |  | [optional]
**seller** | [**\OpenAPI\Client\Model\GetOrderRefundByIdResponseSeller**](GetOrderRefundByIdResponseSeller.md) |  |
**order** | [**\OpenAPI\Client\Model\GetOrderRefundByIdResponseOrder**](GetOrderRefundByIdResponseOrder.md) |  |
**payers** | [**\OpenAPI\Client\Model\GetOrderRefundByIdResponsePayer[]**](GetOrderRefundByIdResponsePayer.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
