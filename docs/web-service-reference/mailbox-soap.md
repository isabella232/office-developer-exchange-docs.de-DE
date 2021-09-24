---
title: Postfach (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4ad59e5b-4047-4c34-a318-ca06c31d3de8
description: Das Mailbox-Element enthält die E-Mail-Adresse des Benutzers, der ermittelt werden soll.
ms.openlocfilehash: 6349a28b7ed97cfaa2bb8ef8f68d93e16d81c377
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514284"
---
# <a name="mailbox-soap"></a>Postfach (SOAP)

Das **Mailbox-Element** enthält die E-Mail-Adresse des Benutzers, der ermittelt werden soll. 
  
```XML
<Mailbox/>
```

**Zeichenfolge**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer (SOAP)](user-soap.md) <br/> |Stellt die Identität eines einzelnen Benutzers dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Postfachelements** ist die E-Mail-Adresse des Benutzers, der ermittelt werden soll. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

