# # GetOrderByIdResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of the order |
**sellerOrderId** | **string** | The ID of the order in the seller&#39;s system | [optional]
**seller** | [**\OpenAPI\Client\Model\GetOrderByIdResponseSeller**](GetOrderByIdResponseSeller.md) |  |
**type** | [**\OpenAPI\Client\Model\OrderType**](OrderType.md) |  |
**ownerId** | **string** | ID of the payer who owns the order | [optional]
**status** | [**\OpenAPI\Client\Model\OrderStatus**](OrderStatus.md) |  |
**amount** | **int** | Total amount of the order expressed in the smallest unit of the currency. |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**redirectUrl** | **string** | URL on your website to redirect the payer to after a successful payment. | [optional]
**expiresAt** | **\DateTime** | Expiration date of the order. | [optional]
**createdAt** | **\DateTime** | The date and time when the entity was created |
**payers** | [**\OpenAPI\Client\Model\GetOrderByIdResponsePayer[]**](GetOrderByIdResponsePayer.md) |  |
**defaultLocale** | [**\OpenAPI\Client\Model\SupportedLocale**](SupportedLocale.md) |  | [optional]
**refundableAmount** | **int** |  |
**refunds** | [**\OpenAPI\Client\Model\GetOrderByIdResponseOrderRefund[]**](GetOrderByIdResponseOrderRefund.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
