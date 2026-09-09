# GetProjectEmailSmtp200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**ProjectSmtpSettingsPublic**](ProjectSmtpSettingsPublic.md) |  | [optional] 

## Example

```python
from mudbase.models.get_project_email_smtp200_response import GetProjectEmailSmtp200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectEmailSmtp200Response from a JSON string
get_project_email_smtp200_response_instance = GetProjectEmailSmtp200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectEmailSmtp200Response.to_json())

# convert the object into a dict
get_project_email_smtp200_response_dict = get_project_email_smtp200_response_instance.to_dict()
# create an instance of GetProjectEmailSmtp200Response from a dict
get_project_email_smtp200_response_from_dict = GetProjectEmailSmtp200Response.from_dict(get_project_email_smtp200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


