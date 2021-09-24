---
title: Status
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: Das Status-Element stellt den Status eines Aufgabenelements dar.
ms.openlocfilehash: 5ec50e3f0c06ad3ec8301ddbe8e7bd249b1e8fe9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525540"
---
# <a name="status"></a>Status

Das **Status-Element** stellt den Status eines Aufgabenelements dar. 
  
```xml
<Status/>
```

 **TaskStatusType**
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

Ein Textwert ist erforderlich. Es folgen die möglichen Textwerte für dieses Element:
  
- NotStarted
    
- InProgress
    
- Abgeschlossen
    
- WaitingOnOthers
    
- Latent
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Festlegen von [CompleteDate](completedate.md) hat den gleichen Effekt wie das Festlegen von [PercentComplete](percentcomplete.md) auf 100 oder **Status** auf **Abgeschlossen**. In einer Anforderung, die mindestens zwei dieser Eigenschaften festlegt, bestimmt die zuletzt verarbeitete Eigenschaft den Wert, der für diese Elemente festgelegt wird. Wenn **PercentComplete** beispielsweise 100 ist, **CompleteDate** 1/1/2007 ist und **Status** NotStarted ist und die Eigenschaften in dieser Reihenfolge gestreamt werden, wird der **Status** der Aufgabe auf NotStarted, das **CompleteDate** auf **NULL** und das **PercentComplete** auf 0 festgelegt. 
  
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

