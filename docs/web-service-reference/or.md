---
title: 'Oder:'
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: Das or-Element stellt einen Suchausdruck dar, der eine logische oder den darin enthaltenen Suchausdruck ausführt. Oder gibt true zurück, wenn eines der untergeordneten Elemente true zurückgibt. Oder muss mindestens zwei untergeordnete Elemente aufweisen.
ms.openlocfilehash: 9bc676da5bbaad64f11f6717fb487c2e9bcf2d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462479"
---
# <a name="or"></a>Oder:

Das **or** -Element stellt einen Suchausdruck dar, der eine logische **oder** den darin enthaltenen Suchausdruck ausführt. **Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen. 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 **Odertyp**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar. <br/><br/>Eines der folgenden Elemente muss **durch das Search** -Element ersetzt werden: <br/> <br/>- [Existiert](exists.md) <br/>- [Schließt](excludes.md) <br/>- [IsEqualTo](isequalto.md) <br/>- [IsNotEqualTo](isnotequalto.md) <br/>- [Isgreaterthan](isgreaterthan.md) <br/>- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/>- [IsLessThan](islessthan.md) <br/>- [IsLessThanOrEqualTo](islessthanorequalto.md) <br/>- [Enthält](contains.md) <br/>- [Nicht](not.md) <br/>- [Und](and.md) <br/>- **Oder** <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.  <br/> |
|[Not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert **und** eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis der **and-** Operation ist **true** , wenn alle im **and-** Element enthaltenen Suchausdrücke **true**sind.  <br/> |
|**- oder -** <br/> |Stellt einen Suchausdruck dar, der eine logische **or** -Operation für den darin enthaltenen Suchausdruck ausführt. **Oder** gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt. **Oder** muss mindestens zwei untergeordnete Elemente aufweisen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

