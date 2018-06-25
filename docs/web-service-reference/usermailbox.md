---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: Das UserMailbox -Element identifiziert ein Benutzerpostfach.
ms.openlocfilehash: 9f359a2b0ba315c236d4bf189c3de321417bd390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839449"
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
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |true  <br/> |
   

