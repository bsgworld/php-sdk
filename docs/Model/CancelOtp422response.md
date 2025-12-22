# # CancelOtp422response

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **message** | **string** | 2FA Service error. | [optional] |
| **errors** | **string[]** | It may be one of the following:  - **Authentication expired** - This error can occur when attempting to cancel an authentication session that is already completed with an “expired” status. It is only possible to cancel an authentication session while it is in the “pending” status.   - **Authentication failed status** - This error can occur when attempting to cancel an authentication session that is already completed with a “failed” status. It is only possible to cancel an authentication session while it is in the “pending” status. | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
