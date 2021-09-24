---
title: Anforderung (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: Das Request-Element stellt eine SOAP-Anforderung (GetFederationInformationRequest) dar.
ms.openlocfilehash: 77ea1f14e98ed09a2a60efed4045ef8d903b3b05
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525582"
---
# <a name="request-getfederationinformation-soap"></a>Anforderung (GetFederationInformation) (SOAP)

Das **Request-Element** stellt eine [SOAP-Anforderung (GetFederationInformationRequest)](getfederationinformationrequest-soap.md) dar. 
  
```XML
<Request>
   <Domain/>
</Request>
```

 **GetFederationInformationRequest**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Domäne (GetFederationInformation) (SOAP)](domain-getfederationinformationsoap.md) <br/> |Identifiziert die Domäne, die über eine Verbundvertrauensstellung verfügt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFederationInformationRequestMessage (SOAP)](getfederationinformationrequestmessage-soap.md) <br/> |Bereitet einen Aufruf an den Server vor, um Konfigurationsdaten für den Sicherheitstokendienst (Security Token Service, STS) anzufordern.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Arbeiten mit AutoErmittlung](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

