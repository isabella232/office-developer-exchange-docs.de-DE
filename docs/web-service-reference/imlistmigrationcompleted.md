---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: Das ImListMigrationCompleted-Element gibt an, ob der Exchange Speicher die von Chatclients verwendeten Chatelemente enthält.
ms.openlocfilehash: b55f3d72259897d7bdf46b351421b0148a41b93e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514613"
---
# <a name="imlistmigrationcompleted"></a>ImListMigrationCompleted

Das **ImListMigrationCompleted-Element** gibt an, ob der Exchange Speicher die von Chatclients verwendeten Chatelemente enthält. 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetImListMigrationCompleted](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **ImListMigrationCompleted-Element** gibt an, dass der Chatkontaktspeicher in den Exchange Speicher migriert wurde. Der Wert **"false"** gibt an, dass der Chatnachrichtenkontaktspeicher nicht migriert wurde. 
  
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
   

