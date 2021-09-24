---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: Das ResultType-Element enthält den Typ der auszuführenden Suche. Der Suchtyp kann nur Statistiken oder nur die Vorschau sein.
ms.openlocfilehash: 65227a8f79a7abd597653b646a7c3985c3e38ac9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509455"
---
# <a name="resulttype"></a>ResultType

Das **ResultType-Element** enthält den Typ der auszuführenden Suche. Der Suchtyp kann nur Statistiken oder nur die Vorschau sein. 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 **SearchResultType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxesResult](searchmailboxesresult.md)  |  [SearchMailboxes](searchmailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **ResultType-Elements** ist der Ergebnistyp, der für eine Ermittlungssuche zurückgegeben wird. Ein Textwert von **StatisticsOnly** gibt die Suchstatistiken zurück. Ein Textwert von **PreviewOnly** gibt Informationen zur Elementvorschau zurück. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

