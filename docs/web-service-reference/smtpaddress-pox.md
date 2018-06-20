---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: Das SmtpAddress-Element enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen.
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831507"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

Das **SmtpAddress** -Element enthält die SMTP-Adresse für den Benutzer konfigurierten Nachricht Informationsspeicher für Öffentliche Ordner zugewiesen. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Konto (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Enthält Informationen, mit denen Clients eine Anforderung der AutoErmittlung zum Ermitteln von Öffentliche Ordner-Informationen für den Benutzer zu senden.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die SMTP-Adresse für den Benutzer konfigurierten Informationsspeicher für Öffentliche Ordner zugewiesen. Diese SMTP-Adresse kann zum Ermitteln der Öffentliche Ordner-Einstellungen im Element ["EmailAddress" (POX)](emailaddress-pox.md) einer Anforderung für die AutoErmittlung verwendet werden. 
  
## <a name="remarks"></a>Hinweise

Das **SmtpAddress** -Element ist ein erforderliches untergeordnetes Element des **PublicFolderInformation** -Elements. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

