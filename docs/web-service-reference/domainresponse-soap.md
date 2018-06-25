---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: Das DomainResponse-Element enthält die angeforderten Einstellungen für die angegebene Domäne.
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758091"
---
# <a name="domainresponse-soap"></a>DomainResponse (SOAP)

Das **DomainResponse** -Element enthält die angeforderten Einstellungen für die angegebene Domäne. 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 **DomainResponse**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Enthält Informationen für die Einstellungen, die nicht zurückgegeben werden kann.  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Stellt die domäneneinstellungen, die in einer autoermittlungsanforderung für die gesendet oder von einer Antwort der AutoErmittlung zurückgegeben wurden.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Identifiziert die als Ziel für die Umleitung an. Das Ziel kann eine URL oder eine e-Mail-Adresse sein.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Gibt den Fehlercode, der bestimmte Anforderung zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Gibt die Fehlermeldung, die die spezifische Anforderung zugeordnet ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |Enthält ein Array von **DomainResponse** -Elementen. Jedes Element **DomainResponse** enthält die angeforderten Einstellungen für den angegebenen Benutzer.  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält die Antworten für jede Domäne.  <br/> |
   
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

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

