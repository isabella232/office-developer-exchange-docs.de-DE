---
title: HiddenRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HiddenRecipient
api_type:
- schema
ms.assetid: a8209f75-0070-4424-8dcd-273cfd192728
description: Das HiddenRecipient-Element gibt an, dass der Empfänger von einer Organisationsrichtlinie hinzugefügt wurde, die vor nicht privilegierten Benutzern ausgeblendet werden soll.
ms.openlocfilehash: 24d7dcad5b8b744351804160ef8d9988b9e393a3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539689"
---
# <a name="hiddenrecipient"></a>HiddenRecipient

Das **HiddenRecipient-Element** gibt an, dass der Empfänger von einer Organisationsrichtlinie hinzugefügt wurde, die vor nicht privilegierten Benutzern ausgeblendet werden soll. 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
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
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.  <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element kann entweder **"true"** oder **"false" sein.** Der Wert **"true"** gibt an, dass der Benutzer von einer Organisationsrichtlinie hinzugefügt wurde. Der Wert **"false"** gibt an, dass der Benutzer nicht von einer Organisationsrichtlinie hinzugefügt wurde. 
  
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

