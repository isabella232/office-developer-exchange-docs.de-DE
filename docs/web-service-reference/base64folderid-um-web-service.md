---
title: base64FolderId (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: Das base64FolderId-Element enthält den Bezeichner des Ordners, der als Standard-E-Mail-Ordner angegeben werden soll, aus dem Unified Messaging Nachrichten über das Telefon in einer Um-Webdienstanforderung (SetTelephoneAccessFolderEmail) liest.
ms.openlocfilehash: 149ad55d0ab09f57b0dc3ace7eb0e17c96265e3f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518932"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (UM-Webdienst)

Das **base64FolderId-Element** enthält den Bezeichner des Ordners, der als Standard-E-Mail-Ordner angegeben werden soll, aus dem Unified Messaging Nachrichten über das Telefon in einer [Um-Webdienstanforderung (SetTelephoneAccessFolderEmail)](settelephoneaccessfolderemail-operation-um-web-service.md) liest. 
  
[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (UM-Webdienst)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Definiert die Anforderung zum Festlegen des E-Mail-Ordners für den Telefonzugriff.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt die MAPI-ID des Ordners dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Festlegen des E-Mail-Ordners für den Telefonzugriff den [SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst).](settelephoneaccessfolderemail-operation-um-web-service.md)
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder-Vorgang](findfolder-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)

