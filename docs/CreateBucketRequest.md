# CreateBucketRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of the bucket | 
**is_public** | **bool** | Whether the bucket is publicly accessible | [optional] [default to False]
**settings** | **object** | Additional bucket settings | [optional] 

## Example

```python
from mudbase.models.create_bucket_request import CreateBucketRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBucketRequest from a JSON string
create_bucket_request_instance = CreateBucketRequest.from_json(json)
# print the JSON string representation of the object
print(CreateBucketRequest.to_json())

# convert the object into a dict
create_bucket_request_dict = create_bucket_request_instance.to_dict()
# create an instance of CreateBucketRequest from a dict
create_bucket_request_from_dict = CreateBucketRequest.from_dict(create_bucket_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


