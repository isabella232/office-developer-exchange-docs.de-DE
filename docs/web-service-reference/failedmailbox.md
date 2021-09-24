---
title: FailedMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3d4c9816-54bb-4932-b4ba-f057c9173a1a
description: Das FailedMailbox -Element gibt die Fehlermeldung für ein Postfach, die nicht auf Suchen.
ms.openlocfilehash: 5e2bfbce5da35ecacd1757a9c612ed226af963ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535258"
---
# <a name="failedmailbox"></a>FailedMailbox

Das **FailedMailbox** -Element gibt die Fehlermeldung für ein Postfach, die nicht auf Suchen. 
  
```XML
<FailedMailbox>
    <Mailbox/>
    <ErrorCode/>
    <ErrorMessage/>
    <IsArchive/>
</FailedMailbox>
```

 **FailedSearchMailboxType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach (Zeichenfolge)](mailbox-string.md) <br/> |Enthält einen Bezeichner für das Postfach.  <br/> |
|[ErrorCode (Int)](errorcode-int.md) <br/> |Gibt den Fehlercode des Postfachs an, die die Suche ist fehlgeschlagen.  <br/> |
|[ErrorMessage](errormessage.md) <br/> |Stellt den Grund für die Überprüfungsfehler.  <br/> |
|[IsArchive](isarchive.md) <br/> |Gibt einen Boolean-Wert, der angibt, ob das Postfach ein Archiv ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FailedMailboxes](failedmailboxes.md) <br/> |Gibt ein Array von Postfächer mit Fehlern.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

