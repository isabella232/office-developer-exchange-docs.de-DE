---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: Das GetMessageTrackingReport-Element enthält die Anforderung für den Vorgang GetMessageTrackingReport zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758738"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

Das **GetMessageTrackingReport** -Element enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID. 
  
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
|[Bereich (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Gibt an, wo die Suche durchzuführen. Dieses Element ist erforderlich.  <br/> |
|[Berichtsvorlage](reporttemplate.md) <br/> |Gibt den Typ der laufenden Bericht abgerufen. Dieses Element ist erforderlich.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Gibt eine Empfängeradresse mit den angegebenen Nachrichtenverfolgungsbericht verwenden. Dieses Element ist optional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Gibt eine Identitätszeichenfolge, die aus der **FindMessageTrackingReport** -Operation abgerufen wurde. Dieses Element ist erforderlich.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Gibt an, dass die Person, die die Aufgabe ausgeführt wird, eine privilegierte Rolle wurde. Dieses Element ist optional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Gibt die Timing und Leistungsinformationen, die verwendet wird, um den Nachrichtenverfolgungsbericht abgeleitet werden. Dieses Element ist optional.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Gibt eine Liste der Eigenschaften für eine oder mehrere Tracking an. Dieses Element ist optional.  <br/> |
   
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
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

