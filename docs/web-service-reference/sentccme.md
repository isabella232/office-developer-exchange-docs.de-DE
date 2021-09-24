---
title: SentCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SentCcMe
api_type:
- schema
ms.assetid: bf5044e4-cbdf-4e24-a16f-b6454a51fcd5
description: Das SentCcMe-Element gibt an, ob sich der Besitzer des Postfachs in der CcRecipients-Eigenschaft eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 82123a44cccf953bf1db6dfaf916d4ebf851851e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521522"
---
# <a name="sentccme"></a>SentCcMe

Das **SentCcMe-Element** gibt an, ob sich der Besitzer des Postfachs in der **CcRecipients-Eigenschaft** eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<SentCcMe>true | false</SentCcMe>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt alle verfügbaren Regelausnahmebedingungen für eine Posteingangsregel dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** gibt an, dass sich der Besitzer des Postfachs in der **CcRecipients-Eigenschaft** der eingehenden Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft. Der Wert **"false"** gibt an, dass sich der Besitzer des Postfachs nicht in der **CcRecipients-Eigenschaft** der eingehenden Nachrichten befinden darf, damit die Bedingung oder Ausnahme zutrifft. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

