---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: Das mailboxtype-Element stellt den Typ des Postfachs dar, das durch die e-Mail-Adresse dargestellt wird.
ms.openlocfilehash: 8c322ab8a87730832f5d199698a369656b058a9a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459798"
---
# <a name="mailboxtype"></a>MailboxType

Das **mailboxtype** -Element stellt den Typ des Postfachs dar, das durch die e-Mail-Adresse dargestellt wird. 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

**MailboxTypeType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöste e-Mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Gibt eine Liste von Besprechungsräumen an.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **mailboxtype** -Element aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Postfach  <br/> |Stellt ein e-Mail-aktiviertes Active Directory-Objekt dar.  <br/> |
|PublicDL  <br/> |Stellt eine öffentliche Verteilerliste dar.  <br/> |
|PrivateDL  <br/> |Stellt eine private Verteilerliste im Postfach eines Benutzers dar.  <br/> |
|Kontakt  <br/> |Stellt einen Kontakt im Postfach eines Benutzers dar.  <br/> |
|PublicFolder  <br/> |Stellt einen öffentlichen Ordner dar.  <br/> |
|Unbekannt  <br/> |Stellt einen unbekannten Typ von Postfach dar.  <br/> |
|OneOff  <br/> |Stellt ein einmaliges Mitglied einer persönlichen Verteilerliste dar.  <br/> |
|GroupMailbox  <br/> |Stellt ein Gruppenpostfach dar.  <br/> |
   
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

