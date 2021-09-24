---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: Das ArchiveItemResponseMessage-Element gibt die Antwortnachricht an eine ArchiveItem-Anforderung an.
ms.openlocfilehash: c0d816039ea0ab9d69d04d979a9dad973e4278b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525260"
---
# <a name="archiveitemresponsemessage"></a>ArchiveItemResponseMessage

Das **ArchiveItemResponseMessage-Element** gibt die Antwortnachricht an eine **ArchiveItem-Anforderung** an. 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 **ItemInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResponseClass  <br/> |Gibt die Klasse der Antwort an.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Gibt den Erfolg an.  <br/> |
|Warnung  <br/> |Gibt eine Warnung an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und für die zukünftige Verwendung reserviert.  <br/> |
|[Items](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt Statusinformationen zu der Anforderung bereit.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange Webdienstanforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

