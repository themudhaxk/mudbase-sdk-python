# EmailRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | [**EmailRequestTo**](EmailRequestTo.md) |  | 
**subject** | **str** |  | 
**html** | **str** |  | [optional] 
**text** | **str** |  | [optional] 
**template_id** | **str** |  | [optional] 
**template_data** | **object** |  | [optional] 

## Example

```python
from mudbase.models.email_request import EmailRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EmailRequest from a JSON string
email_request_instance = EmailRequest.from_json(json)
# print the JSON string representation of the object
print(EmailRequest.to_json())

# convert the object into a dict
email_request_dict = email_request_instance.to_dict()
# create an instance of EmailRequest from a dict
email_request_from_dict = EmailRequest.from_dict(email_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


