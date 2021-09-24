---
title: Benutzer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4e051617-4eea-47d0-871a-ea1f17a0f711
description: Das Users-Element stellt eine Sammlung von E-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen.
ms.openlocfilehash: eabf0d2cd38396e907ca467596c2e55d1eb78e02
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538520"
---
# <a name="users-soap"></a>Benutzer (SOAP)

Das  Users-Element stellt eine Sammlung von E-Mail-Adressen der Benutzer dar, für die Einstellungen abgerufen werden sollen. 
  
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
|[Benutzer (SOAP)](user-soap.md) <br/> |Stellt die E-Mail-Adresse eines Benutzers dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |Stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.  <br/> |
|[Anforderung (SOAP)](request-soap.md) <br/> |Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

