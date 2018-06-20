---
title: Status
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 80121e41-291b-4fc0-a55e-6f677d4b5fb5
description: Status-Element, das den Status eines Aufgabenelements darstellt.
ms.openlocfilehash: 224b61913a5ae8e5b4aa0d756a9f2488df2741bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831584"
---
# <a name="status"></a>Status

**Status** -Element, das den Status eines Aufgabenelements darstellt. 
  
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
  
- Nicht gestartet
    
- InProgress
    
- Completed
    
- WaitingOnOthers
    
- Zurückgestellt
    
## <a name="remarks"></a>Hinweise

Festlegen von [CompleteDate](completedate.md) hat die gleiche Auswirkung wie das [PercentComplete](percentcomplete.md) auf 100 oder **Status** auf **abgeschlossen**festlegen. In einer Anforderung, dass mindestens zwei Sätze von diesen Eigenschaften, die letzte verarbeitete-Eigenschaft den Wert bestimmt wird, der für diese Elemente festgelegt ist. Beispielsweise **PercentComplete** 100 **CompleteDate** ist, 1/1/2007 und **Status** ist nicht gestartet, und die Eigenschaften in dieser Reihenfolge gestreamt werden, der Effekt wird der **Status** des Vorgangs auf nicht gestartet, die **CompleteDate festgelegt werden **auf **null**und die **PercentComplete** auf 0. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Erstellen von Aufgaben](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Deleting Tasks](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

