# GetPaymentRecords200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**records** | [**List[GetPaymentRecords200ResponseDataRecordsInner]**](GetPaymentRecords200ResponseDataRecordsInner.md) |  | [optional] 
**pagination** | [**GetPaymentRecords200ResponseDataPagination**](GetPaymentRecords200ResponseDataPagination.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payment_records200_response_data import GetPaymentRecords200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentRecords200ResponseData from a JSON string
get_payment_records200_response_data_instance = GetPaymentRecords200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetPaymentRecords200ResponseData.to_json())

# convert the object into a dict
get_payment_records200_response_data_dict = get_payment_records200_response_data_instance.to_dict()
# create an instance of GetPaymentRecords200ResponseData from a dict
get_payment_records200_response_data_from_dict = GetPaymentRecords200ResponseData.from_dict(get_payment_records200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


