---
title: MessageXml
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageXml
api_type:
- schema
ms.assetid: bcaf9e35-d351-48f3-baad-f90c633cba8a
description: Das MessageXml-Element stellt zusätzliche Fehlerantwortinformationen bereit.
ms.openlocfilehash: 714f055956cee6686acccd98881a12fb976e6c12
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540762"
---
# <a name="messagexml"></a>MessageXml

Das **MessageXml-Element** stellt zusätzliche Fehlerantwortinformationen bereit. 
  
- [ResponseMessage](responsemessage.md)  
- [MessageXml](messagexml.md)
  
```XML
<MessageXml/>
```

 **xs:any**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Enthält beschreibende Informationen zum Antwortstatus. <br/> <br/>  Nachfolgend sind einige der möglichen XPath-Ausdrücke für dieses Element aufgeführt: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteItem-Anforderung.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen SendItem-Anforderung.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteFolder-Anforderung.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteAttachment-Anforderung.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Unsubscribe-Anforderung.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateFolder-Anforderung.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetFolder-Anforderung.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen UpdateFolder-Anforderung.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen MoveFolder-Anforderung.  <br/> |
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CopyFolder-Anforderung.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateManagedFolder-Anforderung.  <br/> |
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen FindFolder-Anforderung.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateItem-Anforderung.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetItem-Anforderung.  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen UpdateItem-Anforderung.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen MoveItem-Anforderung.  <br/> |
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CopyItem-Anforderung.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateAttachment-Anforderung.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetAttachment-Anforderung.  <br/> |
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen FindItem-Anforderung.  <br/> |
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer ResolveNames-Anforderung.  <br/> |
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen ExpandDL-Anforderung.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Subscribe-Anforderung.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetEvents-Anforderung.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen SendNotification-Anforderung.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderItems-Anforderung.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer ConvertId-Anforderung.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer AddDelegate-Anforderung.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetServerTimeZones-Anforderung.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetSharingFolder-Anforderung.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingFolder-Anforderung.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetSharingMetadata-Anforderung.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingMetadata-Anforderung.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer RefreshSharingFolder-Anforderung.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine RefreshSharingFolder-Anforderung.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Enthält den Status und die Ergebnisse einer **FindConversation-Antwort.**  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer **EmptyFolder-Anforderung.**  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Enthält den Status und das Ergebnis einer **UpdateInboxRules-Anforderung.**  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer **UploadItemsResponse-Anforderung.**  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Enthält eine Antwort auf eine **GetInboxRules-Anforderung.**  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Enthält eine Antwort auf eine **GetServiceConfiguration-Anforderung.**  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Enthält Dienstkonfigurationseinstellungen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist nicht erforderlich und nicht in allen Antworten enthalten. Sie ist für Fehlermeldungen enthalten. In Anforderungen, die Ordner oder Elemente betreffen, enthält das **MessageXML-Element** ein oder mehrere Elemente, die die URIs für die Eigenschaften enthalten, die den Fehler verursacht haben. Ein Beispiel hierfür ist das [FieldURI-Element.](fielduri.md) 
  
Das **MessageXML-Element** ist vom Typ **"xs:any",** was bedeutet, dass wohlgeformte XML-Elemente gültiger Inhalt für dieses Element sind.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

