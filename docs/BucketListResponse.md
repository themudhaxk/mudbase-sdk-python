# BucketListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**buckets** | [**List[Bucket]**](Bucket.md) |  | [optional] 
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 

## Example

```python
from mudbase.models.bucket_list_response import BucketListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BucketListResponse from a JSON string
bucket_list_response_instance = BucketListResponse.from_json(json)
# print the JSON string representation of the object
print(BucketListResponse.to_json())

# convert the object into a dict
bucket_list_response_dict = bucket_list_response_instance.to_dict()
# create an instance of BucketListResponse from a dict
bucket_list_response_from_dict = BucketListResponse.from_dict(bucket_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


