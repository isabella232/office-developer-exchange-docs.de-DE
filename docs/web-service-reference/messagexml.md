---
title: Messagexml verwendet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageXml
api_type:
- schema
ms.assetid: bcaf9e35-d351-48f3-baad-f90c633cba8a
description: Das messagexml verwendet-Element bietet zusätzliche Informationen zur Fehlerantwort.
ms.openlocfilehash: 180b447874523742a1d29d457c4ef020e4124f7c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466276"
---
# <a name="messagexml"></a>Messagexml verwendet

Das **messagexml verwendet** -Element bietet zusätzliche Informationen zur Fehlerantwort. 
  
- [ResponseMessage](responsemessage.md)  
- [Messagexml verwendet](messagexml.md)
  
```XML
<MessageXml/>
```

 **xs: Any**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> | Enthält beschreibende Informationen zum Antwortstatus. <br/> <br/>  Im folgenden sind einige der möglichen XPath-Ausdrücke für dieses Element angegeben: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/ResponseMessage` <br/> <br/> `/GetUserAvailabilityResponse/SuggestionsResponse/ResponseMessage` <br/><br/>  `/SetUserOofSettingsResponse/ResponseMessage` <br/><br/>  `/GetUserOofSettingsResponse/ResponseMessage` <br/> |
|[DeleteItemResponseMessage](deleteitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteItem-Anforderung.  <br/> |
|[SendItemResponseMessage](senditemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen SendItem-Anforderung.  <br/> |
|[DeleteFolderResponseMessage](deletefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteFolder-Anforderung.  <br/> |
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen DeleteAttachment--Anforderung.  <br/> |
|[UnsubscribeResponseMessage](unsubscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen unsubscribe-Anforderung.  <br/> |
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
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen subscribe-Anforderung.  <br/> |
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetEvents-Anforderung.  <br/> |
|[Sendnotificationresponsemessage zurück](sendnotificationresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen SendNotification-Anforderung.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderItems-Anforderung.  <br/> |
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Convert-Anforderung.  <br/> |
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Enthält den Status und das Ergebnis einer AddDelegate-Anforderung.  <br/> |
|[GetServerTimeZonesResponseMessage](getservertimezonesresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetServerTimeZones-Anforderung.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetSharingFolder-Anforderung.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingFolder-Anforderung.  <br/> |
|[GetSharingMetadataResponseMessage](getsharingmetadataresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetSharingMetadata-Anforderung.  <br/> |
|[GetSharingMetadataResponse](getsharingmetadataresponse.md) <br/> |Definiert eine Antwort auf eine GetSharingMetadata-Anforderung.  <br/> |
|[RefreshSharingFolderResponseMessage](refreshsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer RefreshSharingFolder-Anforderung.  <br/> |
|[RefreshSharingFolderResponse](refreshsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine RefreshSharingFolder-Anforderung.  <br/> |
|[FindConversationResponse](findconversationresponse.md) <br/> |Enthält den Status und die Ergebnisse einer **FindConversation** -Antwort.  <br/> |
|[EmptyFolderResponseMessage](emptyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer **EmptyFolder** -Anforderung.  <br/> |
|[UpdateInboxRulesResponse](updateinboxrulesresponse.md) <br/> |Enthält den Status und das Ergebnis einer **UpdateInboxRules** -Anforderung.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer **UploadItemsResponse** -Anforderung.  <br/> |
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Enthält eine Antwort auf eine **GetInboxRules** -Anforderung.  <br/> |
|[GetServiceConfigurationResponse](getserviceconfigurationresponse.md) <br/> |Enthält eine Antwort auf eine **GetServiceConfiguration** -Anforderung.  <br/> |
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Enthält Dienst Konfigurationseinstellungen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist nicht erforderlich und wird nicht in allen Antworten berücksichtigt. Sie ist für Fehlermeldungen enthalten. In Anforderungen, die Ordner oder Elemente umfassen, enthält das **messagexml verwendet** -Element mindestens ein Element, das die URIs für die Eigenschaften enthält, die den Fehler verursacht haben. Ein Beispiel hierfür ist das [FieldURI](fielduri.md) -Element. 
  
Das **messagexml verwendet** -Element ist vom Typ **xs: any**, was bedeutet, dass alle wohlgeformten XML-Daten gültige Inhalte für das this-Element sind.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

