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
ms.openlocfilehash: dea6e36c51ceea53201b668cfba616c03a44df86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456962"
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
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Gibt das Ziel der Umleitung an. Das Ziel kann entweder eine URL oder eine e-Mail-Adresse sein.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Gibt den Fehlercode an, der der spezifischen Anforderung zugeordnet ist.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Gibt die Fehlermeldung an, die der spezifischen Anforderung zugeordnet ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |Enthält ein Array von **DomainResponse** -Elementen. Jedes **DomainResponse** -Element enthält die angeforderten Einstellungen für den angegebenen Benutzer.  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Enthält die Antworten für jede Domäne.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)

