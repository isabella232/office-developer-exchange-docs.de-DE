---
title: GetItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: Das GetItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetItem-Vorgangsanforderung.
ms.openlocfilehash: 3c931a6d7df91e4e90bfd0a69dc4816ee71a0aad
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521962"
---
# <a name="getitemresponsemessage"></a>GetItemResponseMessage

Das **GetItemResponseMessage-Element** enthält den Status und das Ergebnis einer einzelnen [GetItem-Vorgangsanforderung.](getitem-operation.md) 
  
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
|**ResponseClass** <br/> | Beschreibt den Status einer [GetItem-Vorgangsantwort.](getitem-operation.md) <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>– Erfolg<br/>- Warnung<br/>- Fehler |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.<br/><br/>Es folgen Beispiele für Quellen für Warnungen:<br/><br/>– Der Exchange Speicher ist während des Batches offline.<br/>– Active Directory Domain Services (AD DS) ist offline.<br/>– Postfächer werden verschoben.<br/>– MDB ist offline.<br/>– Kennwort ist abgelaufen.  <br/>– Das Kontingent wird überschritten. |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann.<br/><br/>Es folgen Beispiele für Fehlerquellen:<br/><br/>– Ungültige Attribute oder Elemente<br/>– Attribute oder Elemente außerhalb des Bereichs<br/>- Unbekanntes Tag<br/>- Attribut oder Element im Kontext ungültig<br/>– Nicht autorisierter Zugriff, der von einem beliebigen Client versucht wurde<br/>- Serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf<br/><br/>Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md) |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Items](items.md) <br/> |Enthält ein Array von zurückgegebenen Elementen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetItem](getitem.md)
- [GetItem-Vorgang](getitem-operation.md)

