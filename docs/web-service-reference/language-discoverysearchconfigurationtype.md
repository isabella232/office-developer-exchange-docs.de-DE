---
title: Sprache (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Das Language (DiscoverySearchConfigurationType)-Element gibt die Kultur an, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll. Außerdem wird die in einer Suchabfrage verwendete Sprache angegeben.
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463286"
---
# <a name="language-discoverysearchconfigurationtype"></a>Sprache (DiscoverySearchConfigurationType)

Das **Language (DiscoverySearchConfigurationType)** -Element gibt die Kultur an, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll. Außerdem wird die in einer Suchabfrage verwendete Sprache angegeben. 
  
```XML
<Language />
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Language (DiscoverySearchConfigurationType)-** Elements ist eine Kultur oder Sprache. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element gibt das Format von Datumsbereichen an, die im [SearchMailboxes-Vorgang](searchmailboxes-operation.md) oder im SetHoldOnMailboxes- [Vorgang](setholdonmailboxes-operation.md)angegeben sind.
  
Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

