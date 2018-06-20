---
title: String
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: Das String-Element darstellt, eine Zeichenfolge, die von Elementen, Kontakte, Aufgaben und Unterhaltungen verwendet wird.
ms.openlocfilehash: 66260c7ebcb56049a78c5eddbe057dfa8d61f193
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831607"
---
# <a name="string"></a>String

Das **String** -Element darstellt, eine Zeichenfolge, die von Elementen, Kontakte, Aufgaben und Unterhaltungen verwendet wird. 
  
```XML
<String/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die angeben, welche, die Kategorien ein Elements im Postfach gehört.  <br/> |
|[Children](children.md) <br/> |Enthält die Namen der untergeordneten Elemente eines Kontakts.  <br/> |
|[Companies](companies.md) <br/> |Stellt die Auflistung der Unternehmen, die einen Kontakt oder eine Aufgabe zugeordnet sind.  <br/> |
|[Kontakte](contacts-ex15websvcsotherref.md) <br/> |Enthält eine Liste von Kontakten, die mit einem Vorgang verknüpft sind.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Enthält eine Liste von allen Absendern von Unterhaltungselementen im Postfach.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung ungelesen in allen Ordnern im Postfach sind.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Enthält eine Liste der Artikelklassen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein muss.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Enthält eine Liste mit den Nachrichtenklassifikationen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein muss.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Enthält die Liste der Empfänger der Unterhaltung. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert der dieses Element ist eine Zeichenfolge, die eine Kategorie, die das untergeordnete Element eines Kontakts, einer Firma, einem eindeutigen Empfänger einer Unterhaltung oder einen Kontakt, der mit einer Aufgabe verbunden ist darstellt.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation Operation](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

