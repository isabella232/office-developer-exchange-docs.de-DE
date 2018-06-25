---
title: Manifest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af0d7435-fef6-4f0d-bd22-00e3fa576315
description: Das Manifest Element enthält die base64-codierten app-Manifestdatei.
ms.openlocfilehash: 7388e40a96a082666519d1c67af5b218b2b9ab01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830343"
---
# <a name="manifest"></a>Manifest

Das **Manifest** -Element enthält die base64-codierten app-Manifestdatei. 
  
```XML
<Manifest></Manifest>
```

 **base64Binary**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Manifeste](manifests.md) | [InstallApp](installapp.md) | [ClientExtension](clientextension.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der Manifest-Element ist ein ASCII-Darstellung der binary base64-codierte Format der Client-app-Manifestdatei.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

