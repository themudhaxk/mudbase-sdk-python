# FeatureNotAllowedError

Returned when an app-role feature gate denies access (HTTP 403)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**error** | **str** |  | 
**resource** | **str** |  | [optional] 
**action** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from mudbase.models.feature_not_allowed_error import FeatureNotAllowedError

# TODO update the JSON string below
json = "{}"
# create an instance of FeatureNotAllowedError from a JSON string
feature_not_allowed_error_instance = FeatureNotAllowedError.from_json(json)
# print the JSON string representation of the object
print(FeatureNotAllowedError.to_json())

# convert the object into a dict
feature_not_allowed_error_dict = feature_not_allowed_error_instance.to_dict()
# create an instance of FeatureNotAllowedError from a dict
feature_not_allowed_error_from_dict = FeatureNotAllowedError.from_dict(feature_not_allowed_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


