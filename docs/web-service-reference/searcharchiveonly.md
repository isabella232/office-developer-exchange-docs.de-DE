---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: Das SearchArchiveOnly-Element gibt an, ob nur das Archivpostfach nach nicht indizierbaren Elementen durchsucht wird.
ms.openlocfilehash: a4766e101394bb83a0dcebdfe5b92f576f4a4160
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521679"
---
# <a name="searcharchiveonly"></a>SearchArchiveOnly

Das **SearchArchiveOnly-Element** gibt an, ob nur das Archivpostfach nach nicht indizierbaren Elementen durchsucht wird. 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetNonIndexableItemStatisticsế](getnonindexableitemstatistics.md) [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **SearchArchiveOnly-Element** gibt an, dass die Suche nach nicht indizierbaren Elementen nur für das Archivpostfach ausgeführt wird. Der Textwert **"false"** gibt an, dass die Suche für das primäre Postfach und das Archivpostfach ausgeführt wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

