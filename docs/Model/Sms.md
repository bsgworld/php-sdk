# # Sms

## Properties

| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **sender** | **string** | Sender’s name: from 3 to 11 characters for the sender’s alphanumeric name (Latin letters, symbols, numbers, spaces); 3 to 15 characters for the sender’s numeric name. To setup senders visit the [account](https://app.bsg.world/sms/senders) | |
| **text** | **string** | SMS text, max length is 765 chars for GSM 7-bit encoding (Latin), and 355 for UCS-2 | |
| **unsubscribe_caption** | **string** | Caption before unsubscribe link. Space between caption and link is required. | [optional] |
| **transliterate** | **bool** | apply transliteration to sms text if it necessary | [optional] [default to false] |
| **short_links** | [**\BSG\Api\V2\Model\ShortLink[]**](ShortLink.md) | $shortLinks | [optional] |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
