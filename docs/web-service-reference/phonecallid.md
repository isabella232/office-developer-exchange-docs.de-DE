---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: Das PhoneCallId-Element gibt den Bezeichner eines Telefonanrufs an. Dieses Element ist erforderlich.
ms.openlocfilehash: 00b23c8b4023a6fef9c27295c8e023e5324b7026
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528319"
---
# <a name="phonecallid"></a>PhoneCallId

Das **PhoneCallId-Element** gibt den Bezeichner eines Telefonanrufs an. Dieses Element ist erforderlich. 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Identifiziert den Telefonanruf, der getrennt werden soll. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |Stellt eine Anforderung zum Trennen eines Anrufs dar.  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |Stellt eine Anforderung zum Abrufen von Telefonanrufinformationen dar.  <br/> |
|[PlayOnPhoneResponse (Exchange-Webdienste)](playonphoneresponse-exchange-web-services.md) <br/> |Definiert eine Antwort auf eine PlayOnPhone-Anforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

