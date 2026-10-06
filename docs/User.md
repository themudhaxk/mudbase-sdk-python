# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**full_name** | **str** |  | [optional] 
**avatar** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**custom_role** | **str** | Application-level role slug from the project&#39;s Multi-Role feature (e.g. \&quot;customer\&quot;, \&quot;seller\&quot;). Null for org-level (org/admin/member/viewer) users who aren&#39;t project end-users. | [optional] 
**is_anonymous** | **bool** | True for a guest session created via POST /api/auth/anonymous that hasn&#39;t been converted to a full account yet. | [optional] 
**email_verified** | **bool** |  | [optional] 
**phone_verified** | **bool** |  | [optional] 
**two_factor_enabled** | **bool** |  | [optional] 
**last_login** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**org** | [**OrganizationSummary**](OrganizationSummary.md) |  | [optional] 

## Example

```python
from mudbase.models.user import User

# TODO update the JSON string below
json = "{}"
# create an instance of User from a JSON string
user_instance = User.from_json(json)
# print the JSON string representation of the object
print(User.to_json())

# convert the object into a dict
user_dict = user_instance.to_dict()
# create an instance of User from a dict
user_from_dict = User.from_dict(user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


