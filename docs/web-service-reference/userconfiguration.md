---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: Das UserConfiguration-Element definiert ein einzelnes Benutzer Konfigurationsobjekt.
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468908"
---
# <a name="userconfiguration"></a>UserConfiguration

Das **UserConfiguration** -Element definiert ein einzelnes Benutzer Konfigurationsobjekt. 
  
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
|[UserConfigurationName](userconfigurationname.md) <br/> |Stellt den Namen eines Benutzer Konfigurationsobjekts dar. Dieses Element muss verwendet werden, wenn Sie ein Benutzer Konfigurationsobjekt erstellen.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert die Element-ID des Benutzer Konfigurationsobjekts.  <br/> |
|[Wörterbuch](dictionary.md) <br/> |Definiert eine Gruppe von Wörterbuch-Eigenschafts Einträgen für ein Benutzer Konfigurationsobjekt.  <br/> |
|[XMLDATA](xmldata.md) <br/> |Enthält XML-Daten Eigenschafts Inhalt für ein Benutzer Konfigurationsobjekt.  <br/> |
|[BinaryData](binarydata.md) <br/> |Enthält binäre Daten Eigenschafts Inhalte für ein Benutzer Konfigurationsobjekt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Stellt eine Anforderung zum Erstellen eines Benutzer Konfigurationsobjekts dar.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Stellt eine Antwort dar, die ein Benutzer Konfigurationsobjekt zurückgibt.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Stellt eine Anforderung zum Aktualisieren eines Benutzer Konfigurationsobjekts dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

