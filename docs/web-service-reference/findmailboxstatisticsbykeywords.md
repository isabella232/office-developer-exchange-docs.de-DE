---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: Das FindMailboxStatisticsByKeywords-Element gibt eine Anforderung zum Suchen nach Postfachstatistiken nach Schlüsselwort an.
ms.openlocfilehash: e22c7d8dc849d3fd45d6cb158030cbd82119437e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462528"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

Das **FindMailboxStatisticsByKeywords** -Element gibt eine Anforderung zum Suchen nach Postfachstatistiken nach Schlüsselwort an. 
  
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
|[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Enthält ein Array von Postfächern, die vom Haltestatus betroffen sind.  <br/> |
|[Schlüsselwörter](keywords-ex15websvcsotherref.md) <br/> |Gibt Stichwörter für eine Suche an.  <br/> |
|[Sprache](language.md) <br/> |Enthält die für die Suchabfrage verwendete Sprache.  <br/> |
|[Absender](senders.md) <br/> |Gibt ein Array von SMTP-Adressen an.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Gibt ein Array von Empfängern einer Nachricht an.  <br/> |
|[FromDate](fromdate.md) <br/> |Gibt das Datum an, an dem die Nachricht gesendet wurde.  <br/> |
|[ToDate](todate.md) <br/> |Gibt das Datum an, an dem die Nachricht empfangen wurde.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Gibt ein Array von Nachrichten an, die durchsucht werden sollen.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Gibt an, ob in gelöschten Elementen gesucht werden soll.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.  <br/> |
|[Parameter IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Gibt an, ob Elemente eingeschlossen werden sollen, die nicht durchsucht werden können.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

