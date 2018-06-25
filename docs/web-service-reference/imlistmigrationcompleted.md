---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: Das Element ImListMigrationCompleted gibt an, ob der Exchange-Informationsspeicher die instant messaging-Elemente von instant messaging-Clients verwendete enthält.
ms.openlocfilehash: 25f1b583b354a71958fbc8052c492726dc0eb7db
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829893"
---
# <a name="imlistmigrationcompleted"></a>ImListMigrationCompleted

Das Element **ImListMigrationCompleted** gibt an, ob der Exchange-Informationsspeicher die Instant messaging-von instant messaging-Clients verwendete Elemente enthält. 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetImListMigrationCompleted](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das Element **ImListMigrationCompleted** gibt an, dass die instant messaging-Kontakte, die mit der Exchange Store migriert wurde gespeichert. Der Wert **false** gibt an, dass der Sofortnachricht-Kontakte Store nicht migriert wurde. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

