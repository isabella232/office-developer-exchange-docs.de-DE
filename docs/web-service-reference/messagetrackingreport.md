---
title: MessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: Das MessageTrackingReport-Element enthält eine einzelne Nachricht, die in einer GetMessageTrackingReport-Operation zurückgegeben wird.
ms.openlocfilehash: fc3e56fbb1bee411fa31751f558f520874133076
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463216"
---
# <a name="messagetrackingreport"></a>MessageTrackingReport

Das **MessageTrackingReport** -Element enthält eine einzelne Nachricht, die in einer [GetMessageTrackingReport-Operation](getmessagetrackingreport-operation.md)zurückgegeben wird.
  
```XML
<MessageTrackingReport>
   <Sender/>
   <PurportedSender/>
   <Subject/>
   <SubmitTime/>
   <OriginalRecipients/>
   <RecipientTrackingEvents/>
   <Properties/>
</MessageTrackingReport>
```

 **MessageTrackingReportType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Absender (e-mailemailtype)](sender-emailaddresstype.md) <br/> |Enthält Kontaktinformationen für den Absender der e-Mail-Nachricht.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der e-Mail-Nachricht.  <br/> |
|[Übermittlungs Zeitangabe](submittime.md) <br/> |Enthält die Tageszeit, zu der die e-Mail-Nachricht gesendet wurde.  <br/> |
|[Element originalrecipients](originalrecipients.md) <br/> |Enthält eine Liste der Empfänger der e-Mail-Nachricht.  <br/> |
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Enthält eine Liste mit einem oder mehreren Überwachungsereignissen für die Empfänger.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Enthält das Ergebnis einer einzelnen [GetMessageTrackingReport-Vorgangs](getmessagetrackingreport-operation.md) Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)
  
[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

