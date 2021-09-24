---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: Das CompleteDate-Element stellt das Datum dar, an dem ein Element abgeschlossen wurde.
ms.openlocfilehash: 07f6034b4fd91d22ad07167d931bcd02a74782f9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518778"
---
# <a name="completedate"></a>CompleteDate

Das **CompleteDate-Element** stellt das Datum dar, an dem ein Element abgeschlossen wurde. 
  
```xml
<CompleteDate/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[Wert](flag.md) <br/> |Gibt ein Flag für ein Postfachelement an.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der Datum und Uhrzeit darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Festlegen von **CompleteDate** hat den gleichen Effekt wie das Festlegen von [PercentComplete](percentcomplete.md) auf 100 oder [Status](status.md) auf **Abgeschlossen**. In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt wird. Wenn ["PercentComplete"](percentcomplete.md) beispielsweise "100", **"CompleteDate"** der 1. Januar 2007 und ["Status"](status.md) **"NotStarted"** ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der [Status](status.md) der Aufgabe auf **"NotStarted",** ["CompleteDate"](completedate.md) auf **"null"** und ["PercentComplete"](percentcomplete.md) auf "0" festgelegt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Deleting Tasks](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

