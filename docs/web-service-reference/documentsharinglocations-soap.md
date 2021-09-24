---
title: DocumentSharingLocations (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 394f6015-721b-4800-9286-039d430f09b3
description: Das DocumentSharingLocations-Element enthält eine Liste der Speicherort- und Metadateninformationen für einen Dokumentfreigabespeicherort.
ms.openlocfilehash: 179ad59e51b0519fa95b4031f5c9df52a44dba1a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538338"
---
# <a name="documentsharinglocations-soap"></a>DocumentSharingLocations (SOAP)

Das **DocumentSharingLocations-Element** enthält eine Liste der Speicherort- und Metadateninformationen für einen Dokumentfreigabespeicherort. 
  
```XML
<DocumentSharingLocations>
   <DocumentSharingLocation />
</DocumentSharingLocations>
```

 **DocumentSharingLocations**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Enthält den Speicherort und die Metadaten für einen Speicherort für die Dokumentfreigabe.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md) <br/> |Stellt eine Benutzereinstellung dar, bei der es sich um eine Sammlung von Speicherorten und Metadaten für die Dokumentfreigabe handelt.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

