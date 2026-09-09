# GenerateAccessReview200ResponseReport


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | [optional] 
**review_period** | **object** |  | [optional] 
**users** | **List[object]** |  | [optional] 
**summary** | **object** |  | [optional] 
**recommendations** | **List[str]** |  | [optional] 
**generated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.generate_access_review200_response_report import GenerateAccessReview200ResponseReport

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateAccessReview200ResponseReport from a JSON string
generate_access_review200_response_report_instance = GenerateAccessReview200ResponseReport.from_json(json)
# print the JSON string representation of the object
print(GenerateAccessReview200ResponseReport.to_json())

# convert the object into a dict
generate_access_review200_response_report_dict = generate_access_review200_response_report_instance.to_dict()
# create an instance of GenerateAccessReview200ResponseReport from a dict
generate_access_review200_response_report_from_dict = GenerateAccessReview200ResponseReport.from_dict(generate_access_review200_response_report_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


