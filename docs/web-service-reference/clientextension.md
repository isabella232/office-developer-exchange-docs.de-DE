---
title: Client Extension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: Das Client Extension-Element enthält Benutzer-und Konfigurationsinformationen zu einer App.
ms.openlocfilehash: d3d9ce1d242a63f28da3464f0faff86abde502c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460197"
---
# <a name="clientextension"></a>Client Extension

Das **Client Extension** -Element enthält Benutzer-und Konfigurationsinformationen zu einer App. 
  
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
|IsAvailable  <br/> |Gibt an, ob die app verfügbar ist. Der Textwert **true** für das **IsAvailable** -Attribut gibt an, dass die app verfügbar ist. Der Wert **false** gibt an, dass die APP nicht verfügbar ist. Dieses Attribut ist optional.  <br/> |
|Ismandatory  <br/> |Gibt an, ob die APP obligatorisch ist. Der Textwert **true** für das Attribut **ismandatory** gibt an, dass die APP für das Postfach obligatorisch ist. Der Wert **false** gibt an, dass die APP nicht zwingend ist. Dieses Attribut ist optional.  <br/> |
|IsEnabledByDefault  <br/> |Gibt an, ob die App standardmäßig aktiviert ist. Der Textwert **true** für das **IsEnabledByDefault** -Attribut gibt an, dass die App standardmäßig aktiviert ist. Der Wert **false** gibt an, dass die App standardmäßig nicht aktiviert ist. Dieses Attribut ist optional.  <br/> |
|ProvidedTo  <br/> |Gibt an, wem die APP bereitgestellt wird. Dieses Attribut ist optional.  <br/> |
|Typ  <br/> |Gibt den Typ der APP an.  <br/> |
|Bereich  <br/> |Gibt den Bereich der APP an.  <br/> |
|MarketplaceAssetId  <br/> |Gibt die Marketplace-Objekt-ID der APP an.  <br/> |
|MarketplaceContentMarket  <br/> |Gibt die Marketplace-Inhalte an, die ein Benutzer für Details und Besprechungen zu einer APP sieht.  <br/> |
|AppStatus  <br/> |Gibt den Statuscode einer Mail-app in einem unerwarteten Zustand an.  <br/> |
|EToken  <br/> |Gibt das Lizenztoken für kostenpflichtige oder Test-e-Mail-apps an.  <br/> |
   
#### <a name="type"></a>Typ

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Standard  <br/> |Gibt an, dass die App standardmäßig verfügbar ist.  <br/> |
|Private  <br/> |Gibt an, dass die APP privat ist.  <br/> |
|Markt  <br/> |Gibt an, dass die APP eine Marketplace-APP ist.  <br/> |
   
#### <a name="scope"></a>Bereich

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Gibt an, dass die APP keinen Bereich aufweist.  <br/> |
|User  <br/> |Gibt an, dass die APP pro Benutzer ist.  <br/> |
|Organisation  <br/> |Gibt an, dass die APP für eine Organisation ist.  <br/> |
|Standard  <br/> |Gibt an, dass die APP eine Standard-APP ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Gibt die e-Mail-Konten an, die auf die App zugreifen können.  <br/> |
|[Manifest](manifest.md) <br/> |Enthält die codierte App-Manifestdatei von Base-64.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Gibt ein Array von **Client Extension** -Elementen an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

