# # SendOtp422Response

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **message** | **string** | The given data was invalid. | [optional] |
| **errors** | **string[]** | It may be one of the following:  - **User channel not found**  This error can occur when the channel is specified incorrectly. Please ensure that you are using the correct channel and try again.  - **Template not found**  This error can occur when the template identifier is specified incorrectly or the specified template is not present in the system. Please ensure that you are using the correct template identifier and try again.  - **Invalid template status**  This error occurs when the provided template identifier in the request does not match the “Approved” status.  - **Insufficient funds**  Insufficient funds to send OTP. Please top up your account.  - **Exists on the stop list**  We’re unable to send message as the phone number of recipient is currently in stop list.  - **User channel inactive**  The message sending method is disabled. Please enable method in your personal account and try again.  - **This action is available for the account of your type only for your manager phone number.**  To send OTP code is not allowed in Demo account mode.   - **Authentication limit with status pending**  This error can occur when total authentication limit with status “pending” is exceeded for your account.  - **Total authentication limit**  This error can occur when total authentication limit is exceeded for your account.  - **Template is not available** This error occurs when you try to create authentication using a template that is only available in the test mode of your account. Please choose a different template. | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
