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
description: Das UserConfiguration-Element definiert einen einzelnen Benutzer-Konfigurationsobjekt.
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839437"
---
# <a name="userconfiguration"></a>UserConfiguration

Das **UserConfiguration** -Element definiert einen einzelnen Benutzer-Konfigurationsobjekt. 
  
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
|[UserConfigurationName](userconfigurationname.md) <br/> |Der Name eines Benutzers Configuration-Objekts darstellt. Dieses Element muss verwendet werden, wenn Sie eine Benutzer-Konfigurationsobjekt erstellen.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert die Benutzer Konfiguration Element-ID an.  <br/> |
|[Wörterbuch](dictionary.md) <br/> |Definiert eine Reihe von Einträgen in Wörterbuch-Eigenschaft für eine Benutzer-Konfigurationsobjekt.  <br/> |
|[XmlData](xmldata.md) <br/> |Enthält Inhalt für die XML-Eigenschaft für eine Benutzer-Konfigurationsobjekt.  <br/> |
|[BinaryData](binarydata.md) <br/> |Enthält Inhalt von Binärdaten-Eigenschaft für eine Benutzer-Konfigurationsobjekt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |Eine Anforderung zum Erstellen eines Benutzers Konfiguration-Objekts darstellt.  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |Stellt eine Antwort, die ein Benutzer Configuration-Objekt zurückgibt.  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |Stellt eine Anforderung zum Aktualisieren einer Benutzer-Konfigurationsobjekt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

