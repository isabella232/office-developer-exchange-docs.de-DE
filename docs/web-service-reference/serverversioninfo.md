---
title: ServerVersionInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: Das Element ServerVersionInfo stellt die Versionsnummer von Microsoft Exchange Server.
ms.openlocfilehash: aff8a6542e2ae6fb1148dd29051b7b33ad90eeff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831389"
---
# <a name="serverversioninfo"></a>ServerVersionInfo

Das Element **ServerVersionInfo** stellt die Versionsnummer von Microsoft Exchange Server. 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Hauptversion  <br/> |Beschreibt die Hauptversionsnummer.  <br/> |
|MinorVersion  <br/> |Beschreibt die Nummer der Nebenversion.  <br/> |
|MajorBuildNumber  <br/> |Beschreibt die wichtigsten Buildnummer an.  <br/> |
|MinorBuildNumber  <br/> |Beschreibt die Nebenversion Buildnummer an.  <br/> |
|Version  <br/> |Beschreibt die Schemaversion von Exchange-Webdienste (EWS).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wird in den SOAP-Header einer Exchange-Webdienste-Response-Nachricht zurückgegeben.
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

