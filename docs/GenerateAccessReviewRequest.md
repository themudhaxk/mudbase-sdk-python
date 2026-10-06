# GenerateAccessReviewRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | 
**review_period** | [**GenerateAccessReviewRequestReviewPeriod**](GenerateAccessReviewRequestReviewPeriod.md) |  | 

## Example

```python
from mudbase.models.generate_access_review_request import GenerateAccessReviewRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateAccessReviewRequest from a JSON string
generate_access_review_request_instance = GenerateAccessReviewRequest.from_json(json)
# print the JSON string representation of the object
print(GenerateAccessReviewRequest.to_json())

# convert the object into a dict
generate_access_review_request_dict = generate_access_review_request_instance.to_dict()
# create an instance of GenerateAccessReviewRequest from a dict
generate_access_review_request_from_dict = GenerateAccessReviewRequest.from_dict(generate_access_review_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


