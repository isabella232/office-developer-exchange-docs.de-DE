---
title: GetItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: Das GetItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetItem Operation.
ms.openlocfilehash: 0c8527258d4637ede053e189dfb918b910c859d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758726"
---
# <a name="getitemresponsemessage"></a>GetItemResponseMessage

Das **GetItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetItem Operation](getitem-operation.md) . 
  
- [GetItemResponse](getitemresponse.md) 
- [ResponseMessages](responsemessages.md)
- [GetItemResponseMessage](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

**ItemInfoResponseMessageType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer Antwort [GetItem Operation](getitem-operation.md) . <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>-Success<br/>-Warnung<br/>-Fehler |
   
#### <a name="responseclass-attribute-values"></a>Attributwerte ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt ist.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgenden Elemente nicht verarbeitet werden konnte.<br/><br/>Es folgen Beispiele für Datenquellen für Warnungen:<br/><br/>-Der Exchange-Speicher ist während der Batchaktualisierung offline.<br/>-Active Directory-Domänendienste (AD DS) ist offline.<br/>-Postfächer werden verschoben.<br/>-MDB ist offline.<br/>-Kennwort ist abgelaufen.  <br/>-Kontingent überschritten wird. |
|**Fehler** <br/> | Beschreibt eine Anforderung, die nicht gewährleistet werden kann.<br/><br/>Es folgen Beispiele für Datenquellen für Fehler:<br/><br/>-Ungültige Attribute oder Elemente<br/>-Attribute oder Elemente außerhalb des gültigen Bereichs<br/>-Unbekanntes tag<br/>-Attribut oder ein Element im Kontext ist ungültig.<br/>-Nicht autorisierten Zugriff von jedem Client versucht<br/>-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf<br/><br/>Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden. |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Es enthält einen Wert von 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array der zurückgegebenen Elemente an.  <br/> |
   
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

- [GetItem](getitem.md)
- [GetItem Operation](getitem-operation.md)

