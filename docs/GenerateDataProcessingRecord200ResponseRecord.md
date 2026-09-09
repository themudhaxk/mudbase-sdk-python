# GenerateDataProcessingRecord200ResponseRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | [optional] 
**record_date** | **datetime** |  | [optional] 
**data_controller** | **object** |  | [optional] 
**processing_activities** | **List[object]** |  | [optional] 
**data_subjects** | **List[str]** |  | [optional] 
**generated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.generate_data_processing_record200_response_record import GenerateDataProcessingRecord200ResponseRecord

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateDataProcessingRecord200ResponseRecord from a JSON string
generate_data_processing_record200_response_record_instance = GenerateDataProcessingRecord200ResponseRecord.from_json(json)
# print the JSON string representation of the object
print(GenerateDataProcessingRecord200ResponseRecord.to_json())

# convert the object into a dict
generate_data_processing_record200_response_record_dict = generate_data_processing_record200_response_record_instance.to_dict()
# create an instance of GenerateDataProcessingRecord200ResponseRecord from a dict
generate_data_processing_record200_response_record_from_dict = GenerateDataProcessingRecord200ResponseRecord.from_dict(generate_data_processing_record200_response_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


