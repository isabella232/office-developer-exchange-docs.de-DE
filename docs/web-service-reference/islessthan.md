---
title: IsLessThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsLessThan
api_type:
- schema
ms.assetid: 2550469b-6e5d-45a5-9ecc-090d1b409296
description: Das IsLessThan-Element stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die erste Eigenschaft kleiner ist als die zweite.
ms.openlocfilehash: 374bfc20b86f99923034f126c3fd1fe9480fdf67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830040"
---
# <a name="islessthan"></a>IsLessThan

Das **IsLessThan** -Element darstellt, einen Suche-Ausdruck, der eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft vergleicht und gibt **true** zurück, wenn die erste Eigenschaft kleiner ist als die zweite. 
  
```xml
<IsLessThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsLessThan>
```

 **IsLessThanType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |MAPI-Eigenschaften identifiziert.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann. Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar. [Oder](or.md) wird true, wenn ein untergeordnetes Element true zurückgegeben werden, zurück. [Oder](or.md) muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

