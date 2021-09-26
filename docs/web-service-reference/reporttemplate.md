---
title: ReportTemplate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: Das ReportTemplate-Element stellt den Typ des abzurufenden Berichts dar.
ms.openlocfilehash: 18fc98a8d9aaa777a590561aedd4e86fdf91f9af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542800"
---
# <a name="reporttemplate"></a>ReportTemplate

Das **ReportTemplate-Element** stellt den Typ des abzurufenden Berichts dar. 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 **MessageTrackingReportTemplateType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **ReportTemplate-Element** aufgeführt. 
  
**ReportTemplate-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Zusammenfassung  <br/> |Gibt an, dass im Bericht alle Empfänger der Nachricht und der Zustellungsstatus der Nachricht an jeden Empfänger angezeigt werden.  <br/> |
|RecipientPath  <br/> |Gibt an, dass der Bericht für einen einzelnen Empfänger einen vollständigen Verlauf der aufgetretenen Ereignisse anzeigt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

