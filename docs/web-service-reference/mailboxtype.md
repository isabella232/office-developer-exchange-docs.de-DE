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
description: Das Element MailboxType stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.
ms.openlocfilehash: d7232377951e8d9c8f191ac856058bc28467cadd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830305"
---
# <a name="mailboxtype"></a>MailboxType

Das Element **MailboxType** stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird. 
  
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
|[Postfach](mailbox.md) <br/> |Identifiziert eine vollständig aufgelöster E-mail-Adresse.  <br/> |
|[RoomList](roomlist.md) <br/> |Eine Liste der Besprechungsräumen identifiziert.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **MailboxType** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Postfach  <br/> |Ein e-Mail-aktivierte Active Directory-Objekt darstellt.  <br/> |
|PublicDL  <br/> |Stellt eine öffentliche Verteilerliste dar.  <br/> |
|PrivateDL  <br/> |Stellt eine private Verteilerliste im Postfach eines Benutzers dar.  <br/> |
|Kontakt  <br/> |Stellt einen Kontakt im Postfach eines Benutzers dar.  <br/> |
|Öffentliche Ordner  <br/> |Stellt einen öffentlichen Ordner dar.  <br/> |
|Unbekannt  <br/> |Stellt einen unbekannten Typ des Postfachs an.  <br/> |
|OneOff  <br/> |Stellt einen einmaligen Member einer persönlichen Verteilerliste dar.  <br/> |
|GroupMailbox  <br/> |Stellt eine Gruppenpostfach an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

