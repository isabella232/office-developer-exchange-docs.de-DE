---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: Das FindMailboxStatisticsByKeywordsResponseMessage-Element gibt die Antwortnachricht für eine FindMailboxStatisticsByKeywords-Anforderung an.
ms.openlocfilehash: f41a44ebb90b59c7458162dffe445bbeba7c2ba0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513717"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a>FindMailboxStatisticsByKeywordsResponseMessage

Das **FindMailboxStatisticsByKeywordsResponseMessage-Element** gibt die Antwortnachricht für eine **FindMailboxStatisticsByKeywords-Anforderung** an. 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 **FindMailboxStatisticsByKeywordsResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|ResponseClass  <br/> |Gibt die Antwortklasse an.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolg  <br/> |Gibt den Erfolg an.  <br/> |
|Warnung  <br/> |Gibt eine Warnung an.  <br/> |
|Fehler  <br/> |Gibt einen Fehler an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md) <br/> |Gibt das Ergebnis einer Postfachsuche an.  <br/> |
|[MessageText](messagetext.md) <br/> |Stellt eine Textbeschreibung des Status der Antwort bereit.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Stellt Statusinformationen zu der Anforderung bereit.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Derzeit nicht verwendet und für die zukünftige Verwendung reserviert.  <br/> |
|[MessageXml](messagexml.md) <br/> |Bietet zusätzliche Fehlerantwortinformationen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Gibt ein Array von Antwortnachrichten an.  <br/> |
   
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

