---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: Das UserConfigurationName-Element stellt den Namen eines Benutzer Konfigurationsobjekts dar. Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.
ms.openlocfilehash: 020b55919f7f81602a5eb072652d82168607d306
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466031"
---
# <a name="userconfigurationname"></a>UserConfigurationName

Das **UserConfigurationName** -Element stellt den Namen eines Benutzer Konfigurationsobjekts dar. Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt. 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

**UserConfigurationNameType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Enthält einen String-Wert, der den Namen eines Benutzer Konfigurationsobjekts darstellt. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Stellt den Ordner Bezeichner des Ordners dar, der das Benutzer Konfigurationsobjekt enthält.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Stellt einen Distinguished Folder-Namen des Ordners dar, der das Benutzer Konfigurationsobjekt enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |Stellt eine Anforderung zum Löschen eines Benutzer Konfigurationsobjekts dar.  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Stellt eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts dar.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Definiert ein einzelnes Benutzer Konfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

