# # VerifyOtp404Response

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **message** | **string** | TwoFA Service error. | [optional] |
| **errors** | **string[]** | It may be one of the following: - **Authentication not found** - This error can occur when the authentication identifier is specified incorrectly or the specified authentication is not present in the system. Please ensure that you are using the correct authentication identifier and try again. - **The code does not match the expected value** - The error occurs when the provided code does not match the value that was sent to the recipient’s number. | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
