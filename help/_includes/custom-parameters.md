# Custom Parameters field in GGL and MS campaign settings, MS ad group settings, and MS multimedia and responsive ad settings

**[!UICONTROL Custom Parameters]:** (Optional; applicable to audience campaigns only for [!DNL Microsoft Advertising]) Name and value pairs for up to three custom parameters. The maximum length for names is 16 alphanumeric characters; the maximum length for values is 200 characters, including embedded parameters.

You can include your custom parameter names in the tracking templates for the entity and its child entities. When a user clicks a relevant ad, the ad network replaces the parameter name with the defined parameter value. For example, if you create a customer parameter `{_color}=red` and your tracking template includes `http://tracker.example.com/?color={_color}&u={lpurl}`, then "red" is inserted in the color parameter when a user clicks an ad.

Custom parameters at the ad group or ([!DNL Microsoft Advertising] only) ad level override campaign-level
custom parameters with the same name.
