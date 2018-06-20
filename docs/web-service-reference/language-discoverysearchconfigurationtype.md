---
title: Sprache (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Das Sprachelement (DiscoverySearchConfigurationType) gibt die Kultur für das kulturspezifische Format der Datumsbereiche verwendet werden. Es gibt auch die Sprache, die in einer Suchabfrage verwendet.
ms.openlocfilehash: 1e904ac4d7f525b2d12cfe83f0da33b9ed474066
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830197"
---
# <a name="language-discoverysearchconfigurationtype"></a>Sprache (DiscoverySearchConfigurationType)

Das Sprachelement **(DiscoverySearchConfigurationType)** gibt die Kultur für das kulturspezifische Format der Datumsbereiche verwendet werden. Es gibt auch die Sprache, die in einer Suchabfrage verwendet. 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der Sprachelement **(DiscoverySearchConfigurationType)** ist ein Kultur oder Sprache. 
  
## <a name="remarks"></a>Hinweise

Dieses Element gibt das Format der Datumsbereiche in den [SearchMailboxes Vorgang](searchmailboxes-operation.md) oder die [SetHoldOnMailboxes Operation](setholdonmailboxes-operation.md)angegeben.
  
Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

