---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: Das ServerVersionInfo-Element enthält die Version des Servers, der die Anforderung verarbeitet hat.
ms.openlocfilehash: ac52b3eda429e65cb1ec046167a63fe4029d423a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521454"
---
# <a name="serverversioninfo-soap"></a>ServerVersionInfo (SOAP)

Das **ServerVersionInfo-Element** enthält die Version des Servers, der die Anforderung verarbeitet hat. 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 **ServerVersionInfo**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MajorVersion (SOAP)](majorversion-soap.md) <br/> |Die Hauptversionsnummer für den Server.  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |Die Nebenversionsnummer für den Server.  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |Die Hauptbuildnummer für den Server.  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |Die Kleinere Buildnummer für den Server.  <br/> |
|[Version (SOAP)](version-soap.md) <br/> |Eine Beschreibung der Serverproduktversion.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wird im SOAP-Header zurückgegeben.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

