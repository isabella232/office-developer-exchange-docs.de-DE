---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: Das ExpandGroupMembership-Element gibt an, ob die Mitgliedschaft der Gruppe erweitert werden soll, die von einer GetSearchableMailboxes-Anforderung zurückgegeben wird.
ms.openlocfilehash: fb835f8f1fa9fb957c6b3bf3ddef80e68d9c049f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541399"
---
# <a name="expandgroupmembership"></a>ExpandGroupMembership

Das **ExpandGroupMembership-Element** gibt an, ob die Mitgliedschaft der Gruppe erweitert werden soll, die von einer **GetSearchableMailboxes-Anforderung** zurückgegeben wird. 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)  |  [GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **ExpandGroupElement-Element** gibt an, dass die Gruppenmitgliedschaft erweitert wird. Der Wert **"false"** gibt an, dass die Gruppenmitgliedschaft nicht erweitert wird, um die Mitglieder der Gruppe anzuzeigen. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

