---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: Das CanDelete-Element gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.
ms.openlocfilehash: ad7e573aeb2bb72d19f05421d0eab5a2f6ac5539
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515999"
---
# <a name="candelete"></a>CanDelete

Das **CanDelete-Element** gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann. 
  
```xml
<CanDelete/>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element vorhanden ist, ist ein Textwert erforderlich, der einen booleschen Wert darstellt. Der Wert **"true"** gibt an, dass der Ordner gelöscht werden kann. Der Wert **"false"** bedeutet, dass der Ordner nicht gelöscht werden kann. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Löschen eines verwalteten Ordners den [DeleteFolder-Vorgang.](deletefolder-operation.md)
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Löschen von Ordnern](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

