# GetInvoices200ResponseInvoicesInner


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
**hosted_invoice_url** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_invoices200_response_invoices_inner import GetInvoices200ResponseInvoicesInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetInvoices200ResponseInvoicesInner from a JSON string
get_invoices200_response_invoices_inner_instance = GetInvoices200ResponseInvoicesInner.from_json(json)
# print the JSON string representation of the object
print(GetInvoices200ResponseInvoicesInner.to_json())

# convert the object into a dict
get_invoices200_response_invoices_inner_dict = get_invoices200_response_invoices_inner_instance.to_dict()
# create an instance of GetInvoices200ResponseInvoicesInner from a dict
get_invoices200_response_invoices_inner_from_dict = GetInvoices200ResponseInvoicesInner.from_dict(get_invoices200_response_invoices_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


