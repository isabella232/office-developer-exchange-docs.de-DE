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
description: Das SharedFolderId-Element stellt den Bezeichner des freigegebenen Ordners dar, für den der lokale Ordner Bezeichner von einer GetSharingFolder-Vorgangsanforderung zurückgegeben werden soll.
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466122"
---
# <a name="sharedfolderid"></a>SharedFolderId

Das **SharedFolderId** -Element stellt den Bezeichner des freigegebenen Ordners dar, für den der lokale Ordner Bezeichner von einer [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung zurückgegeben werden soll. 
  
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
|[GetSharingFolder](getsharingfolder.md) <br/> |Definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die den Bezeichner des freigegebenen Ordners darstellt, für den die lokale Ordner-ID von einer [GetSharingFolder-Vorgangs](getsharingfolder-operation.md) Anforderung zurückgegeben werden soll. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingFolder-Vorgang](getsharingfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

