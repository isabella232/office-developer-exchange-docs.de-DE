---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: Das FindMailboxStatisticsByKeywords-Element gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen.
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758459"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

Das **FindMailboxStatisticsByKeywords** -Element gibt eine Anforderung an die Postfachstatistiken nach Schlüsselwort suchen. 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 **FindMailboxStatisticsByKeywordsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Enthält ein Array von Postfächern, die von den Haltestatus betroffen sind.  <br/> |
|[Keywords](keywords-ex15websvcsotherref.md) <br/> |Gibt die Schlüsselwörter für die Suche.  <br/> |
|[Language](language.md) <br/> |Enthält die Sprache für die Suchabfrage verwendet.  <br/> |
|[Absender](senders.md) <br/> |Gibt ein Array von SMTP-Adressen.  <br/> |
|[Empfänger (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Gibt ein Array von Empfänger einer Nachricht.  <br/> |
|[FromDate](fromdate.md) <br/> |Gibt das Datum, das die Nachricht gesendet wurde.  <br/> |
|[ToDate](todate.md) <br/> |Gibt das Datum, das die Nachricht empfangen wurde.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Gibt ein Array von Nachrichten suchen.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Gibt an, ob in gelöschte Elemente durchsuchen.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Gibt an, ob das persönliche Archiv in die Suche einzubeziehen.  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Gibt an, ob Elemente enthalten, die durchsucht werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

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

