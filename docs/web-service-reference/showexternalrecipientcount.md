---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: Das ShowExternalRecipientCount-Element gibt an, ob Consumer des GetMailTips-Vorgangs e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird.
ms.openlocfilehash: fc32e5c4a95f0e33b5532af9c77d31bd6446e641
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460470"
---
# <a name="showexternalrecipientcount"></a>ShowExternalRecipientCount

Das **ShowExternalRecipientCount** -Element gibt an, ob Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird. 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
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
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert dieses Elements ist **true** , wenn Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird. Der Wert ist **false** , wenn Consumer des [GetMailTips-Vorgangs](getmailtips-operation.md) keine e-Mail-Tipps anzeigen müssen, die die Anzahl der externen Empfänger angeben, an die eine Nachricht adressiert wird. 
  
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



[GetMailTips-Vorgang](getmailtips-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

