---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: Das GetMessageTrackingReport-Element enthält die Anforderung für den GetMessageTrackingReport-Vorgang zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.
ms.openlocfilehash: cdf4e2c0f17c7d723dc56f30c445bfd527f891a3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516979"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

Das **GetMessageTrackingReport-Element** enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID. 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 **GetMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bereich (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Gibt an, wo die Suche ausgeführt werden soll. Dieses Element ist erforderlich.  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |Gibt den Typ des abzurufenden Nachverfolgungsberichts an. Dieses Element ist erforderlich.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Gibt eine Empfängeradresse an, die mit dem angegebenen Nachverfolgungsbericht verwendet werden soll. Dieses Element ist optional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Gibt eine Identitätszeichenfolge an, die aus dem **FindMessageTrackingReport-Vorgang** abgerufen wurde. Dieses Element ist erforderlich.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Gibt an, dass die Person, die die Aufgabe ausführt, über eine privilegierte Rolle verfügt. Dieses Element ist optional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Gibt Timing- und Leistungsinformationen an, die zum Ableiten des Nachverfolgungsberichts verwendet werden. Dieses Element ist optional.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Gibt eine Liste einer oder mehrerer Nachverfolgungseigenschaften an. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

