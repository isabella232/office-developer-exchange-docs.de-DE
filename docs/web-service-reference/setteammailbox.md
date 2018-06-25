---
title: SetTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6ee7cc-8f88-4de2-ae5c-cabf2f2193d0
description: Das SetTeamMailbox -Element enthält eine Anforderung an ein websitepostfach festlegen.
ms.openlocfilehash: 708863168f4e89775deee8c5d66427df41515089
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831455"
---
# <a name="setteammailbox"></a>SetTeamMailbox

Das **SetTeamMailbox** -Element enthält eine Anforderung an ein websitepostfach festlegen. 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 **SetTeamMailboxRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [Status (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

