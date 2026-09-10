# InitializePayment200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link** | **str** |  | [optional] 
**tx_ref** | **str** |  | [optional] 
**provider_ref** | **str** |  | [optional] 
**amount** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**org_receives** | **float** |  | [optional] 
**platform_percent** | **float** |  | [optional] 
**platform_fixed** | **float** |  | [optional] 

## Example

```python
from mudbase.models.initialize_payment200_response_data import InitializePayment200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of InitializePayment200ResponseData from a JSON string
initialize_payment200_response_data_instance = InitializePayment200ResponseData.from_json(json)
# print the JSON string representation of the object
print(InitializePayment200ResponseData.to_json())

# convert the object into a dict
initialize_payment200_response_data_dict = initialize_payment200_response_data_instance.to_dict()
# create an instance of InitializePayment200ResponseData from a dict
initialize_payment200_response_data_from_dict = InitializePayment200ResponseData.from_dict(initialize_payment200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


