# GetPaymentRecords200ResponseDataPagination


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** |  | [optional] 
**limit** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**pages** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_payment_records200_response_data_pagination import GetPaymentRecords200ResponseDataPagination

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentRecords200ResponseDataPagination from a JSON string
get_payment_records200_response_data_pagination_instance = GetPaymentRecords200ResponseDataPagination.from_json(json)
# print the JSON string representation of the object
print(GetPaymentRecords200ResponseDataPagination.to_json())

# convert the object into a dict
get_payment_records200_response_data_pagination_dict = get_payment_records200_response_data_pagination_instance.to_dict()
# create an instance of GetPaymentRecords200ResponseDataPagination from a dict
get_payment_records200_response_data_pagination_from_dict = GetPaymentRecords200ResponseDataPagination.from_dict(get_payment_records200_response_data_pagination_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


