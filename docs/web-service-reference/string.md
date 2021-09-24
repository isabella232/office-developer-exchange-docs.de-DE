---
title: String
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: Das String-Element stellt eine Zeichenfolge dar, die von Elementen, Kontakten, Aufgaben und Unterhaltungen verwendet wird.
ms.openlocfilehash: dd85cae34ddf829f00660c8b87feb9331505183c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509294"
---
# <a name="string"></a>String

Das **String-Element** stellt eine Zeichenfolge dar, die von Elementen, Kontakten, Aufgaben und Unterhaltungen verwendet wird. 
  
```XML
<String/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die angeben, zu welchen Kategorien ein Element im Postfach gehört.  <br/> |
|[Children](children.md) <br/> |Enthält die Namen der untergeordneten Elemente eines Kontakts.  <br/> |
|[Companies](companies.md) <br/> |Stellt die Sammlung von Unternehmen dar, die einem Kontakt oder einer Aufgabe zugeordnet sind.  <br/> |
|[Kontakte](contacts-ex15websvcsotherref.md) <br/> |Enthält eine Liste der Kontakte, die einem Vorgang zugeordnet sind.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung, die über ein Postfach aggregiert wurde.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in allen Ordnern im Postfach ungelesen sind.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Enthält eine Liste der Elementklassen, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Enthält eine Liste der Nachrichtenklassifizierungen, die für eingehende Nachrichten gestempelt werden müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Enthält die Liste der Empfänger der Unterhaltung. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert dieses Elements ist eine Zeichenfolge, die eine Kategorie, das untergeordnete Element eines Kontakts, ein Unternehmen, einen eindeutigen Empfänger einer Unterhaltung oder einen Kontakt darstellt, der einer Aufgabe zugeordnet ist.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation-Vorgang](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

