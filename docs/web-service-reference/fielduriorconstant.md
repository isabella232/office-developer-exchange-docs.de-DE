---
title: FieldURIOrConstant
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: Das Element FieldURIOrConstant stellt eine Eigenschaft oder einen konstanten Wert beim Vergleich mit einer anderen Eigenschaft verwendet werden.
ms.openlocfilehash: 5195feec2a314d9ec15dc4a25a7a014aded1696a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758419"
---
# <a name="fielduriorconstant"></a>FieldURIOrConstant

Das Element **FieldURIOrConstant** stellt eine Eigenschaft oder einen konstanten Wert beim Vergleich mit einer anderen Eigenschaft verwendet werden. 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

 **FieldURIOrConstantType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konstante](constant.md) <br/> |Gibt einen konstanten Wert in einer Einschränkung.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |MAPI-Eigenschaften identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|["IsEqualTo"](isequalto.md) <br/> |Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und wird zu True ausgewertet, falls diese gleich sind.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft größer ist.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft größer als oder gleich dem zweiten Wert oder-Eigenschaft ist.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die erste Eigenschaft kleiner als der zweite Wert oder -Eigenschaft ist zurück.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die erste Eigenschaft kleiner oder gleich dem zweiten Wert oder-Eigenschaft ist zurück.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die Werte nicht identisch sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="example"></a>Beispiel

Das folgende XML-Beispiel zeigt das FieldURIOrConstant-Element mit einer Konstante und die URI-Feld verwendet.
  
```
[xml]
<Restriction>
  <Or xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

