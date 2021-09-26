---
title: Bitmaske
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: Das Bitmask-Element steht eine Hexadezimal- oder Dezimalmaske dar, die während eines Schließt-Einschränkungsvorgangs verwendet wird.
ms.openlocfilehash: 83307fc7f5ba328c5d6f7574a8b3be1ea25595f3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543590"
---
# <a name="bitmask"></a>Bitmaske

Das **Bitmask**-Element steht eine Hexadezimal- oder Dezimalmaske dar, die während eines [Schließt](excludes.md)-Einschränkungsvorgangs verwendet wird. 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Wert** | Stellt eine Dezimal- bzw. Hexadezimal-Bitmaske dar. Der Wert wird durch den folgenden regulären Ausdruck dargestellt:<br/>`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.<br/><br/>Nachfolgend sehen Sie Beispiele für Hexadezimalwerte für dieses Attribut:<br/>- 0x12AF<br/>- 0X334AE<br/><br/>Nachfolgend sehen Sie Beispiele für Dezimalwerte für dieses Attribut:<br/>- 10<br/>- 255<br/>- 4562 |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Schließt](excludes.md) <br/> |Führt eine bitweise Maske der Eigenschaften aus.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Hexadezimale Werte müssen die Präfix 0x oder 0X aufweisen. Wenn diese Präfix nicht vorhanden ist, wird davon ausgegangen, dass der Wert eine Dezimalzahl sein.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

