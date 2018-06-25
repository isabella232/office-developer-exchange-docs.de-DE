---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: Das TextBody-Element gibt den Textkörper.
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839176"
---
# <a name="textbody"></a>TextBody

Das **TextBody** -Element gibt den Textkörper. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyTypeType  <br/> |Gibt den Typ des Hauptteils an. Der Wert der **Text** für das **BodyTypeType** -Attribut gibt an, dass der Text in nur-Text-Format ist. Der Wert von **HTML** für das **BodyTypeType** -Attribut gibt an, dass der Textkörper in HTML-Formular ist. Das Attribut **BodyTypeType** ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Inhalt des Body abgeschnitten worden sein. Der Textwert **false** für das **IsTruncated** -Attribut gibt an, dass der Inhalt des Body nicht abgeschnitten worden sein. Normalisierte Textkörper werden abgeschnitten, wenn die Länge des Hauptteils Text länger als der Wert im [MaximumBodySize](maximumbodysize.md) -Element festgelegt ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md) | [Kontakt](contact.md) | [Nachricht](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **TextBody** -Elements ist der Textkörper des Elements. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

