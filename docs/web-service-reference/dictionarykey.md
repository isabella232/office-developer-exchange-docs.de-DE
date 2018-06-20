---
title: DictionaryKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DictionaryKey
api_type:
- schema
ms.assetid: f331c8ac-f1c7-4248-a570-97701969d5bf
description: Das DictionaryKey-Element gibt den Wörterbuchschlüssel für eine Wörterbucheigenschaft.
ms.openlocfilehash: 7e706f16fe155278ea56f303ffbb5971c1779879
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757981"
---
# <a name="dictionarykey"></a>DictionaryKey

Das **DictionaryKey** -Element gibt den Wörterbuchschlüssel für eine Wörterbucheigenschaft. 
  
```xml
<DictionaryKey>
   <Type/>
   <Value/>
</DictionaryKey>
```

 **UserConfigurationDictionaryObjectType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Typ (UserConfiguration)](type-userconfiguration.md) <br/> | Gibt ein Dictionary-Objekttyp an.<br/><br/>Der Typ kann eine der folgenden Werte vom Typ String sein:<br/><br/>-DateTime  <br/>-Boolean  <br/>-Byte  <br/>-Zeichenfolge  <br/>-Integer32  <br/>-UnsignedInteger32  <br/>-Integer64  <br/>-UnsignedInteger64  <br/>-StringArray  <br/>-ByteArray  <br/> |
|[Wert (UserConfiguration)](value-userconfiguration.md) <br/> |Gibt den Wert der Dictionary-Objekts als Zeichenfolge.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Der Wörterbucheintrag](dictionaryentry.md) <br/> |Gibt den Inhalt einer einzelnen Wörterbuch Eintrag-Eigenschaft.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

