---
title: MessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: Das MessageTrackingReport-Element enthält eine einzelne Nachricht, die in einem GetMessageTrackingReport-Vorgang zurückgegeben wird.
ms.openlocfilehash: aa55bb9e4f81a4cc0586d7258720aefd743923fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539353"
---
# <a name="messagetrackingreport"></a>MessageTrackingReport

Das **MessageTrackingReport** -Element enthält eine einzelne Nachricht, die in einem [GetMessageTrackingReport -Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.
  
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
|[Absender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Enthält Kontaktinformationen für den Absender der E-Mail-Nachricht.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Enthält Kontaktinformationen für den Absender einer E-Mail-Nachricht.  <br/> |
|[Betreff](subject.md) <br/> |Enthält den Betreff der E-Mail-Nachricht.  <br/> |
|[SubmitTime](submittime.md) <br/> |Enthält die Uhrzeit, zu der die E-Mail-Nachricht gesendet wurde.  <br/> |
|[OriginalRecipients](originalrecipients.md) <br/> |Enthält eine Liste der Empfänger der E-Mail-Nachricht.  <br/> |
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Enthält eine Liste mit einem oder mehreren Nachverfolgungsereignissen für die Empfänger.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste einer oder mehrerer Nachverfolgungseigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Enthält das Ergebnis einer einzelnen [GetMessageTrackingReport-Vorgangsanforderung.](getmessagetrackingreport-operation.md)  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)
  
[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

