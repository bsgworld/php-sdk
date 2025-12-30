# # ResendOtp422Response

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **message** | **string** | TwoFA Service error. | [optional] |
| **errors** | **string[]** | It may be one of the following:  - **Authentication failed status**  This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with a ‘failed’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status.  - **Authentication canceled status** This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with a ‘canceled’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status.  - **Authentication expired**   This error can occur when attempting to resend the OTP code for an authentication session that has already been completed with an ‘expired’ status. Resending the OTP code is only possible when the authentication session is in the ‘pending’ status | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
