---
title: Excludes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: Das Excludes-Element führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert aus.
ms.openlocfilehash: 7923c31a4a1fea0270c9a4372072d7b0a3b79c76
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510141"
---
# <a name="excludes"></a>Excludes

Das **Excludes-Element** führt eine bitweise Maske der angegebenen Eigenschaft und einen angegebenen Wert aus. 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
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
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Mitglieder eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifies MAPI properties.  <br/> |
|[Bitmaske](bitmask.md) <br/> |Stellt eine Hexadezimal- oder Dezimalmaske dar, die während eines [Excludes-Einschränkungsvorgangs](excludes.md) verwendet werden soll. Wenn die Bitmaske eine Hexadezimalzahl darstellt, muss ihr das Präfix 0x oder 0X vorangestellt werden. Andernfalls wird sie als Dezimalzahl betrachtet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[not](not.md) <br/> |Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.  <br/> |
|[Und](and.md) <br/> |Stellt einen Suchausdruck dar, mit dem Sie einen booleschen And-Vorgang zwischen zwei oder mehr Suchausdrücken ausführen können. Das Ergebnis des And-Vorgangs ist **"true",** wenn alle in "And" enthaltenen Suchausdrücke **"True"** sind.  <br/> |
|[- oder -](or.md) <br/> |Stellt einen Suchausdruck dar, der ein logisches OR für den darin enthaltenen Suchausdruck ausführt. Das [Or-Element](or.md) gibt **"true"** zurück, wenn eines seiner untergeordneten Elemente **"true"** zurückgibt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

**"Excludes"** wird in **"true"** aufgelöst, wenn ein and-Vorgang, der für Folgendes ausgeführt wird, in 0 aufgelöst wird: 
  
1. Der bitweise Wert für die Eigenschaft
    
2. Der Bitmaskenwert für die Eigenschaft
    
**Ausschlüsse** können nur auf eine Eigenschaft angewendet werden, die einen ganzzahligen Wert aufweist. Wenn es sich bei dem Eigenschaftstyp um eine andere als eine ganze Zahl handelt, wird in der Antwort ein Fehlercode von **ErrorUnsupportedPathForQuery** zurückgegeben. 
  
Sie können den umgekehrten Vorgang ausführen, indem Sie Not(Excludes) aufrufen.
  
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

