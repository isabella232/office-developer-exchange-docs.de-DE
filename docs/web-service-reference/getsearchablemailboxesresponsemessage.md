---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: Das GetSearchableMailboxesResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetSearchableMailboxes.
ms.openlocfilehash: 2a4d1fe357656fe29d8572e7f32a4bc2e4a6131e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758800"
---
# <a name="getsearchablemailboxesresponsemessage"></a>GetSearchableMailboxesResponseMessage

Das **GetSearchableMailboxesResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetSearchableMailboxes** . 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 **GetSearchableMailboxesResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResponseClass  <br/> |Gibt die Klasse der Antwort.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Gibt Erfolg an.  <br/> |
|Warning  <br/> |Gibt eine Warnung an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchableMailboxes](searchablemailboxes.md) <br/> |Enthält ein Array der Postfächer aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.  <br/> |
|[MessageText](messagetext.md) <br/> |Enthält einen beschreibenden Text für den Status der Antwort.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Enthält Statusinformationen über die Anforderung.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

