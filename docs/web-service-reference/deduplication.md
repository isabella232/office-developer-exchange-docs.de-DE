---
title: Deduplizierung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: Das Deduplizierungselement gibt an, ob das Suchergebnis doppelte Elemente entfernen soll.
ms.openlocfilehash: 6178502d102b8c24b39d7276352c31740c62352c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543408"
---
# <a name="deduplication"></a>Deduplizierung

Das **Deduplizierungselement** gibt an, ob das Suchergebnis doppelte Elemente entfernen soll. 
  
```XML
<Deduplication> true | false </Deduplication>
```

**Boolescher Wert**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxes](searchmailboxes.md)  |  [SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das Deduplizierungselement weist darauf hin, dass Suchergebnisse keine doppelten Elemente enthalten dürfen. Der Wert **"false"** gibt an, dass Suchergebnisse doppelte Elemente enthalten können. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

