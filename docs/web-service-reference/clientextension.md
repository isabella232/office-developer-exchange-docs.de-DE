---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: Das ClientExtension-Element enthält die Benutzer- und Konfigurationsdaten Informationen zu einer app.
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757568"
---
# <a name="clientextension"></a>ClientExtension

Das **ClientExtension** -Element enthält die Benutzer- und Konfigurationsdaten Informationen zu einer app. 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 **ClientExtensionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|IsAvailable  <br/> |Gibt an, ob die app verfügbar ist. Der Textwert **true** für das **IsAvailable** -Attribut gibt an, dass die app zur Verfügung steht. Der Wert **false** gibt an, dass die app nicht verfügbar ist. Dieses Attribut ist optional.  <br/> |
|IsMandatory  <br/> |Gibt an, ob die app zwingend erforderlich ist. Der Textwert **true** für das **IsMandatory** -Attribut gibt an, dass die app für das Postfach zwingend erforderlich ist. Der Wert **false** gibt an, dass die app nicht zwingend erforderlich ist. Dieses Attribut ist optional.  <br/> |
|IsEnabledByDefault  <br/> |Gibt an, ob die app standardmäßig aktiviert ist. Der Textwert **true** für das **IsEnabledByDefault** -Attribut gibt an, dass die app standardmäßig aktiviert ist. Der Wert **false** gibt an, dass die app standardmäßig nicht aktiviert ist. Dieses Attribut ist optional.  <br/> |
|ProvidedTo  <br/> |Gibt an, auf denen die app bereitgestellt wird. Dieses Attribut ist optional.  <br/> |
|Typ  <br/> |Gibt den Typ der app.  <br/> |
|Umfang  <br/> |Gibt den Umfang der app.  <br/> |
|MarketplaceAssetId  <br/> |Gibt die Marketplace-Anlage-ID der app.  <br/> |
|MarketplaceContentMarket  <br/> |Gibt den Marketplace-Inhalt, den ein Benutzer sieht ausführliche und über eine app überprüft.  <br/> |
|AppStatus  <br/> |Gibt den Statuscode einer Mail-App in einem unerwarteten Zustand.  <br/> |
|Etoken  <br/> |Gibt das Lizenztoken für kostenpflichtige oder Testversion Mail-apps.  <br/> |
   
#### <a name="type"></a>Typ

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Standard  <br/> |Gibt an, dass die app standardmäßig verfügbar ist.  <br/> |
|Privat  <br/> |Gibt an, dass die app privat ist.  <br/> |
|MarketPlace  <br/> |Gibt an, dass die app eine app Marketplace ist.  <br/> |
   
#### <a name="scope"></a>Umfang

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass die app keine Bereich verfügt.  <br/> |
|Benutzer  <br/> |Gibt an, dass die app pro Benutzer ist.  <br/> |
|Organisation  <br/> |Gibt an, dass die app für eine Organisation ist.  <br/> |
|Standard  <br/> |Gibt an, dass die app eine app Standard ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Gibt die e-Mail-Konten, die die app zugreifen können.  <br/> |
|[Manifest](manifest.md) <br/> |Enthält die Base64-codierte app-Manifestdatei.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Gibt ein Array von **ClientExtension** -Elementen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

