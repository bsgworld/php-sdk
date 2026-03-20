# # StatJobsCreateRequest

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **type** | **string** | Job creation type | |
| **message_id** | **int[]** | Message Ids | |
| **time_in_from** | **\DateTime** | Datetime when messages were received on the platform | |
| **time_in_to** | **\DateTime** | Datetime when messages were received on the platform | |
| **time_sent_from** | **\DateTime** | Time of sending messages from the platform “from” | [optional] |
| **time_sent_to** | **\DateTime** | Time of sending messages from the platform “to” | [optional] |
| **phones** | **int[]** | phone list | [optional] |
| **sender** | **string** | Source from where the message came to the platform | [optional] |
| **source** | **string** | Source from where the message came to the platform | [optional] |
| **country** | **string** | The name of the country for search | [optional] |
| **operator_id** | **string** | Indication of the country operator | [optional] |
| **status** | **string** | The status of the messages to display | [optional] |
| **sl_clicks** | **string** | The field is available only to the clients who have enabled Short URL service | [optional] |
| **sl_clicks_comp** | **string** | Comparison operator with the clicks count value | [optional] |
| **sl_clicks_count** | **string** | Comparison operator with the clicks count value | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
