# GetInvoice200ResponseInvoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**invoice_number** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**total** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**due_date** | **datetime** |  | [optional] 
**paid_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_invoice200_response_invoice import GetInvoice200ResponseInvoice

# TODO update the JSON string below
json = "{}"
# create an instance of GetInvoice200ResponseInvoice from a JSON string
get_invoice200_response_invoice_instance = GetInvoice200ResponseInvoice.from_json(json)
# print the JSON string representation of the object
print(GetInvoice200ResponseInvoice.to_json())

# convert the object into a dict
get_invoice200_response_invoice_dict = get_invoice200_response_invoice_instance.to_dict()
# create an instance of GetInvoice200ResponseInvoice from a dict
get_invoice200_response_invoice_from_dict = GetInvoice200ResponseInvoice.from_dict(get_invoice200_response_invoice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


