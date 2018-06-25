---
title: Manifeste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 650d9fc0-1504-4db4-95d6-d3ba86df66ca
description: Das Manifeste-Element enthält eine Auflistung von base64-codierten app-Manifesten, die für die e-Mail-Konto installiert sind.
ms.openlocfilehash: 3877841c097e6b968d0af51ae5261e5b4336c7ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830362"
---
# <a name="manifests"></a>Manifeste

Das **Manifeste** -Element enthält eine Auflistung von base64-codierten app-Manifesten, die für die e-Mail-Konto installiert sind. 
  
```XML
<Manifests>
   <Manifest/>
</Manifests>
```

 **ArrayOfAppManifestsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Manifest](manifest.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetAppManifestsResponse](getappmanifestsresponse.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

