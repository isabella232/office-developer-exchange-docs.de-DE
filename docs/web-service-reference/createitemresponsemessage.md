---
title: CreateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateItemResponseMessage
api_type:
- schema
ms.assetid: 595d36c2-f87a-4d50-8e8b-f58d7641564b
description: Das CreateItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateItem-Vorgangsanforderung.
ms.openlocfilehash: 0495cb5ac9a4f749cb1e6a69360023b43ade7954
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511874"
---
# <a name="createitemresponsemessage"></a>CreateItemResponseMessage

Das **CreateItemResponseMessage-Element** enthält den Status und das Ergebnis einer einzelnen [CreateItem-Vorgangsanforderung.](createitem-operation.md) 
  
- [CreateItemResponse](createitemresponse.md)  
- [ResponseMessages](responsemessages.md) 
- [CreateItemResponseMessage](createitemresponsemessage.md)
  
```xml
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 **ItemInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [CreateItem-Vorgangsantwort.](createitem-operation.md)<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.<br/><br/>Es folgen Beispiele für Warnungsquellen:<br/><br/>– Der Exchange Speicher ist während des Batches offline.  <br/>– Active Directory Domain Services (AD DS) ist offline.  <br/>– Postfächer werden verschoben.  <br/>– Die Nachrichtendatenbank (MDB) ist offline.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wird überschritten.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann.<br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente  <br/>– Attribute oder Elemente außerhalb des Bereichs  <br/>- Unbekanntes Tag  <br/>- Attribut oder Element im Kontext ungültig  <br/>– Versuch eines nicht autorisierten Zugriffs durch einen beliebigen Client  <br/>- Serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf<br/><br/>  Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[Items](items.md) <br/> |Enthält ein Array von erstellten Elementen.  <br/> |
   
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

- [CreateItem-Vorgang](createitem-operation.md)
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

