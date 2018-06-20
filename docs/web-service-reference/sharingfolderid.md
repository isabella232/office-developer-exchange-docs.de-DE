---
title: SharingFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: Das SharingFolderId-Element stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung.
ms.openlocfilehash: e0eb1fbd7155040508daf253f5eb4b1352d7426d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831485"
---
# <a name="sharingfolderid"></a>SharingFolderId

Das **SharingFolderId** -Element stellt den Bezeichner des lokalen Ordners in einer Dateifreigabe Beziehung. 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem Id-Attribut angegeben ist. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RefreshSharingFolder](refreshsharingfolder.md) <br/> |Definiert eine Anforderung an den angegebenen lokalen Ordner zu aktualisieren.  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |Definiert eine Antwort auf eine [GetSharingFolder Vorgang](getsharingfolder-operation.md) an.  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [GetSharingFolder Vorgang](getsharingfolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

