---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: Das GetServiceConfiguration-Element definiert eine GetServiceConfiguration-Anforderung.
ms.openlocfilehash: fdc4fd84c658dd0cd2ecabe7fefc06113bca173a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533434"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

Das **GetServiceConfiguration-Element** definiert eine GetServiceConfiguration-Anforderung. 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 **GetServiceConfigurationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Gibt an, an wen der Anrufer gesendet wird. Dieses Element ist optional. Wenn dieses Element nicht vorhanden ist, wird davon ausgegangen, dass der authentifizierte Benutzer der Absender ist. Das **ActingAs-Element** muss zum Anfordern von Absenderhinweisen eingeschlossen werden. Ein ErrorInvalidArgument-Fehler kann in einer Antwort zurückgegeben werden, wenn das **ActingAs-Element** fehlt, keinen Routingtyp enthält, keine E-Mail-Adresse enthält, eine ungültige E-Mail-Adresse enthält, nicht zu einem Benutzer in Active Directory Domain Services (AD DS) aufgelöst wird oder in mehrere Benutzer in AD DS aufgelöst wird.  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Enthält die angeforderten Dienstkonfigurationen. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
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

