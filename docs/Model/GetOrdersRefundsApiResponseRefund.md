# # GetOrdersRefundsApiResponseRefund

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Universally unique identifier (UUID) v4 |
**orderId** | **string** | The ID of the order |
**amount** | **int** | Total amount of the order expressed in the smallest unit of the currency. |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**createdAt** | **\DateTime** | The date and time when the entity was created |
**status** | [**\OpenAPI\Client\Model\OrderStatus**](OrderStatus.md) |  |
**refundedAt** | **\DateTime** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
