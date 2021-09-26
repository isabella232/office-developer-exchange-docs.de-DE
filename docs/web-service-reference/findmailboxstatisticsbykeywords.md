---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: Das FindMailboxStatisticsByKeywords-Element gibt eine Anforderung an, nach Postfachstatistiken nach Schlüsselwort zu suchen.
ms.openlocfilehash: 3f84b0c3bb2a4a0a2a164b9e9120c3505073417e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546504"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

Das **FindMailboxStatisticsByKeywords-Element** gibt eine Anforderung an, nach Postfachstatistiken nach Schlüsselwort zu suchen. 
  
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
|[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Enthält ein Array von Postfächern, die von der Aufbewahrung betroffen sind.  <br/> |
|[Schlüsselwörter](keywords-ex15websvcsotherref.md) <br/> |Gibt Schlüsselwörter für eine Suche an.  <br/> |
|[Language](language.md) <br/> |Enthält die Sprache, die für die Suchabfrage verwendet wird.  <br/> |
|[Absender](senders.md) <br/> |Gibt ein Array von SMTP-Adressen an.  <br/> |
|[Empfänger (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Gibt ein Array von Empfängern einer Nachricht an.  <br/> |
|[FromDate](fromdate.md) <br/> |Gibt das Datum an, an dem die Nachricht gesendet wurde.  <br/> |
|[ToDate](todate.md) <br/> |Gibt das Datum an, an dem die Nachricht empfangen wurde.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Gibt ein Array von Nachrichten an, die durchsucht werden sollen.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Gibt an, ob gelöschte Elemente gesucht werden sollen.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Gibt an, ob Elemente eingeschlossen werden sollen, die nicht durchsucht werden können.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

