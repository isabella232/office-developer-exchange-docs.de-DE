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
description: Das MessageTrackingReport-Element enthält eine Nachricht, die in einem Vorgang GetMessageTrackingReport zurückgegeben wird.
ms.openlocfilehash: d01e0fbf099d096c7f255a8e94070e330577e6ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830457"
---
# <a name="messagetrackingreport"></a>MessageTrackingReport

Das **MessageTrackingReport** -Element enthält eine Nachricht, die in einem [Vorgang GetMessageTrackingReport](getmessagetrackingreport-operation.md)zurückgegeben wird.
  
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
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Kontaktinformationen für den Absender der E-mail-Nachricht enthält.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der E-mail-Nachricht.  <br/> |
|[SubmitTime](submittime.md) <br/> |Enthält die Tageszeit, die die e-Mail-Nachricht gesendet wurde.  <br/> |
|[OriginalRecipients](originalrecipients.md) <br/> |Enthält eine Liste der Empfänger der E-mail-Nachricht.  <br/> |
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Enthält eine Liste mit mindestens einen Tracking-Ereignissen für die Empfänger an.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Enthält das Ergebnis einer einzelnen Anforderung [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)
  
[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

