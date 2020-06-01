---
title: base64FolderId (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: Das base64FolderId-Element enthält den Bezeichner des Ordners, der als Standard-e-Mail-Ordner angegeben wird, aus dem Unified Messaging Nachrichten über das Telefon in einer Anforderung für den SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst) liest.
ms.openlocfilehash: ea31c7a0f93188e563bf95c4a3e6e91f0866746c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458047"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (um-Webdienst)

Das **base64FolderId** -Element enthält den Bezeichner des Ordners, der als Standard-e-Mail-Ordner angegeben wird, aus dem Unified Messaging Nachrichten über das Telefon in einer Anforderung für den [SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md) liest. 
  
[SetTelephoneAccessFolderEmail (um-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (um-Webdienst)](base64folderid-um-web-service.md)
  
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
|[SetTelephoneAccessFolderEmail (um-Webdienst)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Definiert die Anforderung zum Festlegen des e-Mail-Ordners für den Telefon Zugriff.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert Text stellt die MAPI-ID des Ordners dar.
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie den [SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md), um den e-Mail-Ordner für den Telefon Zugriff festzulegen.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetTelephoneAccessFolderEmail (um-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail-Vorgang (um-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder Operation](findfolder-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)

