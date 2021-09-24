---
title: DocumentSharingLocationCollectionSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0e3346f9-7a55-4e87-b121-9b1ee7f227f4
description: Das DocumentSharingLocationCollectionSetting-Element stellt eine Benutzereinstellung dar, bei der es sich um eine Sammlung von Speicherorten und Metadaten für die Dokumentationsfreigabe handelt.
ms.openlocfilehash: 75c420deae5dfd9b441c7f73bf3565018d3bfbd6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538366"
---
# <a name="documentsharinglocationcollectionsetting-soap"></a>DocumentSharingLocationCollectionSetting (SOAP)

Das **DocumentSharingLocationCollectionSetting-Element** stellt eine Benutzereinstellung dar, bei der es sich um eine Sammlung von Speicherorten und Metadaten für die Dokumentationsfreigabe handelt. 
  
[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md)
  
```XML
<DocumentSharingLocationCollectionSetting>
    <DocumentSharingLocations />
</DocumentSharingLocationCollectionSetting>
```

 **DocumentSharingLocationCollectionSetting**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Stellt den Speicherort und die Metadaten für eine Liste der Speicherorte für die Dokumentfreigabe dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Stellt eine Auflistung von Benutzereinstellungen dar.  <br/> |
   
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

