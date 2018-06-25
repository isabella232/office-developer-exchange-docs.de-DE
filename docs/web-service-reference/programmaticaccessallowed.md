---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: Das ProgrammaticAccessAllowed-Element gibt an, ob für die Verwaltung von Informationsrechten verwaltete Daten programmgesteuerter Zugriff aktiviert ist.
ms.openlocfilehash: 50bcce745bd94bf9c2e5ced93825722307e0a096
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830889"
---
# <a name="programmaticaccessallowed"></a>ProgrammaticAccessAllowed

Das **ProgrammaticAccessAllowed** -Element gibt an, ob für die Verwaltung von Informationsrechten verwaltete Daten programmgesteuerter Zugriff aktiviert ist. 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[RightsManagementLicenseData](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **ProgrammaticAccessAllowed** -Element gibt an, dass die Daten programmgesteuert zugegriffen werden kann. Der Wert **false** gibt an, dass die Daten nicht programmgesteuert zugegriffen werden kann. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

