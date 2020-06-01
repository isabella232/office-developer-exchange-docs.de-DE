---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: Das GetServiceConfiguration-Element definiert eine GetServiceConfiguration-Anforderung.
ms.openlocfilehash: e9357a9e3be22e129c4910c01231f9dbd22a2dbe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457872"
---
# <a name="getserviceconfiguration"></a>GetServiceConfiguration

Das **GetServiceConfiguration** -Element definiert eine GetServiceConfiguration-Anforderung. 
  
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
|[Actingies](actingas.md) <br/> |Gibt an, wen der Anrufer sendet. Dieses Element ist optional. Wenn dieses Element nicht vorhanden ist, wird der authentifizierte Benutzer als Absender angenommen. Das **actings** -Element muss enthalten sein, um Absender Hinweise anzufordern. Ein ErrorInvalidArgument-Fehler kann in einer Antwort zurückgegeben werden, wenn das **actings** -Element fehlt, keinen Routingtyp enthält, keine e-Mail-Adresse enthält, eine ungültige e-Mail-Adresse auflöst, für einen Benutzer in Active Directory-Domänendienste (AD DS) nicht aufgelöst wird oder in AD DS in mehrere Benutzer aufgelöst wird.  <br/> |
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Enthält die angeforderten Dienstkonfigurationen. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
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

