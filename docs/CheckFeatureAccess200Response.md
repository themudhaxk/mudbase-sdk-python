# CheckFeatureAccess200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_access** | **bool** |  | [optional] 
**reason** | **str** |  | [optional] 

## Example

```python
from mudbase.models.check_feature_access200_response import CheckFeatureAccess200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CheckFeatureAccess200Response from a JSON string
check_feature_access200_response_instance = CheckFeatureAccess200Response.from_json(json)
# print the JSON string representation of the object
print(CheckFeatureAccess200Response.to_json())

# convert the object into a dict
check_feature_access200_response_dict = check_feature_access200_response_instance.to_dict()
# create an instance of CheckFeatureAccess200Response from a dict
check_feature_access200_response_from_dict = CheckFeatureAccess200Response.from_dict(check_feature_access200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


