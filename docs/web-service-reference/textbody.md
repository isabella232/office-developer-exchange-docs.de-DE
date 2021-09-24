---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: Das TextBody-Element gibt den Textkörper an.
ms.openlocfilehash: 5dfc0aa76f0b0778d785e46fe12259c4a226b89f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515180"
---
# <a name="textbody"></a>TextBody

Das **TextBody-Element** gibt den Textkörper an. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyTypeType  <br/> |Gibt den Textkörpertyp an. Der Wert von **Text** für das **BodyTypeType-Attribut** gibt an, dass sich der Textkörper in Nur-Text-Form befindet. Der **HTML-Wert** für das **BodyTypeType-Attribut** gibt an, dass sich der Textkörper im HTML-Format befindet. Das **BodyTypeType-Attribut** ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Textkörperinhalt abgeschnitten wurde. Der Textwert **"false"** für das **IsTruncated-Attribut** gibt an, dass der Textkörperinhalt nicht abgeschnitten wurde. Der normalisierte Textkörper wird abgeschnitten, wenn die Textkörperlänge länger als der im [MaximumBodySize-Element](maximumbodysize.md) festgelegte Wert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md)  |  [Kontakt](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **TextBody-Elements** ist der Textkörper des Elements. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

