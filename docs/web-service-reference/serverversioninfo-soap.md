---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: Das ServerVersionInfo-Element enthält die Version des Servers, der die Anforderung verarbeitet.
ms.openlocfilehash: b02071e4997aba91fb538d52df2612fe6fd32800
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831385"
---
# <a name="serverversioninfo-soap"></a>ServerVersionInfo (SOAP)

Das **ServerVersionInfo** -Element enthält die Version des Servers, der die Anforderung verarbeitet. 
  
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
|[Hauptversion (SOAP)](majorversion-soap.md) <br/> |Die Nummer der Hauptversion für den Server.  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |Die Nummer der Nebenversion für den Server.  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |Die wichtigsten Buildnummer für den Server.  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |Die minor Buildnummer für den Server.  <br/> |
|[Version (SOAP)](version-soap.md) <br/> |Eine Beschreibung der Version des Produkts.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wird in den SOAP-Header zurückgegeben.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

