---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: Das ResponseMessage-Element enthält beschreibende Informationen über den Antwortstatus für eine einzelne Entität innerhalb einer Anforderung.
ms.openlocfilehash: 69f1f6f12d10044045b72dd644536e742c479b9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831191"
---
# <a name="responsemessage"></a>ResponseMessage

Das **ResponseMessage** -Element enthält beschreibende Informationen über den Antwortstatus für eine einzelne Entität innerhalb einer Anforderung. 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Stellt den Status der Antwort. <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>-Success  <br/>-Warnung  <br/>-Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Attributwerte ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|Warning  <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte. <br/><br/>Es folgen einige möglichen Ursachen für Warnungen:  <br/><br/>-Der Exchange-Speicher ist während der Batchaktualisierung offline.  <br/>– Der Active Directory-Verzeichnisdienst ist offline.  <br/>-Postfächer werden verschoben.  <br/>-Die Nachrichtendatenbank (MDB) ist offline.  <br/>-Ein Kennwort ist abgelaufen.  <br/>-Ein Kontingent überschritten wird.  <br/> |
|Fehler  <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann. <br/><br/>Es folgen einige möglichen Ursachen für Fehler:  <br/><br/>-Ungültige Attribute oder Elemente  <br/>-Attribute oder Elemente außerhalb des gültigen Bereichs  <br/>-Unbekanntes tag  <br/>-Attribut oder ein Element im Kontext ist ungültig.  <br/>-Versuch von jedem Client Zugriff  <br/>-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf  <br/> <br/> Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Es enthält einen Wert von 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Die Frei/Gebucht-Informationen für ein einzelnes Postfachbenutzer enthält. <br/> <br/> Es folgt der 2.0 XPath-Ausdruck, der dieses Element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |Enthält Informationen und Vorschlag Daten für Besprechungsvorschläge angefordert.  <br/><br/> Es folgt der 2.0 XPath-Ausdruck, der dieses Element:<br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Enthält die Antwort Ergebnisse und OOF-Einstellungen für einen Benutzer.  <br/><br/> Es folgt der 2.0 XPath-Ausdruck, der dieses Element:  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[SetUserOofSettingsResponse](setuseroofsettingsresponse.md) <br/> |Das Ergebnis einer versuchte [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) -Nachricht enthält. <br/> <br/> Es folgt der 2.0 XPath-Ausdruck, der dieses Element:  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Hinweise

Der Typ **ResponseMessageType** ist für alle Exchange-Webdienste-Antworten. Der Typ **ResponseMessageType** wird durch den folgenden komplexen Typen erweitert: 
  
- **ApplyConversationActionResponseMessageType**
    
- **AttachmentInfoResponseMessageType**
    
- **DeleteAttachmentResponseMessageType**
    
- **DeleteItemResponseMessageType**
    
- **ExpandDLResponseMessageType**
    
- **FindFolderResponseMessageType**
    
- **FindItemResponseMessageType**
    
- **FolderInfoResponseMessageType**
    
- **GetEventsResponseMessageType**
    
- **ItemInfoResponseMessageType**
    
- **ResolveNamesResponseMessageType**
    
- **SubscribeResponseMessageType**
    
- **SendNotificationResponseMessageType**
    
- **SyncFolderHierarchyResponseMessageType**
    
- **SyncFolderItemsResponseMessageType**
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
### <a name="version-differences"></a>Versionsunterschiede

Die Typen **ApplyConversationActionResponseMessage** und **DeleteItemResponseMessageType** wurden in Exchange Build 15.00.0986.00 eingeführt. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)
- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

