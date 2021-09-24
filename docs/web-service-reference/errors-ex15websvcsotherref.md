---
title: Fehler
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Errors
api_type:
- schema
ms.assetid: ea37a2b5-e2d1-4089-960f-7014b9535a50
description: Das Errors-Element enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.
ms.openlocfilehash: 9a5aba212aefbddbd2a85377e61449d2da408368
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520570"
---
# <a name="errors"></a>Fehler

Das **Errors-Element** enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden. 
  
[FindMessageTrackingReport](findmessagetrackingreport.md)
  
[Fehler](errors-ex15websvcsotherref.md)
  
```xml
<Errors>
   <Properties/>
</Errors>
```

 **ArrayOfArraysOfTrackingPropertiesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Enthält eine Liste einer oder mehrerer Nachverfolgungseigenschaften.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [FindMessageTrackingReport-Vorgangsanforderung.](findmessagetrackingreport-operation.md)  <br/> |
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

