# BucketResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**bucket** | [**Bucket**](Bucket.md) |  | [optional] 

## Example

```python
from mudbase.models.bucket_response import BucketResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BucketResponse from a JSON string
bucket_response_instance = BucketResponse.from_json(json)
# print the JSON string representation of the object
print(BucketResponse.to_json())

# convert the object into a dict
bucket_response_dict = bucket_response_instance.to_dict()
# create an instance of BucketResponse from a dict
bucket_response_from_dict = BucketResponse.from_dict(bucket_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


