---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: Das UserMailbox -Element identifiziert ein Benutzerpostfach.
ms.openlocfilehash: c2a66b23de5e4b312f60019f0b4ecfb4088b3da2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542617"
---
# <a name="usermailbox"></a>UserMailbox

Das **UserMailbox** -Element identifiziert ein Benutzerpostfach. 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 **UserMailboxType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Der Textwert des **Id** -Attributs ist der Bezeichner des Postfachs an.  <br/> |
|IsArchive  <br/> |Der Textwert der **IsArchive** -Attribut gibt an, ob das Postfach ein Archivpostfach ist. Der Textwert **true** für das **IsArchive** -Attribut gibt an, dass das Postfach ein Archivpostfach ist. Der Wert **false** für das **IsArchive** -Attribut gibt an, dass das Postfach eines primären Postfachs ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Postfächer (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) | [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |true  <br/> |
   

