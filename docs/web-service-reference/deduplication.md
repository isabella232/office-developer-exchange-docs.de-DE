---
title: Datendeduplizierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: Das Deduplizierung-Element gibt an, ob das Suchergebnis Duplikate entfernt werden soll.
ms.openlocfilehash: 3f06bb1dccd0677b7fd43c4ad82eda54a0c3f812
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757891"
---
# <a name="deduplication"></a>Datendeduplizierung

Das **Deduplizierung** -Element gibt an, ob das Suchergebnis Duplikate entfernt werden soll. 
  
```XML
<Deduplication> true | false </Deduplication>
```

**Boolean**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das Deduplizierung-Element gibt an, dass die Suchergebnisse möglicherweise keine Duplikate enthalten. Der Wert **false** gibt an, dass Suchergebnisse doppelte Elemente enthalten können. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

