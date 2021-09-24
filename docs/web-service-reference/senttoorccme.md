---
title: SentToOrCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SentToOrCcMe
api_type:
- schema
ms.assetid: ca43e05d-df37-485b-9276-34678025f2b7
description: Das SentToOrCcMe-Element gibt an, ob sich der Besitzer des Postfachs in einer ToRecipients- oder CcRecipients-Eigenschaft eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 0e9dddf53c2b671613a5a4c20e3b845a5d38c247
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510890"
---
# <a name="senttoorccme"></a>SentToOrCcMe

Das **SentToOrCcMe-Element** gibt an, ob sich der Besitzer des Postfachs in einer **ToRecipients-** oder **CcRecipients-Eigenschaft** eingehender Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<SentToOrCcMe>true | false</SentToOrCcMe>
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

Der Textwert **"true"** gibt an, dass sich der Besitzer des Postfachs in der **ToRecipients-** oder **CcRecipients-Eigenschaft** der eingehenden Nachrichten befinden muss, damit die Bedingung oder Ausnahme zutrifft. Der Wert **"false"** gibt an, dass sich der Besitzer des Postfachs nicht in der **ToRecipients-** oder **CcRecipients-Eigenschaft** der eingehenden Nachrichten befinden darf, damit die Bedingung oder Ausnahme zutrifft. 
  
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

