---
title: DeleteFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponseMessage
api_type:
- schema
ms.assetid: de4c63ff-80b2-40c2-bc06-ef0c23beacd4
description: Das DeleteFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung DeleteFolder-Vorgang.
ms.openlocfilehash: 5601fe2e48ad002e0fab60d812e7d70c7398f3ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757922"
---
# <a name="deletefolderresponsemessage"></a>DeleteFolderResponseMessage

Das **DeleteFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [DeleteFolder-Vorgang](deletefolder-operation.md) . 
  
- [DeleteFolderResponse](deletefolderresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [DeleteFolderResponseMessage](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer Antwort [DeleteFolder-Vorgang](deletefolder-operation.md) .<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>-Success  <br/>-Warnung  <br/>-Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Attributwerte ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.<br/><br/>Es folgen Beispiele für die Quellen der Warnungen:<br/><br/>-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.<br/>-Active Directory-Domänendienste (AD DS) wird offline geschaltet.<br/>-Postfächer werden verschoben.<br/>-Die Nachrichtendatenbank (MDB) wird offline geschaltet.<br/>-Ein Kennwort ist abgelaufen.<br/>-Ein Kontingent überschritten wird.  <br/> |
|**Fehler** <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann.<br/><br/>Es folgen Beispiele für Datenquellen von Fehlern:<br/><br/>-Ungültige Attribute oder Elemente<br/>-Attribute oder Elemente außerhalb des gültigen Bereichs<br/>-Unbekanntes tag<br/>-Attribut oder ein Element im Kontext ist ungültig.<br/>-Versuch von jedem Client Zugriff<br/>-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf  <br/><br/>  Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Beschreibender Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Es enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteFolder-Vorgang](deletefolder-operation.md)
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Löschen von Ordnern](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

