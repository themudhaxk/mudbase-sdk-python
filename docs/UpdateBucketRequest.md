# UpdateBucketRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Updated name of the bucket | [optional] 
**is_public** | **bool** | Update whether the bucket is publicly accessible | [optional] 
**settings** | **object** | Updated bucket settings | [optional] 

## Example

```python
from mudbase.models.update_bucket_request import UpdateBucketRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateBucketRequest from a JSON string
update_bucket_request_instance = UpdateBucketRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateBucketRequest.to_json())

# convert the object into a dict
update_bucket_request_dict = update_bucket_request_instance.to_dict()
# create an instance of UpdateBucketRequest from a dict
update_bucket_request_from_dict = UpdateBucketRequest.from_dict(update_bucket_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


