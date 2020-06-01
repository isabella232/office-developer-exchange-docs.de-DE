---
title: GetDiscoverySearchConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b84a4c6-cb0a-4bca-85b2-fec32227930b
description: Das GetDiscoverySearchConfigurationResponseMessage-Element gibt die Antwortnachricht für eine GetDiscoverySearchConfiguration-Anforderung an.
ms.openlocfilehash: 23d1c5b7a61a9161d7383ec8b38cd0ebbebfc8cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460974"
---
# <a name="getdiscoverysearchconfigurationresponsemessage"></a>GetDiscoverySearchConfigurationResponseMessage

Das **GetDiscoverySearchConfigurationResponseMessage** -Element gibt die Antwortnachricht für eine **GetDiscoverySearchConfiguration** -Anforderung an. 
  
```XML
<GetDiscoverySearchConfigurationResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponseMessage>
```

 **GetDiscoverySearchConfigurationResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[MessageText](messagetext.md)  |  [Response Code](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [Messagexml verwendet](messagexml.md)  |  [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ResponseMessages](responsemessages.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

