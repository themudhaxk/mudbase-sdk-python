# RequestManualPayoutRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | 

## Example

```python
from mudbase.models.request_manual_payout_request import RequestManualPayoutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RequestManualPayoutRequest from a JSON string
request_manual_payout_request_instance = RequestManualPayoutRequest.from_json(json)
# print the JSON string representation of the object
print(RequestManualPayoutRequest.to_json())

# convert the object into a dict
request_manual_payout_request_dict = request_manual_payout_request_instance.to_dict()
# create an instance of RequestManualPayoutRequest from a dict
request_manual_payout_request_from_dict = RequestManualPayoutRequest.from_dict(request_manual_payout_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


