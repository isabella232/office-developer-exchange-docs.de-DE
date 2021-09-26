---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: Das SharedFolderId-Element stellt den Bezeichner des freigegebenen Ordners dar, dessen lokaler Ordnerbezeichner von einer GetSharingFolder-Vorgangsanforderung zurückgegeben werden soll.
ms.openlocfilehash: 7e47ba49abed99bdb3cfd00eb43d2ef276d4ef37
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545972"
---
# <a name="sharedfolderid"></a>SharedFolderId

Das **SharedFolderId-Element** stellt den Bezeichner des freigegebenen Ordners dar, dessen lokaler Ordnerbezeichner von einer [GetSharingFolder-Vorgangsanforderung](getsharingfolder-operation.md) zurückgegeben werden soll. 
  
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
|[GetSharingFolder](getsharingfolder.md) <br/> |Definiert eine Anforderung zum Abrufen des lokalen Ordnerbezeichners eines angegebenen freigegebenen Ordners.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die den Bezeichner des freigegebenen Ordners darstellt, für den der lokale Ordnerbezeichner von einer [GetSharingFolder-Vorgangsanforderung](getsharingfolder-operation.md) zurückgegeben werden soll. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingFolder-Vorgang](getsharingfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

