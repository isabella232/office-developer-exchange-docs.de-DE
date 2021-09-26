---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: Das SmtpAddress-Element enthält die SMTP-Adresse, die dem für den Benutzer konfigurierten Nachrichtenspeicher für öffentliche Ordner zugewiesen ist.
ms.openlocfilehash: d257b193a3254afceaa72d396a8c2724bb3165c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546987"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

Das **SmtpAddress-Element** enthält die SMTP-Adresse, die dem für den Benutzer konfigurierten Nachrichtenspeicher für öffentliche Ordner zugewiesen ist. 
  
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
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Enthält Informationen, mit denen Clients eine AutoErmittlungsanforderung senden können, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die SMTP-Adresse dar, die dem für den Benutzer konfigurierten Öffentlichen Ordnerspeicher zugewiesen ist. Diese SMTP-Adresse kann im [EMailAddress (POX)-Element](emailaddress-pox.md) einer AutoErmittlungsanforderung verwendet werden, um Einstellungen für öffentliche Ordner zu ermitteln. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **SmtpAddress-Element** ist ein erforderliches untergeordnetes Element des **PublicFolderInformation-Elements.** 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

