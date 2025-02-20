---
title: "schedule resource type"
description: "A collection of schedulingGroups, shifts, timeOffReasons and timesOff within a team."
author: "akumar39"
ms.localizationpriority: medium
ms.subservice: "teams"
doc_type: resourcePageType_
ms.date: 07/22/2024
---

# schedule resource type

Namespace: microsoft.graph

A collection of [schedulingGroup](schedulinggroup.md) objects, [shift](shift.md) objects, [timeOffReason](timeoffreason.md) objects, and [timeOff](timeoff.md) objects within a [team](../resources/team.md). 

## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[Create or replace](../api/team-put-schedule.md) | [schedule](schedule.md) | Create or replace a schedule.|
|[Get](../api/schedule-get.md) | [schedule](schedule.md) | Get a schedule.|
|[Share](../api/schedule-share.md) | None | Share a schedule time range with schedule members.|

## Properties
|Name                   |Type           |Description                                                                                                                                      |
|-----------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled 			    |Boolean    | Indicates whether the schedule is enabled for the team. Required.|
| id			        |string  |ID of the schedule.|
| offerShiftRequestsEnabled			        |Boolean  | Indicates whether offer shift requests are enabled for the schedule.             |
| openShiftsEnabled			        |Boolean  | Indicates whether open shifts are enabled for the schedule.             | 
| provisionStatus       |operationStatus    | The status of the schedule provisioning. The possible values are `notStarted`, `running`, `completed`, `failed`. |
| provisionStatusCode   |string  | Additional information about why schedule provisioning failed. |
| swapShiftsRequestsEnabled			        |Boolean| Indicates whether swap shifts requests are enabled for the schedule.             |
| timeClockEnabled			        |Boolean  | Indicates whether time clock is enabled for the schedule.             |
| timeOffRequestsEnabled			        |Boolean | Indicates whether time off requests are enabled for the schedule.             | 
| timeZone 		        |string  | Indicates the time zone of the schedule team using tz database format. Required.|


## Relationships
|Name                   |Type           |Description                                                                                                                                      |
|-----------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| offerShiftRequests   |[offerShiftRequest](offershiftrequest.md) collection  | The offer requests for shifts in the schedule. |
| openShiftChangeRequests   |[openShiftChangeRequest](openshiftchangerequest.md) collection  | The open shift requests in the schedule. |
| openShifts   |[openShift](openshift.md) collection | The set of open shifts in a scheduling group in the schedule. |
| schedulingGroups   |[schedulingGroup](schedulinggroup.md) collection  | The logical grouping of users in the schedule (usually by role). |
| shifts   | [shift](shift.md) collection  | The shifts in the schedule. |
| swapShiftsChangeRequests   |[swapShiftsChangeRequest](swapshiftschangerequest.md) collection  | The swap requests for shifts in the schedule. |
| timesOff   |[timeOff](timeoff.md) collection  | The instances of times off in the schedule. |
| timeOffReasons   |[timeOffReason](timeoffreason.md) collection  | The set of reasons for a time off in the schedule. |
| timeOffRequests   |[timeOffRequest](timeoffrequest.md) collection  | The time off requests in the schedule. |
| workforceIntegrations   |[workforceIntegration](workforceintegration.md) collection  | An instance of a workforce integration per team with outbound data flow on synchronous change notifications (for supported entities). |

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.schedule"
}-->

```json
{
  "id": "833fc4df-c88b-4398-992f-d8afcfe41df2",
  "enabled": true,
  "timeZone": "America/Chicago",
  "provisionStatus": "Completed",
  "provisionStatusCode": null
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "schedule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

