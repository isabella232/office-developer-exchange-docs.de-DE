---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: Das UserConfiguration-Element definiert ein einzelnes Benutzerkonfigurationsobjekt.
ms.openlocfilehash: 3821cabf777143de4a68d20a90cb78acedcff552
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538555"
---
# <a name="userconfiguration"></a>UserConfiguration

Das **UserConfiguration-Element** definiert ein einzelnes Benutzerkonfigurationsobjekt. 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 **UserConfigurationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |Stellt den Namen eines Benutzerkonfigurationsobjekts dar. Dieses Element muss verwendet werden, wenn Sie ein Benutzerkonfigurationsobjekt erstellen.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert den Bezeichner des Benutzerkonfigurationsobjektelements.  <br/> |
|[Wörterbuch](dictionary.md) <br/> |Definiert eine Reihe von Wörterbucheigenschaftseinträgen für ein Benutzerkonfigurationsobjekt.  <br/> |
|[XmlData](xmldata.md) <br/> |Enthält XML-Dateneigenschaftsinhalte für ein Benutzerkonfigurationsobjekt.  <br/> |
|[BinaryData](binarydata.md) <br/> |Enthält binäre Dateneigenschafteninhalte für ein Benutzerkonfigurationsobjekt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Stellt eine Anforderung zum Erstellen eines Benutzerkonfigurationsobjekts dar.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Stellt eine Antwort dar, die ein Benutzerkonfigurationsobjekt zurückgibt.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Stellt eine Anforderung zum Aktualisieren eines Benutzerkonfigurationsobjekts dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

