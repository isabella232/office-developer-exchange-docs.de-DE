---
title: Antwort (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: Das Antwort-Element darstellt, die Antwort zu einem Anruf GetDomainSettings für eine einzelne Domäne.
ms.openlocfilehash: 316d77104894cf5ed9121e7dab1c38646765c948
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831169"
---
# <a name="response-getdomainsettings-soap"></a>Antwort (GetDomainSettings) (SOAP)

Das **Antwort** -Element darstellt, die Antwort zu einem Anruf **GetDomainSettings** für eine einzelne Domäne. 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält die Antwort für jede Domäne in einer Anforderung **GetDomainSettings** angefordert.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Enthält den Fehlercode, der die Antwort zugeordnet ist, falls zutreffend.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Enthält die Fehlermeldung, die die Antwort zugeordnet ist, falls zutreffend.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |Mit dem Anrufer die Domäne gibt Konfigurationseinstellungen zurück.  <br/> |
   
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



[GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

