---
title: FieldURI
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FieldURI
api_type:
- schema
ms.assetid: 24af8e3b-3074-4c8c-8d0a-52446508d044
description: Das FieldURI-Element identifiziert Eigenschaften, auf die häufig vom URI verwiesen wird.
ms.openlocfilehash: 9e343941e77a271d817ef193b74dec9104646f71
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530627"
---
# <a name="fielduri"></a>FieldURI

Das **FieldURI**-Element identifiziert Eigenschaften, auf die häufig vom URI verwiesen wird. 
  
```XML
<FieldURI FieldURI="" />
```

 **PathToUnindexedFieldType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**FieldURI** <br/> |Identifiziert den URI der Eigenschaft.  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI Attribute

|**Wert**|**Beschreibung**|
|:-----|:-----|
|folder:FolderId  <br/> |Identifies the **FolderId** property.  <br/> |
|folder:ParentFolderId  <br/> |Identifies the **ParentFolderId** property.  <br/> |
|folder:DisplayName  <br/> |Identifies the **DisplayName** property.  <br/> |
|folder:UnreadCount  <br/> |Identifies the **UnreadCount** property.  <br/> |
|folder:TotalCount  <br/> |Identifies the **TotalCount** property.  <br/> |
|folder:ChildFolderCount  <br/> |Identifies the **ChildFolderCount** property.  <br/> |
|folder:FolderClass  <br/> |Identifies the **FolderClass** property.  <br/> |
|folder:SearchParameters  <br/> |Identifies the **SearchParameters** property.  <br/> |
|folder:ManagedFolderInformation  <br/> |Identifies the **ManagedFolderInformation** property.  <br/> |
|folder:PermissionSet  <br/> |Identifies the **PermissionSet** property.  <br/> |
|folder:EffectiveRights  <br/> |Identifies the **EffectiveRights** property.  <br/> |
|folder:SharingEffectiveRights  <br/> |Identifies the **SharingEffectiveRights** property.  <br/> |
|item:ItemId  <br/> |Identifies the **ItemId** property.  <br/> |
|item:ParentFolderId  <br/> |Identifies the **ParentFolderId** property.  <br/> |
|item:ItemClass  <br/> |Identifies the **ItemClass** property.  <br/> |
|item:MimeContent  <br/> |Identifies the **MimeContent** property.  <br/> |
|item:Attachments  <br/> |Identifies the **Attachments** property.  <br/> |
|item:Subject  <br/> |Identifies the **Subject** property.  <br/> |
|item:DateTimeReceived  <br/> |Identifies the **DateTimeReceived** property.  <br/> |
|item:Size  <br/> |Identifies the **Size** property.  <br/> |
|item:Categories  <br/> |Identifies the **Categories** property.  <br/> |
|item:HasAttachments  <br/> |Identifies the **HasAttachments** property.  <br/> |
|item:Importance  <br/> |Identifies the **Importance** property.  <br/> |
|item:InReplyTo  <br/> |Identifies the **InReplyTo** property.  <br/> |
|item:InternetMessageHeaders  <br/> |Identifies the **InternetMessageHeaders** property.  <br/> |
|item:IsAssociated  <br/> |Identifies the **IsAssociated** property.  <br/> |
|item:IsDraft  <br/> |Identifies the **IsDraft** property.  <br/> |
|item:IsFromMe  <br/> |Identifies the **IsFromMe** property.  <br/> |
|item:IsResend  <br/> |Identifies the **IsResend** property.  <br/> |
|item:IsSubmitted  <br/> |Identifies the **IsSubmitted** property.  <br/> |
|item:IsUnmodified  <br/> |Identifies the **IsUnmodified** property.  <br/> |
|item:DateTimeSent  <br/> |Identifies the **DateTimeSent** property.  <br/> |
|item:DateTimeCreated  <br/> |Identifies the **DateTimeCreated** property.  <br/> |
|item:Body  <br/> |Identifies the **Body** property.  <br/> |
|item:ResponseObjects  <br/> |Identifies the **ResponseObjects** property.  <br/> |
|item:Sensitivity  <br/> |Identifies the **Sensitivity** property.  <br/> |
|item:ReminderDueBy  <br/> |Identifies the **ReminderDueBy** property.  <br/> |
|item:ReminderIsSet  <br/> |Identifies the **ReminderIsSet** property.  <br/> |
|item:ReminderNextTime  <br/> |Identifies the **ReminderNextTime** property.  <br/> |
|item:ReminderMinutesBeforeStart  <br/> |Identifies the **ReminderMinutesBeforeStart** property.  <br/> |
|item:DisplayTo  <br/> |Identifies the **DisplayTo** property.  <br/> |
|item:DisplayCc  <br/> |Identifies the **DisplayCc** property.  <br/> |
|item:Culture  <br/> |Identifies the **Culture** property.  <br/> |
|item:EffectiveRights  <br/> |Identifies the **EffectiveRights** property.  <br/> |
|item:LastModifiedName  <br/> |Identifies the **LastModifiedName** property.  <br/> |
|item:LastModifiedTime  <br/> |Identifies the **LastModifiedTime** property.  <br/> |
|item:ConversationId  <br/> |Identifies the **ConversationId** property.  <br/> |
|item:UniqueBody  <br/> |Identifies the **UniqueBody** property.  <br/> |
|item:Flag  <br/> |Identifies the **Flag** property.  <br/> |
|item:StoreEntryId  <br/> |Identifies the **StoreEntryId** property.  <br/> |
|item:InstanceKey  <br/> |Identifies the **InstanceKey** property.  <br/> |
|item:NormalizedBody  <br/> |Identifies the **NormalizedBody** property.  <br/> |
|item:EntityExtractionResult  <br/> |Identifies the **EntityExtractionResult** property.  <br/> |
|itemPolicyTag  <br/> |Idnentifies the **PolicyTag** property.  <br/> |
|item:ArchiveTag  <br/> |Identifies the **ArchiveTag** property.  <br/> |
|item:RetentionDate  <br/> |Identifies the **RetentionDate** property.  <br/> |
|item:Preview  <br/> |Identifies the **Preview** property.  <br/> |
|item:NextPredictedAction  <br/> |Identifies the **NextPredictedAction** property.  <br/> |
|item:GroupingAction  <br/> |Identifies the **GroupingAction** property.  <br/> |
|item:PredictedActionReasons  <br/> |Identifies the **PredictedActionReasons** property  <br/> |
|item:IsClutter  <br/> |Intended for internal use only.  <br/> |
|item:RightsManagementLicenseData  <br/> |Identifies the **RightsManagementLicenseData** property.  <br/> |
|item:BlockStatus  <br/> |Identifies the **BlockStatus** property.  <br/> |
|item:HasBlockedImages  <br/> |Identifies the **HasBlockedImages** property.  <br/> |
|item:WebClientReadFormQueryString  <br/> |Identifies the **WebClientReadFormQueryString** property.  <br/> |
|item:WebClientEditFormQueryString  <br/> |Identifies the **WebClientEditFormQueryString** property.  <br/> |
|item:TextBody  <br/> |Identifies the **TextBody** property.  <br/> |
|item:IconIndex  <br/> |Identifies the **IconIndex** property.  <br/> |
|item:MimeContentUTF8  <br/> |Identifies the **MimeContentUTF8** property.  <br/> |
|message:ConversationIndex  <br/> |Identifies the **ConversationIndex** property.  <br/> |
|message:ConversationTopic  <br/> |Identifies the **ConversationTopic** property.  <br/> |
|message:InternetMessageId  <br/> |Identifies the **InternetMessageId** property.  <br/> |
|message:IsRead  <br/> |Identifies the **IsRead** property.  <br/> |
|message:IsResponseRequested  <br/> |Identifies the **IsResponseRequested** property.  <br/> |
|message:IsReadReceiptRequested  <br/> |Identifies the **IsReadReceiptRequested** property.  <br/> |
|message:IsDeliveryReceiptRequested  <br/> |Identifies the **IsDeliveryReceiptRequested** property.  <br/> |
|message:ReceivedBy  <br/> |Identifies the **ReceivedBy** property.  <br/> |
|message:ReceivedRepresenting  <br/> |Identifies the **ReceivedRepresenting** property.  <br/> |
|message:References  <br/> |Identifies the **References** property.  <br/> |
|message:ReplyTo  <br/> |Identifies the **ReplyTo** property.  <br/> |
|message:From  <br/> |Identifies the **From** property.  <br/> |
|message:Sender  <br/> |Identifies the **Sender** property.  <br/> |
|message:ToRecipients  <br/> |Identifies the **ToRecipients** property.  <br/> |
|message:CcRecipients  <br/> |Identifies the **CcRecipients** property.  <br/> |
|message:BccRecipients  <br/> |Identifies the **BccRecipients** property.  <br/> |
|message:ApprovalRequestData  <br/> |Identifies the **ApprovalRequestData** property.  <br/> |
|message:VotingInformation  <br/> |Identifies the **VotingInformation** property.  <br/> |
|message:ReminderMessageData  <br/> |Identifies the **ReminderMessageData** property.  <br/> |
|meeting:AssociatedCalendarItemId  <br/> |Identifies the **AssociatedCalendarItemId** property.  <br/> |
|meeting:IsDelegated  <br/> |Identifies the **IsDelegated** property.  <br/> |
|meeting:IsOutOfDate  <br/> |Identifies the **IsOutOfDate** property.  <br/> |
|meeting:HasBeenProcessed  <br/> |Identifies the **HasBeenProcessed** property.  <br/> |
|meeting:ResponseType  <br/> |Identifies the **ResponseType** property.  <br/> |
|meeting:ProposedStart  <br/> |Identifies the **ProposedStart** property.  <br/> |
|meeting:PropsedEnd  <br/> |Identifies the **ProposedEnd** property.  <br/> |
|meetingRequest:MeetingRequestType  <br/> |Identifies the **MeetingRequestType** property.  <br/> |
|meetingRequest:IntendedFreeBusyStatus  <br/> |Identifies the **IntendedFreeBusyStatus** property.  <br/> |
|meetingRequest:ChangeHighlights  <br/> |Identifies the **ChangeHighlights** property.  <br/> |
|calendar:Start  <br/> |Identifies the **Start** property.  <br/> |
|calendar:End  <br/> |Identifies the **End** property.  <br/> |
|calendar:OriginalStart  <br/> |Identifies the **OriginalStart** property.  <br/> |
|calendar:StartWallClock  <br/> |Identifies the **StartWallClock** property.  <br/> |
|calendar:EndWallClock  <br/> |Identifies the **EndWallClock** property.  <br/> |
|calendar:StartTimeZoneId  <br/> |Identifies the **StartTimeZoneId** property.  <br/> |
|calendar:EndTimeZoneId  <br/> |Identifies the **EndTimeZoneId** property.  <br/> |
|calendar:IsAllDayEvent  <br/> |Identifies the **IsAllDayEvent** property.  <br/> |
|calendar:LegacyFreeBusyStatus  <br/> |Identifies the **LegacyFreeBusyStatus** property.  <br/> |
|calendar:Location  <br/> |Identifies the **Location** property.  <br/> |
|calendar:When  <br/> |Identifies the **When** property.  <br/> |
|calendar:IsMeeting  <br/> |Identifies the **IsMeeting** property.  <br/> |
|calendar:IsCancelled  <br/> |Identifies the **IsCancelled** property.  <br/> |
|calendar:IsRecurring  <br/> |Identifies the **IsRecurring** property.  <br/> |
|calendar:MeetingRequestWasSent  <br/> |Identifies the **MeetingRequestWasSent** property.  <br/> |
|calendar:IsResponseRequested  <br/> |Identifies the **IsResponseRequested** property.  <br/> |
|calendar:CalendarItemType  <br/> |Identifies the **CalendarItemType** property.  <br/> |
|calendar:MyResponseType  <br/> |Identifies the **MyResponseType** property.  <br/> |
|calendar:Organizer  <br/> |Identifies the **Organizer** property.  <br/> |
|calendar:RequiredAttendees  <br/> |Identifies the **RequiredAttendees** property.  <br/> |
|calendar:OptionalAttendees  <br/> |Identifies the **OptionalAttendees** property.  <br/> |
|calendar:Resources  <br/> |Identifies the **Resources** property.  <br/> |
|calendar:ConflictingMeetingCount  <br/> |Identifies the **ConflictingMeetingCount** property.  <br/> |
|calendar:AdjacentMeetingCount  <br/> |Identifies the **AdjacentMeetingCount** property.  <br/> |
|calendar:ConflictingMeetings  <br/> |Identifies the **ConflictingMeetings** property.  <br/> |
|calendar:AdjacentMeetings  <br/> |Identifies the **AdjacentMeetings** property.  <br/> |
|calendar:Duration  <br/> |Identifies the **Duration** property.  <br/> |
|calendar:TimeZone  <br/> |Identifies the **TimeZone** property.  <br/> |
|calendar:AppointmentReplyTime  <br/> |Identifies the **AppointmentReplyTime** property.  <br/> |
|calendar:AppointmentSequenceNumber  <br/> |Identifies the **AppointmentSequenceNumber** property.  <br/> |
|calendar:AppointmentState  <br/> |Identifies the **AppointmentState** property.  <br/> |
|calendar:Recurrence  <br/> |Identifies the **Recurrence** property.  <br/> |
|calendar:FirstOccurrence  <br/> |Identifies the **FirstOccurrence** property.  <br/> |
|calendar:LastOccurrence  <br/> |Identifies the **LastOccurrence** property.  <br/> |
|calendar:ModifiedOccurrences  <br/> |Identifies the **ModifiedOccurrences** property.  <br/> |
|calendar:DeletedOccurrences  <br/> |Identifies the **DeletedOccurrences** property.  <br/> |
|calendar:MeetingTimeZone  <br/> |Identifies the **MeetingTimeZone** property.  <br/> |
|calendar:ConferenceType  <br/> |Identifies the **ConferenceType** property.  <br/> |
|calendar:AllowNewTimeProposal  <br/> |Identifies the **AllowNewTimeProposal** property.  <br/> |
|calendar:IsOnlineMeeting  <br/> |Identifies the **IsOnlineMeeting** property.  <br/> |
|calendar:MeetingWorkspaceUrl  <br/> |Identifies the **MeetingWorkspaceUrl** property.  <br/> |
|calendar:NetShowUrl  <br/> |Identifies the **NetShowUrl** property.  <br/> |
|calendar:UID  <br/> |Identifies the **UID** property.  <br/> |
|calendar:RecurrenceId  <br/> |Identifies the **RecurrenceId** property.  <br/> |
|calendar:DateTimeStamp  <br/> |Identifies the **DateTimeStamp** property.  <br/> |
|calendar:StartTimeZone  <br/> |Identifies the **StartTimeZone** property.  <br/> |
|calendar:EndTimeZone  <br/> |Identifies the **EndTimeZone** property.  <br/> |
|calendar:JoinOnlineMeetingUrl  <br/> |Identifies the **JoinOnlineMeetingUrl** property.  <br/> |
|calendar:OnlineMeetingSettings  <br/> |Identifies the **OnlineMeetingSettings** property.  <br/> |
|calendar:IsOrganizer  <br/> |Identifies the **IsOrganizer** property.  <br/> |
|task:ActualWork  <br/> |Identifies the **ActualWork** property.  <br/> |
|task:AssignedTime  <br/> |Identifies the **AssignedTime** property.  <br/> |
|task:BillingInformation  <br/> |Identifies the **BillingInformation** property.  <br/> |
|task:ChangeCount  <br/> |Identifies the **ChangeCount** property.  <br/> |
|task:Companies  <br/> |Identifies the **Companies** property.  <br/> |
|task:CompleteDate  <br/> |Identifies the **CompleteDate** property.  <br/> |
|task:Contacts  <br/> |Identifies the **Contacts** property.  <br/> |
|task:DelegationState  <br/> |Identifies the **DelegationState** property.  <br/> |
|task:Delegator  <br/> |Identifies the **Delegator** property.  <br/> |
|task:DueDate  <br/> |Identifies the **DueDate** property.  <br/> |
|task:IsAssignmentEditable  <br/> |Identifies the **IsAssignmentEditable** property.  <br/> |
|task:IsComplete  <br/> |Identifies the **IsComplete** property.  <br/> |
|task:IsRecurring  <br/> |Identifies the **IsRecurring** property.  <br/> |
|task:IsTeamTask  <br/> |Identifies the **IsTeamTask** property.  <br/> |
|task:Mileage  <br/> |Identifies the **Mileage** property.  <br/> |
|task:Owner  <br/> |Identifies the **Owner** property.  <br/> |
|task:PercentComplete  <br/> |Identifies the **PercentComplete** property.  <br/> |
|task:Recurrence  <br/> |Identifies the **Recurrence** property.  <br/> |
|task:StartDate  <br/> |Identifies the **StartDate** property.  <br/> |
|task:Status  <br/> |Identifies the **Status** property.  <br/> |
|task:StatusDescription  <br/> |Identifies the **StatusDescription** property.  <br/> |
|task:TotalWork  <br/> |Identifies the **TotalWork** property.  <br/> |
|contacts:Alias  <br/> |Identifies the **Alias** property. This property was introduced in Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|contacts:AssistantName  <br/> |Identifies the **AssistantName** property.  <br/> |
|contacts:Birthday  <br/> |Identifies the **Birthday** property.  <br/> |
|contacts:BusinessHomePage  <br/> |Identifies the **BusinessHomePage** property.  <br/> |
|contacts:Children  <br/> |Identifies the **Children** property.  <br/> |
|contacts:Companies  <br/> |Identifies the **Companies** property.  <br/> |
|contacts:CompanyName  <br/> |Identifies the **CompanyName** property.  <br/> |
|contacts:CompleteName  <br/> |Identifies the **CompleteName** property.  <br/> |
|contacts:ContactSource  <br/> |Identifies the **ContactSource** property.  <br/> |
|contacts:Culture  <br/> |Identifies the **Culture** property.  <br/> |
|contacts:Department  <br/> |Identifies the **Department** property.  <br/> |
|contacts:DisplayName  <br/> |Identifies the **DisplayName** property.  <br/> |
|contacts:DirectoryId  <br/> |Identifies the **DirectoryId** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:DirectReports  <br/> |Identifies the **DirectReports** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:EmailAddresses  <br/> |Identifies the **EmailAddresses** property.  <br/> |
|contacts:FileAs  <br/> |Identifies the **FileAs** property.  <br/> |
|contacts:FileAsMapping  <br/> |Identifies the **FileAsMapping** property.  <br/> |
|contacts:Generation  <br/> |Identifies the **Generation** property.  <br/> |
|contacts:GivenName  <br/> |Identifies the **GivenName** property.  <br/> |
|contacts:ImAddresses  <br/> |Identifies the **ImAddresses** property.  <br/> |
|contacts:Initials  <br/> |Identifies the **Initials** property.  <br/> |
|contacts:JobTitle  <br/> |Identifies the **JobTitle** property.  <br/> |
|contacts:Manager  <br/> |Identifies the **Manager** property.  <br/> |
|contacts:ManagerMailbox  <br/> |Identifies the **ManagerMailbox** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:MiddleName  <br/> |Identifies the **MiddleName** property.  <br/> |
|contacts:Mileage  <br/> |Identifies the **Mileage** property.  <br/> |
|contacts:MSExchangeCertificate  <br/> |Identifies the **MSExchangeCertificate** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:Nickname  <br/> |Identifies the **Nickname** property.  <br/> |
|contacts:Notes  <br/> |Identifies the **Notes** property. This property was introduced with in Exchange 2010 SP2.  <br/> |
|contacts:OfficeLocation  <br/> |Identifies the **OfficeLocation** property.  <br/> |
|contacts:PhoneNumbers  <br/> |Identifies the **PhoneNumbers** property.  <br/> |
|contacts:PhoneticFullName  <br/> |Identifies the **PhoneticFullName** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:PhoneticFirstName  <br/> |Identifies the **PhoneticFirstName** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:PhoneticLastName  <br/> |Identifies the **PhoneticLastName** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:Photo  <br/> |Identifies the **Photo** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:PhysicalAddresses  <br/> |Identifies the **PhysicalAddresses** property.  <br/> |
|contacts:PostalAddressIndex  <br/> |Identifies the **PostalAddressIndex** property.  <br/> |
|contacts:Profession  <br/> |Identifies the **Profession** property.  <br/> |
|contacts:SpouseName  <br/> |Identifies the **SpouseName** property.  <br/> |
|contacts:Surname  <br/> |Identifies the **Surname** property.  <br/> |
|contacts:WeddingAnniversary  <br/> |Identifies the **WeddingAnniversary** property.  <br/> |
|contacts:UserSMIMECertificate  <br/> |Identifies the **UserSMIMECertificate** property. This property was introduced in Exchange 2010 SP2.  <br/> |
|contacts:HasPicture  <br/> |Identifies the **HasPicture** property.  <br/> |
|distributionlist:Members  <br/> |Identifies the **Members** property.  <br/> |
|postitem:PostedTime  <br/> |Identifies the **PostedTime** property.  <br/> |
|conversation:ConversationId  <br/> |Identifies the **ConversationId** property.  <br/> |
|conversation:ConversationTopic  <br/> |Identifies the **ConversationTopic** property.  <br/> |
|conversation:UniqueRecipients  <br/> |Identifies the **UniqueRecipients** property.  <br/> |
|conversation:GlobalUniqueRecipients  <br/> |Identifies the **GlobalUniqueRecipients** property.  <br/> |
|conversation:UniqueUnreadSenders  <br/> |Identifies the **UniqueUnreadSenders** property.  <br/> |
|conversation:GlobalUniqueUnreadSenders  <br/> |Identifies the **GlobalUniqueUnreadSenders** property.  <br/> |
|conversation:UniqueSenders  <br/> |Identifies the **UniqueSenders** property.  <br/> |
|conversation:GlobalUniqueSenders  <br/> |Identifies the **GlobalUniqueSenders** property.  <br/> |
|conversation:LastDeliveryTime  <br/> |Identifies the **LastDeliveryTime** property.  <br/> |
|conversation:GlobalLastDeliveryTime  <br/> |Identifies the **GlobalLastDeliveryTime** property.  <br/> |
|conversation:Categories  <br/> |Identifies the **Categories** property.  <br/> |
|conversation:GlobalCategories  <br/> |Identifies the **GlobalCategories** property.  <br/> |
|conversation:FlagStatus  <br/> |Identifies the **FlagStatus** property.  <br/> |
|conversation:GlobalFlagStatus  <br/> |Identifies the **GlobalFlagStatus** property.  <br/> |
|conversation:HasAttachments  <br/> |Identifies the **HasAttachments** property.  <br/> |
|conversation:GlobalHasAttachments  <br/> |Identifies the **GlobalHasAttachments** property.  <br/> |
|conversation:HasIrm  <br/> |Identifies the **HasIrm** property.  <br/> |
|conversation:GlobalHasIrm  <br/> |Identifies the **GlobalHasIrm** property.  <br/> |
|conversation:MessageCount  <br/> |Identifies the **MessageCount** property.  <br/> |
|conversation:GlobalMessageCount  <br/> |Identifies the **GlobalMessageCount** property.  <br/> |
|conversation:UnreadCount  <br/> |Identifies the **UnreadCount** property.  <br/> |
|conversation:GlobalUnreadCount  <br/> |Identifies the **GlobalUnreadCount** property.  <br/> |
|conversation:Size  <br/> |Identifies the **Size** property.  <br/> |
|conversation:GlobalSize  <br/> |Identifies the **GlobalSize** property.  <br/> |
|conversation:ItemClasses  <br/> |Identifies the **ItemClasses** property.  <br/> |
|conversation:GlobalItemClasses  <br/> |Identifies the **GlobalItemClasses** property.  <br/> |
|conversation:Importance  <br/> |Identifies the **Importance** property.  <br/> |
|conversation:GlobalImportance  <br/> |Identifies the **GlobalImportance** property.  <br/> |
|conversation:ItemIds  <br/> |Identifies the **ItemIds** property.  <br/> |
|conversation:GlobalItemIds  <br/> |Identifies the **GlobalItemIds** property.  <br/> |
|conversation:LastModifiedTime  <br/> |Identifies the **LastModifiedTime** property.  <br/> |
|conversation:InstanceKey  <br/> |Identifies the **InstanceKey** property.  <br/> |
|conversation:Preview  <br/> |Identifies the **Preview** property.  <br/> |
|conversation:GlobalParentFolderId  <br/> |Identifies the **GlobalParentFolderId** property.  <br/> |
|conversation:NextPredictedAction  <br/> |Identifies the **NextPredictedAction** property.  <br/> |
|conversation:GroupingAction  <br/> |Identifies the **GroupingAction** property.  <br/> |
|conversation:IconIndex  <br/> |Identifies the **IconIndex** property.  <br/> |
|conversation:GlobalIconIndex  <br/> |Identifies the **GlobalIconIndex** property.  <br/> |
|conversation:DraftItemIds  <br/> |Identifies the **DraftItemIds** property.  <br/> |
|conversation:HasClutter  <br/> |Intended for internal use only.  <br/> |
|persona:PersonaId  <br/> |Identifies the **PersonaId** property.  <br/> |
|persona:PersonaType  <br/> |Identifies the **PersonaType** property.  <br/> |
|persona:GivenName  <br/> |Identifies the **GivenName** property.  <br/> |
|persona:CompanyName  <br/> |Identifies the **CompanyName** property.  <br/> |
|persona:Surname  <br/> |Identifies the **Surname** property.  <br/> |
|persona:DisplayName  <br/> |Identifies the **DisplayName** property.  <br/> |
|persona:EmailAddress  <br/> |Identifies the **EmailAddress** property.  <br/> |
|persona:FileAs  <br/> |Identifies the **FileAs** property.  <br/> |
|persona:HomeCity  <br/> |Identifies the **HomeCity** property.  <br/> |
|persona:CreationTime  <br/> |Identifies the **CreationTime** property.  <br/> |
|persona:RelevanceScore  <br/> |Identifies the **RelevanceScore** property.  <br/> |
|persona:WorkCity  <br/> |Identifies the **WorkCity** property.  <br/> |
|persona:PersonaObjectStatus  <br/> |Identifies the **PersonaObjectStatus** property.  <br/> |
|persona:FileAsId  <br/> |Identifies the **FileAsId** property.  <br/> |
|persona:DisplayNamePrefix  <br/> |Identifies the **DisplayNamePrefix** property.  <br/> |
|persona:YomiCompanyName  <br/> |Identifies the **YomiCompanyName** property.  <br/> |
|persona:YomiFirstName  <br/> |Identifies the **YomiFirstName** property.  <br/> |
|persona:YomiLastName  <br/> |Identifies the **YomiLastName** property.  <br/> |
|persona:Title  <br/> |Identifies the **Title** property.  <br/> |
|persona:EmailAddresses  <br/> |Identifies the **EmailAddresses** property.  <br/> |
|persona:PhoneNumber  <br/> |Identifies the **PhoneNumber** property.  <br/> |
|persona:ImAddress  <br/> |Identifies the **ImAddress** property.  <br/> |
|persona:ImAddresses  <br/> |Identifies the **ImAddresses** property.  <br/> |
|persona:ImAddresses2  <br/> |Identifies the **ImAddresses2** property.  <br/> |
|persona:ImAddresses3  <br/> |Identifies the **ImAddresses3** property.  <br/> |
|persona:FolderIds  <br/> |Identifies the **FolderIds** property.  <br/> |
|persona:Attributions  <br/> |Identifies the **Attributions** property.  <br/> |
|persona:DisplayNames  <br/> |Identifies the **DisplayNames** property.  <br/> |
|persona:Initials  <br/> |Identifies the **Initials** property.  <br/> |
|persona:FileAses  <br/> |Identifies the **FileAses** property.  <br/> |
|persona:FileAsIds  <br/> |Identifies the **FileAsIds** property.  <br/> |
|persona:DisplayNamePrefixes  <br/> |Identifies the **DisplayNamePrefixes** property.  <br/> |
|persona:GivenNames  <br/> |Identifies the **GivenNames** property.  <br/> |
|persona:MiddleNames  <br/> |Identifies the **MiddleNames** property.  <br/> |
|persona:Surnames  <br/> |Identifies the **Surnames** property.  <br/> |
|persona:Generations  <br/> |Identifies the **Generations** property.  <br/> |
|persona:Nicknames  <br/> |Identifies the **Nicknames** property.  <br/> |
|persona:YomiCompanyNames  <br/> |Identifies the **YomiCompanyNames** property.  <br/> |
|persona:YomiFirstNames  <br/> |Identifies the **YomiFirstNames** property.  <br/> |
|persona:YomiLastNames  <br/> |Identifies the **YomiLastNames** property.  <br/> |
|persona:BusinessPhoneNumbers  <br/> |Identifies the **BusinessPhoneNumbers** property.  <br/> |
|persona:BusinessPhoneNumbers2  <br/> |Identifies the **BusinessPhoneNumbers2** property.  <br/> |
|persona:HomePhones  <br/> |Identifies the **HomePhones** property.  <br/> |
|persona:HomePhones2  <br/> |Identifies the **HomePhones2** property.  <br/> |
|persona:MobilePhones  <br/> |Identifies the **MobilePhones** property.  <br/> |
|persona:MobilePhones2  <br/> |Identifies the **MobilePhones2** property.  <br/> |
|persona:AssistantPhoneNumbers  <br/> |Identifies the **AssistantPhoneNumbers** property.  <br/> |
|persona:CallbackPhones  <br/> |Identifies the **CallbackPhones** property.  <br/> |
|persona:CarPhones  <br/> |Identifies the **CarPhones** property.  <br/> |
|persona:HomeFaxes  <br/> |Identifies the **HomeFaxes** property.  <br/> |
|persona:OrganizationMainPhones  <br/> |Identifies the **OrganizationMainPhones** property.  <br/> |
|persona:OtherFaxes  <br/> |Identifies the **OtherFaxes** property.  <br/> |
|persona:OtherTelephones  <br/> |Identifies the **OtherTelephones** property.  <br/> |
|persona:OtherPhones2  <br/> |Identifies the **OtherPhones2** property.  <br/> |
|persona:Pagers  <br/> |Identifies the **Pagers** property.  <br/> |
|persona:RadioPhones  <br/> |Identifies the **RadioPhones** property.  <br/> |
|persona:TelexNumbers  <br/> |Identifies the **TelexNumbers** property.  <br/> |
|persona:WorkFaxes  <br/> |Identifies the **WorkFaxes** property.  <br/> |
|persona:Emails1  <br/> |Identifies the **Emails1** property.  <br/> |
|persona:Emails2  <br/> |Identifies the **Emails2** property.  <br/> |
|persona:Emails3  <br/> |Identifies the **Emails3** property.  <br/> |
|persona:BusinessHomePages  <br/> |Identifies the **BusinessHomePages** property.  <br/> |
|persona:School  <br/> |Identifies the **School** property.  <br/> |
|persona:PersonalHomePages  <br/> |Identifies the **PersonalHomePages** property.  <br/> |
|persona:OfficeLocations  <br/> |Identifies the **OfficeLocations** property.  <br/> |
|persona:BusinessAddresses  <br/> |Identifies the **BusinessAddresses** property.  <br/> |
|persona:HomeAddresses  <br/> |Identifies the **HomeAddresses** property.  <br/> |
|persona:OtherAddresses  <br/> |Identifies the **OtherAddresses** property.  <br/> |
|persona:Titles  <br/> |Identifies the **Titles** property.  <br/> |
|persona:Departments  <br/> |Identifies the **Departments** property.  <br/> |
|persona:CompanyNames  <br/> |Identifies the **CompanyNames** property.  <br/> |
|persona:Managers  <br/> |Identifies the **Managers** property.  <br/> |
|persona:AssistantNames  <br/> |Identifies the **AssistantNames** property.  <br/> |
|persona:Professions  <br/> |Identifies the **Professions** property.  <br/> |
|persona:SpouseNames  <br/> |Identifies the **SpouseNames** property.  <br/> |
|persona:Hobbies  <br/> |Identifies the **Hobbies** property.  <br/> |
|persona:WeddingAnniversaries  <br/> |Identifies the **WeddingAnniversaries** property.  <br/> |
|persona:Birthdays  <br/> |Identifies the **Birthdays** property.  <br/> |
|persona:Children  <br/> |Identifies the **Children** property.  <br/> |
|persona:Locations  <br/> |Identifies the **Locations** property.  <br/> |
|persona:ExtendedProperties  <br/> |Identifies the **ExtendedProperties** property.  <br/> |
|persona:PostalAddress  <br/> |Identifies the **PostalAddress** property.  <br/> |
|persona:Bodies  <br/> |Identifies the **Bodies** property.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> | Identifiziert zusätzliche Eigenschaften zum Abrufen, Festlegen oder Erstellen.  <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:  <br/>  `/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[AggregateOn](aggregateon.md) <br/> |Stellt die Eigenschaft dar, die zum Ermitteln der Reihenfolge gruppierter Elemente für einen gruppierten FindItem-Ergebnissatz verwendet werden.  <br/> |
|[GroupBy](groupby.md) <br/> |Gibt eine beliebige Gruppierung für FindItem-Abfragen an.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung einer einzelnen Eigenschaft eines Elements in einer UpdateItem-Operation dar.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine einzelne Eigenschaft zu einem Ordner in einer UpdateFolder-Operation dar.  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Stellt einen Löschvorgang für das Löschen einer angegebenen Eigenschaft aus einem Element während eines UpdateItem-Aufrufs dar.  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Stellt einen Löschvorgang einer angegebenen Eigenschaft aus einem Ordner während eines UpdateFolder-Aufrufs dar.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Exists](exists.md) <br/> |Stellt einen Suchausdruck dar, der **true** zurückgibt, wenn die angegebene Eigenschaft zu einem Element vorhanden ist.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** ausgibt, wenn sie gleich sind.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer ist.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft größer oder gleich der zweiten ist.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als die zweite ist.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner als die zweite ist.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Stellt einen Suchausdruck dar, der einer Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Wert nicht identisch sind.  <br/> |
|[Schließt](excludes.md) <br/> |Führt eine bitweise Maske der Eigenschaften aus.  <br/> |
|[Enthält](contains.md) <br/> |Stellt einen Suchausdruck dar, der bestimmt, ob eine angegebene Eigenschaft den angegebenen konstanten Zeichenfolgewert enthält.  <br/> |
|[FieldOrder](fieldorder.md) <br/> |Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist Teil der [Pfad](path.md)-Ersetzungsgruppe. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie das FieldURI-Element verwendet wird.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

