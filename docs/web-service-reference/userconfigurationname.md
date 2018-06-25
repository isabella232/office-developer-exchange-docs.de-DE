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
description: Das Element UserConfigurationName stellt den Namen eines Benutzers Configuration-Objekts. Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: 40580343e92493c3d39b090371708269ec3274b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839436"
---
# <a name="userconfigurationname"></a>UserConfigurationName

Das Element **UserConfigurationName** stellt den Namen eines Benutzers Configuration-Objekts. Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt. 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

 **UserConfigurationNameType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Enthält einen String-Wert, der den Namen eines Benutzers Configuration-Objekts darstellt. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Stellt den Ordner Bezeichner des Ordners, der das Benutzerobjekt Konfiguration enthält.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Stellt einen definierten Ordnernamen des Ordners, der das Benutzerobjekt Konfiguration enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |Stellt eine Anforderung zum Löschen einer Benutzer-Konfigurationsobjekt.  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |Eine Anforderung zum Abrufen eines Benutzers Konfiguration-Objekts darstellt.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Definiert einen einzelnen Benutzer-Konfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

