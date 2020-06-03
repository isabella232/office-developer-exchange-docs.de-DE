---
title: RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: Das RefreshSharingFolder-Element definiert eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners. Es ist das Basiselement für den RefreshSharingFolder-Vorgang.
ms.openlocfilehash: 4454607fa2c3114cc7279fd7c30f8aee74707baa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467928"
---
# <a name="refreshsharingfolder"></a>RefreshSharingFolder

Das **RefreshSharingFolder** -Element definiert eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners. Es ist das Basiselement für den [RefreshSharingFolder-Vorgang](refreshsharingfolder-operation.md).
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 **RefreshSharingFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SharingFolderId](sharingfolderid.md) <br/> |Stellt den Bezeichner des lokalen Ordners in einer Freigabebeziehung dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

