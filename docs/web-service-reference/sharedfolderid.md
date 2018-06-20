---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: Das Element SharedFolderId stellt den Bezeichner des freigegebenen Ordner mit der ID der lokalen Ordner, für die durch die Anforderung einer GetSharingFolder-Operation zurückgegeben werden sollen.
ms.openlocfilehash: 6d4e541ef3cae89e413efa8cc5f1beaf651dc4dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831477"
---
# <a name="sharedfolderid"></a>SharedFolderId

Das Element **SharedFolderId** stellt den Bezeichner des freigegebenen Ordner mit der ID der lokalen Ordner, für die eine Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) zurückgegeben werden sollen. 
  
```xml
<SharedFolderId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die den Bezeichner des freigegebenen Ordners darstellt, der lokalen Ordner Bezeichner für die durch eine Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) zurückgegeben werden sollen. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingFolder-Vorgang](getsharingfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

