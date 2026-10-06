# TestWebhookTransformationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payload** | **object** | Sample payload to transform | 
**transformations** | [**List[GetWebhookConfig200ResponseDataTransformationsInner]**](GetWebhookConfig200ResponseDataTransformationsInner.md) | Transformation rules to apply | 

## Example

```python
from mudbase.models.test_webhook_transformation_request import TestWebhookTransformationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TestWebhookTransformationRequest from a JSON string
test_webhook_transformation_request_instance = TestWebhookTransformationRequest.from_json(json)
# print the JSON string representation of the object
print(TestWebhookTransformationRequest.to_json())

# convert the object into a dict
test_webhook_transformation_request_dict = test_webhook_transformation_request_instance.to_dict()
# create an instance of TestWebhookTransformationRequest from a dict
test_webhook_transformation_request_from_dict = TestWebhookTransformationRequest.from_dict(test_webhook_transformation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


