---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: Das InPlaceHoldIdentity-Element gibt die Identität des Haltestatus, der die Postfachelemente beibehält.
ms.openlocfilehash: 954e6ad6c3e0b7786d6bbb8230dba913a32359bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829938"
---
# <a name="inplaceholdidentity"></a>InPlaceHoldIdentity

Das **InPlaceHoldIdentity** -Element gibt die Identität des Haltestatus, der die Postfachelemente beibehält. 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **InPlaceHoldIdentity** -Elements ist der Postfach-Archiv-Bezeichner. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

