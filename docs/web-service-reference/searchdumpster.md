---
title: SearchDumpster
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: Das SearchDumpster-Element gibt an, ob im Exchange Dumpster gesucht werden soll.
ms.openlocfilehash: 4d8f05393691e38e3a4154e955d03c8591064a1a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521690"
---
# <a name="searchdumpster"></a>SearchDumpster

Das **SearchDumpster-Element** gibt an, ob im Exchange Dumpster gesucht werden soll. 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **SearchDumpster-Element** gibt an, dass die Postfachstatistiksuche den Exchange Dumpster enthält. Der Wert **"false"** gibt an, dass der Exchange Dumpster nicht durchsucht wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

