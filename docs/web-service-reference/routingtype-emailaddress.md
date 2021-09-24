---
title: RoutingType (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 74d83198-0d9d-4c78-a2bc-9a671859ff37
description: Das RoutingType-Element stellt das Routingprotokoll für den Empfänger dar.
ms.openlocfilehash: cc4d18ff9fa18f0ec2024f15cb6a3bd4199832de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534429"
---
# <a name="routingtype-emailaddress"></a>RoutingType (EmailAddress)

Das **RoutingType-Element** stellt das Routingprotokoll für den Empfänger dar. 
  
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
|[E-Mail (EmailAddressType)](email-emailaddresstype.md) <br/> |Gibt die E-Mail-Adresse des MailboxData-Objekts an. Dieses Element wird im [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.  <br/><br/> Es folgt der XPath für dieses Element:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Postfach (Verfügbarkeit)](mailbox-availability.md) <br/> | Stellt den Postfachbenutzer für eine SetUserOofSettings- oder GetUserOofSettings-Anforderung dar.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist optional. Im Folgenden sind die möglichen Werte aufgeführt:

* SMTP
* EX

Wenn kein Wert angegeben wird, wird der Standardwert von SMTP verwendet.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element kann höchstens einmal im [Email -Element (EmailAddressType)](email-emailaddresstype.md) auftreten. Dieses Element ist nicht erforderlich. Dieses Element ist für die Einbindung zukünftiger Protokolle vorhanden. Ein weiteres **RoutingType-Element** wird für den Zugriff auf Elemente im Postfach eines Benutzers verwendet. 
  
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
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

