---
title: MessageText
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageText
api_type:
- schema
ms.assetid: 59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1
description: Das MessageText-Element enthält einen beschreibenden Text für den Status der Antwort.
ms.openlocfilehash: e90313c1b8616658932de4b394d4a2b3ed0fd054
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830462"
---
# <a name="messagetext"></a>MessageText

Das **MessageText** -Element enthält einen beschreibenden Text für den Status der Antwort. 
  
```XML
<MessageText/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Enthält beschreibende Informationen über den Antwortstatus.  <br/> <br/> Im folgenden sind einige der möglichen XPath-Ausdrücke auf dieses Element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer DeleteItem Anforderung.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung den SendItem.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteFolder-Anforderung.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer DeleteAttachment Anforderung.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung zum Abmelden.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateFolder-Anforderung.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetFolder-Anforderung.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer UpdateFolder Anforderung.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen MoveFolder-Anforderung.  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CopyFolder-Anforderung.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer CreateManagedFolder Anforderung.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer FindFolder Anforderung.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateItem-Anforderung.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetItem-Anforderung.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer UpdateItem Anforderung.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen MoveItem-Anforderung.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer "CopyItem" Anforderung.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer CreateAttachment Anforderung.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetAttachment Anforderung.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer FindItem Anforderung.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung ResolveNames.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung der ExpandDL.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Subscribe-Anforderung.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetEvents Anforderung.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SendNotification Anforderung.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung SyncFolderHierarchy.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung SyncFolderItems.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung ConvertId.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung AddDelegate.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung GetServerTimeZones.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung GetSharingFolder.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingFolder an.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung GetSharingMetadata.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingMetadata an.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung RefreshSharingFolder.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine RefreshSharingFolder an.  <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Stellt einen ungültigen Empfänger für eine Anforderung GetSharingMetadata.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Enthält den Status und die Ergebnisse einer **FindConversation** Antwort.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen **EmptyFolder** -Anforderung.  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Enthält eine Antwort auf eine Anforderung **UpdateInboxRules** .  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Enthält eine Antwort auf eine **GetInboxRules** an.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Enthält eine Antwort auf eine **GetServiceConfiguration** an.  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Konfigurationseinstellungen für enthält.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist nicht erforderlich, und ist nicht in allen Antworten enthalten. Wenn Fehlermeldungen zurückgegeben werden, wird dieses Element hinzugefügt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

