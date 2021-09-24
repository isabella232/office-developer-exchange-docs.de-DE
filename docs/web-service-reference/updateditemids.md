---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: Das UpdatedItemIds-Element gibt die Bezeichner der aktualisierten Erinnerungselemente an.
ms.openlocfilehash: 59e17e32d5df3f8a6000b05899f2fe0c5de2ec00
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538611"
---
# <a name="updateditemids"></a>UpdatedItemIds

Das **UpdatedItemIds-Element** gibt die Bezeichner der aktualisierten Erinnerungselemente an. 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 **NonEmptyArrayOfItemIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ItemId](itemid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[PerformReminderActionResponse](performreminderactionresponse.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Wenn der [PerformReminderAction-Vorgang](performreminderaction-operation.md) nicht erfolgreich abgeschlossen wurde oder keine Änderungen auf dem Server vorgenommen wurden, wird das **UpdatedItemIds-Element** als leerer Wert zurückgegeben. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PerformReminderActionResponse](performreminderactionresponse.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

