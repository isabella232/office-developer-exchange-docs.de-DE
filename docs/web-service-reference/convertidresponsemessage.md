---
title: ConvertIdResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertIdResponseMessage
api_type:
- schema
ms.assetid: 7a439cae-0268-4328-9ded-af56ad642227
description: Das ConvertIdResponseMessage-Element enthält den Status und das Ergebnis einer ConvertId-Vorgangsanforderung.
ms.openlocfilehash: 28792cd62b76323f942138796ee2d0596b9664ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518659"
---
# <a name="convertidresponsemessage"></a>ConvertIdResponseMessage

Das **ConvertIdResponseMessage-Element** enthält den Status und das Ergebnis einer [ConvertId-Vorgangsanforderung.](convertid-operation.md) 
  
- [ConvertIdResponse](convertidresponse.md) 
- [ResponseMessages](responsemessages.md)
- [ConvertIdResponseMessage](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 **ConvertIdResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [ConvertId-Vorgangsantwort.](convertid-operation.md)<br/><br/>Die folgenden Werte sind für dieses Attribut gültig:<br/><br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht vollständig verarbeitet wurde oder für die ein unbeabsichtigtes Ergebnis aufgetreten ist.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann.<br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Ungültige Attribute oder Elemente  <br/>– Attribute oder Elemente, die außerhalb des Gültigen liegen  <br/>– Ein unbekanntes Tag  <br/>– Ein Attribut oder Element, das im Kontext ungültig ist  <br/>– Ein nicht autorisierter Zugriffsversuch durch einen beliebigen Client  <br/>– Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf<br/><br/>Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, auf den die Anforderung gestoßen ist.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und für die zukünftige Verwendung reserviert. Dieses Element enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[AlternateId](alternateid.md) <br/> |Beschreibt einen konvertierten Bezeichner in der Antwort.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Pro konvertierter ID wird eine Antwortnachricht zurückgegeben. Das [AlternateId-Element](alternateid.md) fehlt in der Antwort, wenn ein Fehlerantwortcode zurückgegeben wird. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ConvertId-Vorgang](convertid-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

