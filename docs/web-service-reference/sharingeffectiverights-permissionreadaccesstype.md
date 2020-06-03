---
title: SharingEffectiveRights (PermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: Das SharingEffectiveRights-Element gibt die Berechtigungen an, die der Benutzer für die Kontaktdaten verwendet, die freigegeben werden.
ms.openlocfilehash: 64b1e6d831068e9699e9cd47693e74919e0416a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526662"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a>SharingEffectiveRights (PermissionReadAccessType)

Das **SharingEffectiveRights** -Element gibt die Berechtigungen an, die der Benutzer für die Kontaktdaten verwendet, die freigegeben werden. 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 **PermissionReadAccessType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner dar, der in einem Postfach enthalten ist.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **SharingEffectiveRights** -Element aufgeführt. 
  
**SharingEffectiveRights-Element Text Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen im Ordner verfügt.  <br/> |
|FullDetails  <br/> |Gibt an, dass der Benutzer über die Berechtigung zum Lesen aller Elemente im Ordner verfügt.  <br/> |
   
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

