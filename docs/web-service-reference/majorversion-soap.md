---
title: Hauptversion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0b2a83cf-e173-4073-9603-b2ea3b36ec1a
description: Das Hauptversion-Element darstellt, der die Hauptversionsnummer für den Server.
ms.openlocfilehash: ca619d4c36e17ca9a811019f0a13b45353cab1e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830333"
---
# <a name="majorversion-soap"></a>Hauptversion (SOAP)

Das **Hauptversion** -Element darstellt, der die Hauptversionsnummer für den Server. 
  
```XML
<MajorVersion/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Enthält die Version des Servers, der die Anforderung verarbeitet.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für das Element **Hauptversion** ist eine ganze Zahl, die die Nummer der Hauptversion des Servers darstellt, der die Anforderung verarbeitet. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
  
[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

