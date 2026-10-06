# CreateOrUpdateFeeSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | 
**enabled** | **bool** |  | [optional] 
**fee_amount** | **float** |  | [optional] 
**payout_address** | **str** |  | [optional] 
**payout_threshold** | **float** |  | [optional] 

## Example

```python
from mudbase.models.create_or_update_fee_settings_request import CreateOrUpdateFeeSettingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrUpdateFeeSettingsRequest from a JSON string
create_or_update_fee_settings_request_instance = CreateOrUpdateFeeSettingsRequest.from_json(json)
# print the JSON string representation of the object
print(CreateOrUpdateFeeSettingsRequest.to_json())

# convert the object into a dict
create_or_update_fee_settings_request_dict = create_or_update_fee_settings_request_instance.to_dict()
# create an instance of CreateOrUpdateFeeSettingsRequest from a dict
create_or_update_fee_settings_request_from_dict = CreateOrUpdateFeeSettingsRequest.from_dict(create_or_update_fee_settings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


