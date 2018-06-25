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
description: Das Element RoutingType stellt das routing-Protokoll für den Empfänger.
ms.openlocfilehash: a0a6cf312bcb1d4b4818a82bc8d8d3e3f33ad6f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831255"
---
# <a name="routingtype-emailaddress"></a>RoutingType (EmailAddress)

Das Element **RoutingType** stellt das routing-Protokoll für den Empfänger. 
  
```XML
<RoutingType/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail (EmailAddressType)](email-emailaddresstype.md) <br/> |Gibt die e-Mail-Adresse des MailboxData-Objekts. Dieses Element wird in den [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.  <br/><br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Postfach (Verfügbarkeit)](mailbox-availability.md) <br/> | Stellt den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetUserOofSettingsRequest/Mailbox` <br/><br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist optional. Der einzige gültige Wert ist SMTP. Wenn kein Wert angegeben ist, wird der Standardwert der SMTP-verwendet.
  
## <a name="remarks"></a>Hinweise

Dieses Element kann höchstens einmal im Element [E-Mail (EmailAddressType)](email-emailaddresstype.md) auftreten. Dieses Element ist nicht erforderlich. Dieses Element ist für die Aufnahme der zukünftigen Protokolle vorhanden. Eine andere **RoutingType** -Element wird für den Zugriff auf Elemente im Postfach des Benutzers verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

