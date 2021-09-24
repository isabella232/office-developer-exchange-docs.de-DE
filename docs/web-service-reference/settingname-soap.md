---
title: SettingName (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: Das SettingName-Element stellt den Namen einer Einstellung in der Antwort dar.
ms.openlocfilehash: 1a676f55ad86496ae8bdbdfbeaeb9827b1aa6646
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531881"
---
# <a name="settingname-soap"></a>SettingName (SOAP)

Das **SettingName-Element** stellt den Namen einer Einstellung in der Antwort dar. 
  
```XML
<SettingName/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Stellt einen Fehler dar, der beim Abrufen einer Benutzereinstellung zurückgegeben wird.  <br/> |
|[DomainSettingError (SOAP)](domainsettingerror-soap.md) <br/> |Stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer **GetDomainSettings-Anforderung** dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert des **SettingName-Elements** stellt den Namen einer Einstellung in einer Antwort dar. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

