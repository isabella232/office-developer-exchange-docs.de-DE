---
title: IsGreaterThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsGreaterThanOrEqualTo
api_type:
- schema
ms.assetid: 373cc954-314d-40e2-be03-cc08aefc0d5b
description: Das IsGreaterThanOrEqualTo-Element stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und "true" zurückgibt, wenn die erste Eigenschaft größer oder gleich der zweiten ist.
ms.openlocfilehash: 97ea04f60e5a7d03d4b495feb58dc2f597e2a4ea
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532795"
---
# <a name="isgreaterthanorequalto"></a>IsGreaterThanOrEqualTo

Das **IsGreaterThanOrEqualTo-Element** stellt einen Suchausdruck dar, der eine Eigenschaft mit einem Konstantenwert oder einer anderen Eigenschaft vergleicht und **"true"** zurückgibt, wenn die erste Eigenschaft größer oder gleich der zweiten ist. 
  
```xml
<IsGreaterThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

**IsGreaterThanOrEqualToType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Mitglieder eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen And-Vorgang zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis des And-Vorgangs ist **"true",** wenn alle in "And" enthaltenen Suchausdrücke **"True"** sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der ein logisches OR für den darin enthaltenen Suchausdruck ausführt. [Oder](or.md) gibt "true" zurück, wenn eines seiner untergeordneten Elemente "true" zurückgibt. [Oder](or.md) es müssen zwei oder mehr untergeordnete Elemente vorhanden sein.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

