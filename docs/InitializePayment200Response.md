# InitializePayment200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**InitializePayment200ResponseData**](InitializePayment200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.initialize_payment200_response import InitializePayment200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitializePayment200Response from a JSON string
initialize_payment200_response_instance = InitializePayment200Response.from_json(json)
# print the JSON string representation of the object
print(InitializePayment200Response.to_json())

# convert the object into a dict
initialize_payment200_response_dict = initialize_payment200_response_instance.to_dict()
# create an instance of InitializePayment200Response from a dict
initialize_payment200_response_from_dict = InitializePayment200Response.from_dict(initialize_payment200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


