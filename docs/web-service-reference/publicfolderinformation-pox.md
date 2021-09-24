---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: Das PublicFolderInformation-Element enthält Informationen, mit denen Clients eine AutoErmittlungsanforderung senden können, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln.
ms.openlocfilehash: d77ea350f05c5d6137d3b67cfd49119bf9590e53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540622"
---
# <a name="publicfolderinformation-pox"></a>PublicFolderInformation (POX)

Das **PublicFolderInformation-Element** enthält Informationen, mit denen Clients eine AutoErmittlungsanforderung senden können, um Informationen zu öffentlichen Ordnern für den Benutzer zu ermitteln. 
  
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
|[SmtpAddress (POX)](smtpaddress-pox.md) <br/> |Enthält die SMTP-Adresse, die dem nachrichtenspeicher für öffentliche Ordner zugewiesen ist, der für den Benutzer konfiguriert ist. Diese SMTP-Adresse kann im [EMailAddress (POX)-Element](emailaddress-pox.md) einer AutoErmittlungsanforderung verwendet werden, um Einstellungen für öffentliche Ordner zu ermitteln.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **PublicFolderInformation-Element** ist ein optionales untergeordnetes Element des **Account-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

