---
title: Anrufer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: Das Anruf-ID-Element gibt den Bezeichner eines Telefonanrufs an. Dieses Element ist erforderlich.
ms.openlocfilehash: 3e4b9dba5e8be6e45a0c16508531fbc6cf91c170
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459700"
---
# <a name="phonecallid"></a>Anrufer

Das **Anruf** -ID-Element gibt den Bezeichner eines Telefonanrufs an. Dieses Element ist erforderlich. 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt den Telefonanruf an, der getrennt werden soll. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |Stellt eine Anforderung zum Trennen eines Anrufs dar.  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |Stellt eine Anforderung zum Abrufen von Telefonanruf Informationen dar.  <br/> |
|[PlayOnPhoneResponse (Exchange Webdienste)](playonphoneresponse-exchange-web-services.md) <br/> |Definiert eine Antwort auf eine PlayOnPhone-Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

