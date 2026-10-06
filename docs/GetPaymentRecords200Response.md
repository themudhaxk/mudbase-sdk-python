# GetPaymentRecords200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetPaymentRecords200ResponseData**](GetPaymentRecords200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payment_records200_response import GetPaymentRecords200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentRecords200Response from a JSON string
get_payment_records200_response_instance = GetPaymentRecords200Response.from_json(json)
# print the JSON string representation of the object
print(GetPaymentRecords200Response.to_json())

# convert the object into a dict
get_payment_records200_response_dict = get_payment_records200_response_instance.to_dict()
# create an instance of GetPaymentRecords200Response from a dict
get_payment_records200_response_from_dict = GetPaymentRecords200Response.from_dict(get_payment_records200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


