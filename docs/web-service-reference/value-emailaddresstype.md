---
title: Wert (e-mailemailtype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: Das Value-Element gibt den Wert einer e-mailemail an, die einem attributes-Array zugeordnet ist.
ms.openlocfilehash: 45af2aaab7d2475ae46ae24ed13b1435f5b352c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467599"
---
# <a name="value-emailaddresstype"></a>Wert (e-mailemailtype)

Das **value** -Element gibt den Wert einer e- **mailemail** an, die einem attributes-Array zugeordnet ist. 
  
```XML
<Value>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
   <OriginalDisplayName/>
</Value>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Name (Zeichenfolge)](name-string.md)  |  [E-mailemail (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)  |  [Mailboxtype](mailboxtype.md)  |  [ItemID](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[EmailAddressAttributedValue](emailaddressattributedvalue.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   

