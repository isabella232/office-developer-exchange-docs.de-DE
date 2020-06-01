---
title: SetHoldOnMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 909194d6-e2b1-4774-bf29-04ed4318df1d
description: Das SetHoldOnMailboxesResponse-Element stellt eine Antwort auf eine SetHoldOnMailboxes-Anforderung dar.
ms.openlocfilehash: 37ad5c6e8f880831a98ff2e649a92cee99930889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44438082"
---
# <a name="setholdonmailboxesresponse"></a>SetHoldOnMailboxesResponse

Das **SetHoldOnMailboxesResponse** -Element stellt eine Antwort auf eine **SetHoldOnMailboxes** -Anforderung dar. 
  
```XML
<SetHoldOnMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponse>
```

 **SetHoldOnMailboxesResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [MailboxHoldResult](mailboxholdresult.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

