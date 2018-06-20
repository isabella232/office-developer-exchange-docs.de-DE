---
title: ApplyConversationActionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationActionResponseMessage
api_type:
- schema
ms.assetid: a09edc89-7f2f-4846-a3a5-06694c97b9f6
description: Das ApplyConversationActionResponseMessage-Element enthält den Status und die Ergebnisse einer ApplyConversationAction Vorgang Anforderung.
ms.openlocfilehash: d8c5571cfc9c2ea6aaf09cb26a0e47e4abfc3f40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757356"
---
# <a name="applyconversationactionresponsemessage"></a>ApplyConversationActionResponseMessage

Das **ApplyConversationActionResponseMessage** -Element enthält den Status und die Ergebnisse einer Anforderung [ApplyConversationAction Vorgang](applyconversationaction-operation.md) .  
  
- [ApplyConversationActionResponse](applyconversationactionresponse.md)
- [ResponseMessages](responsemessages.md)
- [ApplyConversationActionResponseMessage](applyconversationactionresponsemessage.md)
  
```XML
<ApplyConversationActionResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ApplyConversationActionResponseMessage>
```

 **ApplyConversationActionResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status der Antwort.<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<ul><li>Erfolg</li><li>Warning</li><li>Fehler</li></ul> |
   
#### <a name="responseclass-attribute-values"></a>Attributwerte ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.<br/><br/>Es folgen Beispiele für die Quellen der Warnungen:<ul><li>Exchange-Speicher ist während der Batchaktualisierung offline.</li><li>Active Directory-Domänendienste (AD DS) ist offline.</li><li>Postfächer verschoben wurden.</li><li>Die Nachrichtendatenbank (MDB) ist offline.</li><li>Ein Kennwort ist abgelaufen.</li><li>Ein Kontingent wurde überschritten.</li></ul> |
|**Fehler** <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann.<br/><br/>Es folgen Beispiele für Datenquellen von Fehlern:  <ul><li>Ungültige Attribute oder Elemente</li><li>Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</li><li>Ein unbekanntes tag  </li><li>Ein Attribut oder ein Element, das nicht im Kontext gültig ist</li><li>Ein Versuch nicht autorisierten Zugriff von jedem client</li><li>Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</li></ul>Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert. Dieses Element enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
### <a name="version-differences"></a>Versionsunterschiede

In Versionen von Exchange, beginnend mit Build 15.00.0986.00 ist das **ApplyConversationActionResponseMessage** -Element vom Typ **ApplyConversationActionResponseMessageType**. In früheren Versionen ist das Element vom Typ **ResponseMessageType**.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

