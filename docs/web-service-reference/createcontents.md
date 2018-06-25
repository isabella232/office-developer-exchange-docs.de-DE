---
title: CreateContents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateContents
api_type:
- schema
ms.assetid: 8a9cd241-0d73-4be8-a563-a945898d1a0e
description: Das CreateContents-Element gibt an, ob ein Client eine Inhaltstabelle erstellen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: f84ffdd2e6b485436d9e4ccd5f03a6e2c57fcfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757747"
---
# <a name="createcontents"></a>CreateContents

Das **CreateContents** -Element gibt an, ob ein Client eine Inhaltstabelle erstellen kann. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<CreateContents>true or false</CreateContents>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EffectiveRights](effectiverights.md) <br/> |Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element wurde eingeführten InExchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass ein Client eine Inhaltstabelle erstellen kann. 
  
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nur auf Folder-Objekten verwendet.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Setting Folder-Level Permissions](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

