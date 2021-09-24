---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: Das ResolveNamesResponseMessage-Element enthält den Status und das Ergebnis einer ResolveNames-Vorgangsanforderung.
ms.openlocfilehash: a7debc5f5056ad7a33ebfaf2b0d5d914acdb2397
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523475"
---
# <a name="resolvenamesresponsemessage"></a>ResolveNamesResponseMessage

Das **ResolveNamesResponseMessage-Element** enthält den Status und das Ergebnis einer [ResolveNames-Vorgangsanforderung.](resolvenames-operation.md) 
  
- [ResolveNamesResponse](resolvenamesresponse.md) 
- [ResponseMessages](responsemessages.md)
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 **ResolveNamesResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ResponseClass** <br/> | Beschreibt den Status einer [ResolveNames-Vorgangsantwort.](resolvenames-operation.md) <br/><br/>Die folgenden Werte sind für dieses Attribut gültig:  <br/><br/>– Erfolg  <br/>- Warnung  <br/>- Fehler  <br/> |
   
#### <a name="responseclass-attribute"></a>ResponseClass-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Success** <br/> |Beschreibt eine Anforderung, die erfüllt wird. Dies tritt auf, wenn der angeforderte Name eindeutig ist und die Antwort einen einzelnen Empfänger enthält.  <br/> |
|**Warning** <br/> | Beschreibt eine Anforderung, die nicht verarbeitet wurde. Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten. <br/><br/>Es folgt ein Beispiel für Warnungsquellen:  <br/><br/>– Der Exchange Speicher wird während des Batches offline geschaltet.  <br/>– Active Directory Domain Services (AD DS) wird offline geschaltet.  <br/>– Postfächer werden verschoben.  <br/>– Die Postfachdatenbank (MDB) wird offline geschaltet.  <br/>– Ein Kennwort ist abgelaufen.  <br/>– Ein Kontingent wird überschritten.  <br/>– Der angeforderte Name ist mehrdeutig, und die Antwort enthält mehrere Empfänger.  <br/> |
|**Error** <br/> | Beschreibt eine Anforderung, die nicht erfüllt werden kann. <br/><br/>Es folgen Beispiele für Fehlerquellen:  <br/><br/>– Der angeforderte Name konnte nicht aufgelöst werden.  <br/>– Attribute oder Elemente sind ungültig.  <br/>– Attribute oder Elemente liegen außerhalb des Gültigen.  <br/>– Ein Tag ist unbekannt.  <br/>– Ein Attribut oder Element ist im Kontext ungültig.  <br/>– Ein nicht autorisierter Zugriffsversuch durch einen Beliebigen Client ist aufgetreten.  <br/>– Ein serverseitiger Fehler ist als Reaktion auf einen gültigen clientseitigen Aufruf aufgetreten.  <br/>  <br/>Informationen zu dem Fehler finden Sie in den [ResponseCode-](responsecode.md) und [MessageText-Elementen.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt Fehlerinformationen zur Anforderung bereit.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert. Sie enthält den Wert 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[ResolutionSet](resolutionset.md) <br/> |Enthält ein Array von Auflösungen für einen mehrdeutigen Namen.  <br/> |
   
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ResolveNames](resolvenames.md)
- [ResolveNamesResponse](resolvenamesresponse.md)
- [ResolveNames-Vorgang](resolvenames-operation.md)

