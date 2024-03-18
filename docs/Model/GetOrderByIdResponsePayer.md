# # GetOrderByIdResponsePayer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The ID of the payer |
**index** | **int** | Index of the payer. The index is used to calculate the gradient of the payer&#39;s color and his position |
**status** | [**\OpenAPI\Client\Model\PayerStatus**](PayerStatus.md) |  |
**name** | **string** | Payer display name | [optional]
**amount** | **int** | Amount due by the payer expressed in the smallest unit of the currency. |
**payments** | [**\OpenAPI\Client\Model\GetOrderByIdResponsePayment[]**](GetOrderByIdResponsePayment.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
