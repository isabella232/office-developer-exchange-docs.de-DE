---
title: AnonymousAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: Das AnonymousAccessAllowed-Element gibt an, ob ein Dokument sharing-Location als authentifizierten Benutzer erforderlich ist.
ms.openlocfilehash: 7ca208aa0d75b254463400a5e207079d722fc0a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757270"
---
# <a name="anonymousaccessallowed-soap"></a>AnonymousAccessAllowed (SOAP)

Das **AnonymousAccessAllowed** -Element gibt an, ob ein Dokument sharing-Location als authentifizierten Benutzer erforderlich ist. 
  
```XML
<AnonymousAccessAllowed /> 
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Stellt Informationen zum Standort und Metadaten für ein Dokument sharing-Location.  <br/> |
   
## <a name="text-value"></a>Textwert

Der boolesche Wert des **AnonymousAccessAllowed** -Elements gibt an, ob den freigegebene Speicherort als authentifizierten Benutzer erforderlich ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP-Autodiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

