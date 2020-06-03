---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: Das routingtype-Element stellt das Routingprotokoll für den Empfänger dar.
ms.openlocfilehash: 2193e72c38c687669f6e052b4d2526029aa89d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459034"
---
# <a name="routingtype-emailaddress"></a>RoutingType (EmailAddress)

Das **routingtype** -Element stellt das Routingprotokoll für den Empfänger dar. 
  
```XML
<RoutingType/>
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
|[E-Mail (e-Mail-Adresse)](email-emailaddresstype.md) <br/> |Gibt die e-Mail-Adresse des MailboxData-Objekts an. Dieses Element wird im GetUserAvailability- [Vorgang](getuseravailability-operation.md)verwendet.  <br/><br/> Es folgt der XPath für dieses Element:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Postfach (Verfügbarkeit)](mailbox-availability.md) <br/> | Stellt den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung dar.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist optional. Im Folgenden sind die möglichen Werte aufgeführt:

* SMTP
* Ex

Wenn kein Wert angegeben wird, wird der Standardwert von SMTP verwendet.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element kann höchstens einmal im [e-Mail-Element (Epost (Email Type))](email-emailaddresstype.md) vorkommen. Dieses Element ist nicht erforderlich. Dieses Element ist für die Integration zukünftiger Protokolle vorhanden. Ein anderes **Routing** Type-Element wird für den Zugriff auf Elemente im Postfach eines Benutzers verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

