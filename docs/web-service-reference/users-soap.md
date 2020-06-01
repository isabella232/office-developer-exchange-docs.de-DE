---
title: Benutzer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Das users-Element stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.
ms.openlocfilehash: 851447a2918e365b7c5d8812a61c9d425d26ffa2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461898"
---
# <a name="users-soap"></a>Benutzer (SOAP)

Das **Users** -Element stellt eine Auflistung von e-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen. 
  
```XML
<Users>
   <User/>
</Users>
```

 **Benutzer**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benutzer (SOAP)](user-soap.md) <br/> |Stellt die e-Mail-Adresse eines Benutzers dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |Stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.  <br/> |
|[Request (SOAP)](request-soap.md) <br/> |Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

