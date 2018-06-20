---
title: base64FolderId (UM-Webdienst)
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
description: Das base64FolderId-Element enthält den Bezeichner des Ordners, der als e-Mail-Standardordner angeben aus der Unified Messaging Nachrichten über das Telefon in einer SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst) Anforderung liest.
ms.openlocfilehash: 7d710542418a717c6fcad243a22682e5840ebbd2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757430"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (UM-Webdienst)

Das **base64FolderId** -Element enthält den Bezeichner des Ordners, der als e-Mail-Standardordner angeben aus der Unified Messaging Nachrichten über das Telefon in einer Anforderung [SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md) liest. 
  
[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (UM-Webdienst)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Definiert die Anforderung an den Telefon Zugriff auf e-Mail-Ordner festzulegen.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt die MAPI-ID des Ordners.
  
## <a name="remarks"></a>Hinweise

Wenn den Telefon Zugriff e-Mail-Ordner festlegen möchten, verwenden Sie die [SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md).
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetTelephoneAccessFolderEmail (UM-Webdienst)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail-Vorgang (UM-Webdienst)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder Operation](findfolder-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)

