---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: Das MailboxType-Element stellt den Postfachtyp dar, der durch die E-Mail-Adresse dargestellt wird.
ms.openlocfilehash: f7605bf0e90851352efaaabed09e878be0925581
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524049"
---
# <a name="mailboxtype"></a>MailboxType

Das **MailboxType-Element** stellt den Postfachtyp dar, der durch die E-Mail-Adresse dargestellt wird. 
  
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
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöste E-Mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifiziert eine Liste von Besprechungsräumen.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **MailboxType-Element** aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Postfach  <br/> |Stellt ein E-Mail-aktiviertes Active Directory-Objekt dar.  <br/> |
|PublicDL  <br/> |Stellt eine öffentliche Verteilerliste dar.  <br/> |
|PrivateDL  <br/> |Stellt eine private Verteilerliste im Postfach eines Benutzers dar.  <br/> |
|Kontakt  <br/> |Stellt einen Kontakt im Postfach eines Benutzers dar.  <br/> |
|PublicFolder  <br/> |Stellt einen öffentlichen Ordner dar.  <br/> |
|Unbekannt  <br/> |Stellt einen unbekannten Postfachtyp dar.  <br/> |
|OneOff  <br/> |Stellt ein einmaliges Mitglied einer persönlichen Verteilerliste dar.  <br/> |
|GroupMailbox  <br/> |Stellt ein Gruppenpostfach dar.  <br/> |
   
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

