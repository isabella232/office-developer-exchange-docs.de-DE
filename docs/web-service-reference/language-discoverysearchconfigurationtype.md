---
title: Language (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Das Language (DiscoverySearchConfigurationType)-Element identifiziert die Kultur, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll. Außerdem wird die sprache angegeben, die in einer Suchabfrage verwendet wird.
ms.openlocfilehash: 5d51960aa00b2c47d96972abc05e4d6027eeecb3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540895"
---
# <a name="language-discoverysearchconfigurationtype"></a>Language (DiscoverySearchConfigurationType)

Das **Language (DiscoverySearchConfigurationType)-Element** identifiziert die Kultur, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll. Außerdem wird die sprache angegeben, die in einer Suchabfrage verwendet wird. 
  
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

Der Textwert des **Language -Elements (DiscoverySearchConfigurationType)** ist eine Kultur oder Sprache. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element gibt das Format von Datumsbereichen an, die im [SearchMailboxes-Vorgang](searchmailboxes-operation.md) oder im [SetHoldOnMailboxes-Vorgang](setholdonmailboxes-operation.md)angegeben sind.
  
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

