---
title: DictionaryKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DictionaryKey
api_type:
- schema
ms.assetid: f331c8ac-f1c7-4248-a570-97701969d5bf
description: Das DictionaryKey-Element gibt den Wörterbuchschlüssel für eine Wörterbucheigenschaft an.
ms.openlocfilehash: feae35d292c212b41394f63c0840ec4d3c3b8800
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519779"
---
# <a name="dictionarykey"></a>DictionaryKey

Das **DictionaryKey-Element** gibt den Wörterbuchschlüssel für eine Wörterbucheigenschaft an. 
  
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
|[Typ (UserConfiguration)](type-userconfiguration.md) <br/> | Gibt einen Wörterbuchobjekttyp an.<br/><br/>Der Typ kann einer der folgenden Zeichenfolgenwerte sein:<br/><br/>- DateTime  <br/>- Boolean  <br/>- Byte  <br/>- Zeichenfolge  <br/>- Ganze Zahl32  <br/>- UnsignedInteger32  <br/>- Integer64  <br/>- UnsignedInteger64  <br/>- StringArray  <br/>- ByteArray  <br/> |
|[Wert (UserConfiguration)](value-userconfiguration.md) <br/> |Gibt den Wert des Wörterbuchobjekts als Zeichenfolge an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DictionaryEntry](dictionaryentry.md) <br/> |Gibt den Inhalt einer einzelnen Wörterbucheintragseigenschaft an.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

