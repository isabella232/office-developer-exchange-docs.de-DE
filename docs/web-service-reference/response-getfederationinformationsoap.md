---
title: Antwort (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Das Antwort-Element enthält die GetFederationInformation-Vorgang (SOAP) Antwortinformationen.
ms.openlocfilehash: 946cba56d7503a0e20ec59640f4f1258c00a844e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831171"
---
# <a name="response-getfederationinformation-soap"></a>Antwort (GetFederationInformation) (SOAP)

Das **Antwort** -Element enthält die [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) Antwort-Informationen. 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 **GetFederationInformationResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Definiert den Ort einer Anwendung.  <br/> |
|[Domänen (SOAP)](domains-soap.md) <br/> |Stellt die Domäne-Auflistung in einer [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)oder die Domänen an, denen die Organisation in einem [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)im Verbund wurde die Konfigurationen für die zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |Definiert eine Antwort auf eine [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) an.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md)

