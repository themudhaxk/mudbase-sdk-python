# GetInvoice200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice** | [**GetInvoice200ResponseInvoice**](GetInvoice200ResponseInvoice.md) |  | [optional] 

## Example

```python
from mudbase.models.get_invoice200_response import GetInvoice200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetInvoice200Response from a JSON string
get_invoice200_response_instance = GetInvoice200Response.from_json(json)
# print the JSON string representation of the object
print(GetInvoice200Response.to_json())

# convert the object into a dict
get_invoice200_response_dict = get_invoice200_response_instance.to_dict()
# create an instance of GetInvoice200Response from a dict
get_invoice200_response_from_dict = GetInvoice200Response.from_dict(get_invoice200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


