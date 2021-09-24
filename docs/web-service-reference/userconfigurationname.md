---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: Das UserConfigurationName-Element stellt den Namen eines Benutzerkonfigurationsobjekts dar. Der Name des Benutzerkonfigurationsobjekts ist der Bezeichner für ein Benutzerkonfigurationsobjekt.
ms.openlocfilehash: 7563435f25a5307aa908a64baceffb3c81138149
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517385"
---
# <a name="userconfigurationname"></a>UserConfigurationName

Das **UserConfigurationName-Element** stellt den Namen eines Benutzerkonfigurationsobjekts dar. Der Name des Benutzerkonfigurationsobjekts ist der Bezeichner für ein Benutzerkonfigurationsobjekt. 
  
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
|**Name** <br/> |Enthält einen Zeichenfolgenwert, der den Namen eines Benutzerkonfigurationsobjekts darstellt. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Stellt den Ordnerbezeichner des Ordners dar, der das Benutzerkonfigurationsobjekt enthält.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Stellt einen definierten Ordnernamen des Ordners dar, der das Benutzerkonfigurationsobjekt enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |Stellt eine Anforderung zum Löschen eines Benutzerkonfigurationsobjekts dar.  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Stellt eine Anforderung zum Abrufen eines Benutzerkonfigurationsobjekts dar.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Definiert ein einzelnes Benutzerkonfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

