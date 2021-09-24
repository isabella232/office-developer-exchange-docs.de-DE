---
title: PercentComplete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PercentComplete
api_type:
- schema
ms.assetid: 58a67f8a-c4dc-42dc-97ae-a9e5cc672d2d
description: Das PercentComplete-Element beschreibt den Abschlussstatus eines Vorgangs.
ms.openlocfilehash: 48e6163377d51d64f63e966c525def48f930733e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519247"
---
# <a name="percentcomplete"></a>PercentComplete

Das **PercentComplete-Element** beschreibt den Abschlussstatus eines Vorgangs. 
  
```xml
<PercentComplete/>
```

 **Doppel**
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
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl zwischen 0 und 100 darstellt, ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Festlegen von **PercentComplete** auf 100 hat die gleiche Auswirkung wie das Festlegen des [CompleteDate](completedate.md) -Elements oder das Festlegen des [Status](status.md) -Elements auf **Abgeschlossen**. In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt wird. Wenn **"PercentComplete"** beispielsweise "100", ["CompleteDate"](completedate.md) der 1. Januar 2007 und ["Status"](status.md) "NotStarted" ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der [Status](status.md) der Aufgabe auf "NotStarted", ["CompleteDate"](completedate.md) auf **"null"** und **"PercentComplete"** auf "0" festgelegt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
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

