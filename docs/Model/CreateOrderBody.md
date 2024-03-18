# # CreateOrderBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**\OpenAPI\Client\Model\OrderType**](OrderType.md) |  |
**amount** | **int** | Total amount of the order expressed in the smallest unit of the currency. |
**currency** | [**\OpenAPI\Client\Model\Currency**](Currency.md) |  |
**sellerOrderId** | **string** | The ID of the order in the seller&#39;s system | [optional]
**redirectUrl** | **string** | URL on your website to redirect the payer to after a successful payment. | [optional]
**duration** | **int** | Maximum duration of the order in milliseconds. | [optional]
**email** | **string** | The email of the owner payer. Only working in single_payer mode. | [optional]
**phoneNumber** | **string** | The email of the owner payer. Only working in single_payer mode. | [optional]
**defaultLocale** | [**\OpenAPI\Client\Model\SupportedLocale**](SupportedLocale.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
