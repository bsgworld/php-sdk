# # Campaign

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **tariff_code** | **int** | Tariff code null by default. Your can pass specified one if you have several. For more information please visit the [account prices](https://app.bsg.world/prices/sms) | [optional] |
| **validity** | **int** | validity time in hours. The default is 72 hours. Integer from 1 to 72 | [optional] [default to 72] |
| **start_at** | **\DateTime** | Start sending the messages at | [optional] |
| **add_to_contact_book** | **bool** | Specifies whether to add the specified phone number of the message recipient to the contact book | [optional] [default to true] |
| **check_stop_list** | **bool** | Check the recipient’s phone number for being in the stop list.  Possible values:    - true – if the number is found in the stop list, do not send the message  - false – ignore the stop list | [optional] [default to true] |
| **recipients** | [**\BSG\Api\V2\Model\Recipients**](Recipients.md) |  | |
| **channels** | **string[]** |  | |
| **rcs** | [**\BSG\Api\V2\Model\Rcs**](Rcs.md) |  | [optional] |
| **viber** | [**\BSG\Api\V2\Model\Viber**](Viber.md) |  | [optional] |
| **sms** | [**\BSG\Api\V2\Model\Sms**](Sms.md) |  | [optional] |
| **voice** | [**\BSG\Api\V2\Model\Voice**](Voice.md) |  | [optional] |
| **telegram** | [**\BSG\Api\V2\Model\Telegram**](Telegram.md) |  | [optional] |
| **dry_run** | **bool** | Allows you to check the validity of the request without actual campaign sending | [optional] [default to false] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
