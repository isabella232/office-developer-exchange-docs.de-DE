---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: Das PublicFolderInformation-Element enthält Informationen, die Clients zum Senden einer Anforderung der AutoErmittlung zum Ermitteln von Informationen für den Benutzer für Öffentliche Ordner verwenden können.
ms.openlocfilehash: bb4432a664024c3d1ccb17826948cfe7a1b58cdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830927"
---
# <a name="publicfolderinformation-pox"></a>PublicFolderInformation (POX)

Das **PublicFolderInformation** -Element enthält Informationen, die Clients zum Senden einer Anforderung der AutoErmittlung zum Ermitteln von Informationen für den Benutzer für Öffentliche Ordner verwenden können. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SmtpAddress (POX)](smtpaddress-pox.md) <br/> |Enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen. Diese SMTP-Adresse kann zum Ermitteln der Öffentliche Ordner-Einstellungen im Element ["EmailAddress" (POX)](emailaddress-pox.md) einer Anforderung für die AutoErmittlung verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Gibt die kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **PublicFolderInformation** -Element ist ein optionales untergeordnetes Element des Elements **Konto** . 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

