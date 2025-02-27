---
external help file:
Module Name: Az.Monitor
online version: https://learn.microsoft.com/powershell/module/az.monitor/update-azAutoscaleSetting
schema: 2.0.0
---

# Update-AzAutoscaleSetting

## SYNOPSIS
Updates an existing AutoscaleSettingsResource.
To update other fields use the CreateOrUpdate method.

## SYNTAX

### UpdateExpanded (Default)
```
Update-AzAutoscaleSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Enabled <Boolean>] [-Notification <IAutoscaleNotification[]>]
 [-PredictiveAutoscalePolicyScaleLookAheadTime <TimeSpan>]
 [-PredictiveAutoscalePolicyScaleMode <PredictiveAutoscalePolicyScaleMode>] [-Profile <IAutoscaleProfile[]>]
 [-Tag <Hashtable>] [-TargetResourceLocation <String>] [-TargetResourceUri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzAutoscaleSetting -InputObject <IAutoscaleIdentity> [-Enabled <Boolean>]
 [-Notification <IAutoscaleNotification[]>] [-PredictiveAutoscalePolicyScaleLookAheadTime <TimeSpan>]
 [-PredictiveAutoscalePolicyScaleMode <PredictiveAutoscalePolicyScaleMode>] [-Profile <IAutoscaleProfile[]>]
 [-Tag <Hashtable>] [-TargetResourceLocation <String>] [-TargetResourceUri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Updates an existing AutoscaleSettingsResource.
To update other fields use the CreateOrUpdate method.

## EXAMPLES

### Example 1: Update Tag and Enable existing autoscale setting
```powershell
Update-AzAutoscaleSetting -ResourceGroupName test-group -Name test-autoscalesetting -Tag @{'key'='val'} -Enabled $true
```

Update Tag and Enable existing autoscale setting

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled
the enabled flag.
Specifies whether automatic scaling is enabled for the resource.
The default value is 'false'.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Models.IAutoscaleIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
The autoscale setting name.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AutoscaleSettingName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Notification
the collection of notifications.
To construct, see NOTES section for NOTIFICATION properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Models.Api20221001.IAutoscaleNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PredictiveAutoscalePolicyScaleLookAheadTime
the amount of time to specify by which instances are launched in advance.
It must be between 1 minute and 60 minutes in ISO 8601 format.

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PredictiveAutoscalePolicyScaleMode
the predictive autoscale mode

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Support.PredictiveAutoscalePolicyScaleMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
the collection of automatic scaling profiles that specify different scaling parameters for different time periods.
A maximum of 20 profiles can be specified.
To construct, see NOTES section for PROFILE properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Models.Api20221001.IAutoscaleProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group.
The name is case insensitive.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
The ID of the target subscription.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Resource tags

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceLocation
the location of the resource that the autoscale setting should be added to.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceUri
the resource identifier of the resource that the autoscale setting should be added to.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Models.IAutoscaleIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Monitor.Autoscale.Models.Api20221001.IAutoscaleSettingResource

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


`INPUTOBJECT <IAutoscaleIdentity>`: Identity Parameter
  - `[AutoscaleSettingName <String>]`: The autoscale setting name.
  - `[Id <String>]`: Resource identity path
  - `[ResourceGroupName <String>]`: The name of the resource group. The name is case insensitive.
  - `[SubscriptionId <String>]`: The ID of the target subscription.

`NOTIFICATION <IAutoscaleNotification[]>`: the collection of notifications.
  - `[EmailCustomEmail <String[]>]`: the custom e-mails list. This value can be null or empty, in which case this attribute will be ignored.
  - `[EmailSendToSubscriptionAdministrator <Boolean?>]`: a value indicating whether to send email to subscription administrator.
  - `[EmailSendToSubscriptionCoAdministrator <Boolean?>]`: a value indicating whether to send email to subscription co-administrators.
  - `[Webhook <IWebhookNotification[]>]`: the collection of webhook notifications.
    - `[Property <IWebhookNotificationProperties>]`: a property bag of settings. This value can be empty.
      - `[(Any) <String>]`: This indicates any property can be added to this object.
    - `[ServiceUri <String>]`: the service address to receive the notification.

`PROFILE <IAutoscaleProfile[]>`: the collection of automatic scaling profiles that specify different scaling parameters for different time periods. A maximum of 20 profiles can be specified.
  - `CapacityDefault <String>`: the number of instances that will be set if metrics are not available for evaluation. The default is only used if the current instance count is lower than the default.
  - `CapacityMaximum <String>`: the maximum number of instances for the resource. The actual maximum number of instances is limited by the cores that are available in the subscription.
  - `CapacityMinimum <String>`: the minimum number of instances for the resource.
  - `Name <String>`: the name of the profile.
  - `Rule <IScaleRule[]>`: the collection of rules that provide the triggers and parameters for the scaling action. A maximum of 10 rules can be specified.
    - `MetricTriggerMetricName <String>`: the name of the metric that defines what the rule monitors.
    - `MetricTriggerMetricResourceUri <String>`: the resource identifier of the resource the rule monitors.
    - `MetricTriggerOperator <ComparisonOperationType>`: the operator that is used to compare the metric data and the threshold.
    - `MetricTriggerStatistic <MetricStatisticType>`: the metric statistic type. How the metrics from multiple instances are combined.
    - `MetricTriggerThreshold <Double>`: the threshold of the metric that triggers the scale action.
    - `MetricTriggerTimeAggregation <TimeAggregationType>`: time aggregation type. How the data that is collected should be combined over time. The default value is Average.
    - `MetricTriggerTimeGrain <TimeSpan>`: the granularity of metrics the rule monitors. Must be one of the predefined values returned from metric definitions for the metric. Must be between 12 hours and 1 minute.
    - `MetricTriggerTimeWindow <TimeSpan>`: the range of time in which instance data is collected. This value must be greater than the delay in metric collection, which can vary from resource-to-resource. Must be between 12 hours and 5 minutes.
    - `ScaleActionCooldown <TimeSpan>`: the amount of time to wait since the last scaling action before this action occurs. It must be between 1 week and 1 minute in ISO 8601 format.
    - `ScaleActionDirection <ScaleDirection>`: the scale direction. Whether the scaling action increases or decreases the number of instances.
    - `ScaleActionType <ScaleType>`: the type of action that should occur when the scale rule fires.
    - `[MetricTriggerDimension <IScaleRuleMetricDimension[]>]`: List of dimension conditions. For example: [{"DimensionName":"AppName","Operator":"Equals","Values":["App1"]},{"DimensionName":"Deployment","Operator":"Equals","Values":["default"]}].
      - `DimensionName <String>`: Name of the dimension.
      - `Operator <ScaleRuleMetricDimensionOperationType>`: the dimension operator. Only 'Equals' and 'NotEquals' are supported. 'Equals' being equal to any of the values. 'NotEquals' being not equal to all of the values
      - `Value <String[]>`: list of dimension values. For example: ["App1","App2"].
    - `[MetricTriggerDividePerInstance <Boolean?>]`: a value indicating whether metric should divide per instance.
    - `[MetricTriggerMetricNamespace <String>]`: the namespace of the metric that defines what the rule monitors.
    - `[MetricTriggerMetricResourceLocation <String>]`: the location of the resource the rule monitors.
    - `[ScaleActionValue <String>]`: the number of instances that are involved in the scaling action. This value must be 1 or greater. The default value is 1.
  - `[FixedDateEnd <DateTime?>]`: the end time for the profile in ISO 8601 format.
  - `[FixedDateStart <DateTime?>]`: the start time for the profile in ISO 8601 format.
  - `[FixedDateTimeZone <String>]`: the timezone of the start and end times for the profile. Some examples of valid time zones are: Dateline Standard Time, UTC-11, Hawaiian Standard Time, Alaskan Standard Time, Pacific Standard Time (Mexico), Pacific Standard Time, US Mountain Standard Time, Mountain Standard Time (Mexico), Mountain Standard Time, Central America Standard Time, Central Standard Time, Central Standard Time (Mexico), Canada Central Standard Time, SA Pacific Standard Time, Eastern Standard Time, US Eastern Standard Time, Venezuela Standard Time, Paraguay Standard Time, Atlantic Standard Time, Central Brazilian Standard Time, SA Western Standard Time, Pacific SA Standard Time, Newfoundland Standard Time, E. South America Standard Time, Argentina Standard Time, SA Eastern Standard Time, Greenland Standard Time, Montevideo Standard Time, Bahia Standard Time, UTC-02, Mid-Atlantic Standard Time, Azores Standard Time, Cape Verde Standard Time, Morocco Standard Time, UTC, GMT Standard Time, Greenwich Standard Time, W. Europe Standard Time, Central Europe Standard Time, Romance Standard Time, Central European Standard Time, W. Central Africa Standard Time, Namibia Standard Time, Jordan Standard Time, GTB Standard Time, Middle East Standard Time, Egypt Standard Time, Syria Standard Time, E. Europe Standard Time, South Africa Standard Time, FLE Standard Time, Turkey Standard Time, Israel Standard Time, Kaliningrad Standard Time, Libya Standard Time, Arabic Standard Time, Arab Standard Time, Belarus Standard Time, Russian Standard Time, E. Africa Standard Time, Iran Standard Time, Arabian Standard Time, Azerbaijan Standard Time, Russia Time Zone 3, Mauritius Standard Time, Georgian Standard Time, Caucasus Standard Time, Afghanistan Standard Time, West Asia Standard Time, Ekaterinburg Standard Time, Pakistan Standard Time, India Standard Time, Sri Lanka Standard Time, Nepal Standard Time, Central Asia Standard Time, Bangladesh Standard Time, N. Central Asia Standard Time, Myanmar Standard Time, SE Asia Standard Time, North Asia Standard Time, China Standard Time, North Asia East Standard Time, Singapore Standard Time, W. Australia Standard Time, Taipei Standard Time, Ulaanbaatar Standard Time, Tokyo Standard Time, Korea Standard Time, Yakutsk Standard Time, Cen. Australia Standard Time, AUS Central Standard Time, E. Australia Standard Time, AUS Eastern Standard Time, West Pacific Standard Time, Tasmania Standard Time, Magadan Standard Time, Vladivostok Standard Time, Russia Time Zone 10, Central Pacific Standard Time, Russia Time Zone 11, New Zealand Standard Time, UTC+12, Fiji Standard Time, Kamchatka Standard Time, Tonga Standard Time, Samoa Standard Time, Line Islands Standard Time
  - `[RecurrenceFrequency <RecurrenceFrequency?>]`: the recurrence frequency. How often the schedule profile should take effect. This value must be Week, meaning each week will have the same set of profiles. For example, to set a daily schedule, set **schedule** to every day of the week. The frequency property specifies that the schedule is repeated weekly.
  - `[ScheduleDay <String[]>]`: the collection of days that the profile takes effect on. Possible values are Sunday through Saturday.
  - `[ScheduleHour <Int32[]>]`: A collection of hours that the profile takes effect on. Values supported are 0 to 23 on the 24-hour clock (AM/PM times are not supported).
  - `[ScheduleMinute <Int32[]>]`: A collection of minutes at which the profile takes effect at.
  - `[ScheduleTimeZone <String>]`: the timezone for the hours of the profile. Some examples of valid time zones are: Dateline Standard Time, UTC-11, Hawaiian Standard Time, Alaskan Standard Time, Pacific Standard Time (Mexico), Pacific Standard Time, US Mountain Standard Time, Mountain Standard Time (Mexico), Mountain Standard Time, Central America Standard Time, Central Standard Time, Central Standard Time (Mexico), Canada Central Standard Time, SA Pacific Standard Time, Eastern Standard Time, US Eastern Standard Time, Venezuela Standard Time, Paraguay Standard Time, Atlantic Standard Time, Central Brazilian Standard Time, SA Western Standard Time, Pacific SA Standard Time, Newfoundland Standard Time, E. South America Standard Time, Argentina Standard Time, SA Eastern Standard Time, Greenland Standard Time, Montevideo Standard Time, Bahia Standard Time, UTC-02, Mid-Atlantic Standard Time, Azores Standard Time, Cape Verde Standard Time, Morocco Standard Time, UTC, GMT Standard Time, Greenwich Standard Time, W. Europe Standard Time, Central Europe Standard Time, Romance Standard Time, Central European Standard Time, W. Central Africa Standard Time, Namibia Standard Time, Jordan Standard Time, GTB Standard Time, Middle East Standard Time, Egypt Standard Time, Syria Standard Time, E. Europe Standard Time, South Africa Standard Time, FLE Standard Time, Turkey Standard Time, Israel Standard Time, Kaliningrad Standard Time, Libya Standard Time, Arabic Standard Time, Arab Standard Time, Belarus Standard Time, Russian Standard Time, E. Africa Standard Time, Iran Standard Time, Arabian Standard Time, Azerbaijan Standard Time, Russia Time Zone 3, Mauritius Standard Time, Georgian Standard Time, Caucasus Standard Time, Afghanistan Standard Time, West Asia Standard Time, Ekaterinburg Standard Time, Pakistan Standard Time, India Standard Time, Sri Lanka Standard Time, Nepal Standard Time, Central Asia Standard Time, Bangladesh Standard Time, N. Central Asia Standard Time, Myanmar Standard Time, SE Asia Standard Time, North Asia Standard Time, China Standard Time, North Asia East Standard Time, Singapore Standard Time, W. Australia Standard Time, Taipei Standard Time, Ulaanbaatar Standard Time, Tokyo Standard Time, Korea Standard Time, Yakutsk Standard Time, Cen. Australia Standard Time, AUS Central Standard Time, E. Australia Standard Time, AUS Eastern Standard Time, West Pacific Standard Time, Tasmania Standard Time, Magadan Standard Time, Vladivostok Standard Time, Russia Time Zone 10, Central Pacific Standard Time, Russia Time Zone 11, New Zealand Standard Time, UTC+12, Fiji Standard Time, Kamchatka Standard Time, Tonga Standard Time, Samoa Standard Time, Line Islands Standard Time

## RELATED LINKS

