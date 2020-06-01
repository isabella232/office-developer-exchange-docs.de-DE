---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: Das TextBody-Element gibt den Textkörper an.
ms.openlocfilehash: c0002785fb990a251267218f7a5f232e521db41a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459483"
---
# <a name="textbody"></a>TextBody

Das **TextBody** -Element gibt den Textkörper an. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyTypeType  <br/> |Gibt den Typ des Texts an. Der Wert des **Texts** für das **BodyTypeType** -Attribut gibt an, dass sich der Text im nur-Text-Format befindet. Der Wert von **HTML** für das **BodyTypeType** -Attribut gibt an, dass sich der Text im HTML-Format befindet. Das **BodyTypeType** -Attribut ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Textkörper Inhalt abgeschnitten wurde. Der Textwert **false** für das Attribut **IsTruncated** gibt an, dass der Inhalt des Texts nicht abgeschnitten wurde. Der normalisierte Text wird abgeschnitten, wenn die Textkörper Länge länger ist als der im [MaximumBodySize](maximumbodysize.md) -Element festgelegte Wert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [Verteilerliste](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der TextText-Wert des **TextBody** -Elements ist der Textkörper des Elements. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

