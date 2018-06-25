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
description: Das SharingEffectiveRights-Element gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird.
ms.openlocfilehash: 19e67827dd2dbff6fb70423980d670da5cc257a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831486"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a>SharingEffectiveRights (PermissionReadAccessType)

Das **SharingEffectiveRights** -Element gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird. 
  
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
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner, der in einem Postfach enthalten ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **SharingEffectiveRights** -Element. 
  
**Text-Elementwerte SharingEffectiveRights**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass der Benutzer nicht über die Berechtigung zum Lesen von Elementen in den Ordner verfügt.  <br/> |
|FullDetails  <br/> |Gibt an, dass der Benutzer die Berechtigung zum Lesen aller Elemente im Ordner verfügt.  <br/> |
   
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

