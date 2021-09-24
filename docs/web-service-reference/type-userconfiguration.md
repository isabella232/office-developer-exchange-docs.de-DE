---
title: Typ (UserConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Type
api_type:
- schema
ms.assetid: d09a9621-6950-451a-90dc-920af9cab35c
description: Das Type-Element gibt einen Wörterbuchobjekttyp an.
ms.openlocfilehash: f0bafa9023a42fdf8464891e8df7931a0766b416
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538730"
---
# <a name="type-userconfiguration"></a>Typ (UserConfiguration)

Das **Type-Element** gibt einen Wörterbuchobjekttyp an. 
  
```xml
<Type>DateTime or Boolean or Byte or String or Integer32 or UnsignedInteger32 or Integer64 or UnsignedInteger64 or StringArray or ByteArray</Type> 
```

 **UserConfigurationDictionaryObjectTypesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DictionaryKey](dictionarykey.md) <br/> |Gibt den Wörterbuchschlüssel für eine Wörterbucheigenschaft an.  <br/> |
|[DictionaryValue](dictionaryvalue.md) <br/> |Gibt den Wörterbuchwert für eine Wörterbucheigenschaft an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **Type-Element** aufgeführt. 
  
**Type-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|DateTime  <br/> ||
|Boolesch  <br/> ||
|Byte  <br/> ||
|String  <br/> ||
|Ganze Zahl32  <br/> ||
|UnsignedInteger32  <br/> ||
|Ganze Zahl64  <br/> ||
|UnsignedInteger64  <br/> ||
|StringArray  <br/> ||
|ByteArray  <br/> ||
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

