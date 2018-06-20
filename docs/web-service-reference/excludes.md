---
title: Schließt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: Das Element ausgeschlossen führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert.
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758307"
---
# <a name="excludes"></a>Schließt

Das Element **ausgeschlossen** führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 **ExcludesType**
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
|[Bitmaske](bitmask.md) <br/> |Stellt eine hexadezimale oder decimal Maske, die während einer Einschränkung [ausgeschlossen](excludes.md) verwendet werden. Wenn die Bitmaske eine hexadezimale Zahl darstellt, muss es 0 X oder 0 X vorangestellt werden. Andernfalls wird er eine Dezimalzahl betrachtet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Einschränkung](restriction.md) <br/> |Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.  <br/> |
|[Und](and.md) <br/> |Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann. Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar. Das Element [oder](or.md) gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Ausgeschlossen** lösen auf **true fest,** Wenn eine AND-Operation für die folgenden auf 0 aufgelöst wird: 
  
1. Die bitweise Wert für die Eigenschaft
    
2. Der Bitmaskenwert für die-Eigenschaft
    
 **Ausgeschlossen** kann nur auf eine Eigenschaft angewendet werden, die einen ganzzahligen Wert hat. Wenn der Eigenschaftentyp etwas anderes als eine ganze Zahl ist, wird ein Fehlercode des **ErrorUnsupportedPathForQuery** in der Antwort zurückgegeben. 
  
Sie können den umgekehrten Vorgang durch Aufrufen von Not(Excludes) ausführen.
  
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

