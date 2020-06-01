---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: Das MessageTrackingSearchResult-Element enthält ein einzelnes Nachrichten Ergebnis für ein FindMessageTrackingReportResponse-Element.
ms.openlocfilehash: 27e70cd9e11b480ab6bbb9b28275f142da7c76ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466682"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

Das **MessageTrackingSearchResult** -Element enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element. 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 **FindMessageTrackingSearchResultType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Betreff](subject.md) <br/> |Enthält den Betreff der e-Mail-Nachricht.  <br/> |
|[Absender (e-mailemailtype)](sender-emailaddresstype.md) <br/> |Enthält die Adresse des Absenders des e-Mail-Nachrichten.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.  <br/> |
|[Recipients (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Enthält eine Liste der e-Mail-Adressen, die diese Nachricht erhalten haben.  <br/> |
|[Übermittelt](submittedtime.md) <br/> |Enthält die Zeit, zu der die Nachricht übermittelt wurde.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Enthält eine interne ID, die die Nachricht in der Transportdatenbank identifiziert.  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuvor akzeptiert hat.  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuerst akzeptiert hat.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |Enthält eine Liste der Nachrichten, die den Suchkriterien entsprechen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

