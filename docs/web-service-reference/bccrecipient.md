---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: Das BccRecipient-Element stellt einen Empfänger dar, der eine Blindkopie (BCC) einer e-Mail-Nachricht empfängt.
ms.openlocfilehash: 8296af1d74338bdfb1f4cb7bc7449ad91a9cd531
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461527"
---
# <a name="bccrecipient"></a>BccRecipient

Das **BccRecipient** -Element stellt einen Empfänger dar, der eine Blindkopie (BCC) einer e-Mail-Nachricht empfängt. 
  
```XML
<BccRecipient>true | false</BccRecipient>
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

Dieses Element kann entweder **true** oder **false**sein. Der Wert **true** gibt an, dass der Empfänger Blind Kohlenstoff kopiert ist; der Wert **false** gibt an, dass der Empfänger nicht Blind Carbon kopiert wird. 
  
## <a name="remarks"></a>Bemerkungen

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

