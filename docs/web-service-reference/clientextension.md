---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: Das ClientExtension-Element enthält Benutzer- und Konfigurationsinformationen zu einer App.
ms.openlocfilehash: fa02ad0f5f4312fefecee32d2ed24f0bb0585365
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519961"
---
# <a name="clientextension"></a>ClientExtension

Das **ClientExtension-Element** enthält Benutzer- und Konfigurationsinformationen zu einer App. 
  
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
|Isavailable  <br/> |Gibt an, ob die App verfügbar ist. Der Textwert **"true"** für das **IsAvailable-Attribut** gibt an, dass die App verfügbar ist. Der Wert **"false"** gibt an, dass die App nicht verfügbar ist. Dieses Attribut ist optional.  <br/> |
|IsMandatory  <br/> |Gibt an, ob die App obligatorisch ist. Der Textwert **"true"** für das **IsMandatory-Attribut** gibt an, dass die App für das Postfach obligatorisch ist. Der Wert **"false"** gibt an, dass die App nicht obligatorisch ist. Dieses Attribut ist optional.  <br/> |
|IsEnabledByDefault  <br/> |Gibt an, ob die App standardmäßig aktiviert ist. Der Textwert **"true"** für das **IsEnabledByDefault-Attribut** gibt an, dass die App standardmäßig aktiviert ist. Der Wert **"false"** gibt an, dass die App nicht standardmäßig aktiviert ist. Dieses Attribut ist optional.  <br/> |
|ProvidedTo  <br/> |Gibt an, für wen die App bereitgestellt wird. Dieses Attribut ist optional.  <br/> |
|Typ  <br/> |Gibt den Typ der App an.  <br/> |
|Umfang  <br/> |Gibt den Bereich der App an.  <br/> |
|MarketplaceAssetId  <br/> |Gibt den Marketplace-Objektbezeichner der App an.  <br/> |
|MarketplaceContentMarket  <br/> |Gibt den Marketplace-Inhalt an, den ein Benutzer für Details und Rezensionen zu einer App sieht.  <br/> |
|AppStatus  <br/> |Gibt den Statuscode einer Mail-App in einem unerwarteten Zustand an.  <br/> |
|Etoken  <br/> |Gibt das Lizenztoken für kostenpflichtige oder Test-Mail-Apps an.  <br/> |
   
#### <a name="type"></a>Typ

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Standard  <br/> |Gibt an, dass die App standardmäßig verfügbar ist.  <br/> |
|Private  <br/> |Gibt an, dass die App privat ist.  <br/> |
|Markt  <br/> |Gibt an, dass es sich bei der App um eine Marketplace-App handelt.  <br/> |
   
#### <a name="scope"></a>Umfang

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass die App keinen Bereich hat.  <br/> |
|Benutzer  <br/> |Gibt an, dass die App pro Benutzer ausgeführt wird.  <br/> |
|Organization (Organisation)  <br/> |Gibt an, dass die App für eine Organisation vorgesehen ist.  <br/> |
|Standard  <br/> |Gibt an, dass es sich bei der App um eine Standard-App handelt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Gibt die E-Mail-Konten an, die auf die App zugreifen können.  <br/> |
|[Manifest](manifest.md) <br/> |Enthält die base64-codierte App-Manifestdatei.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Gibt ein Array von **ClientExtension-Elementen** an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

