---
title: AnonymousAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bf819a65-30f2-4881-a34f-cb30a9c2b6a7
description: Das AnonymousAccessAllowed-Element gibt an, ob ein Dokumentfreigabespeicherort einen authentifizierten Benutzer erfordert.
ms.openlocfilehash: bf31b8dd4e61393539a1cba0387d1fbbc7f282d7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516125"
---
# <a name="anonymousaccessallowed-soap"></a>AnonymousAccessAllowed (SOAP)

Das **AnonymousAccessAllowed-Element** gibt an, ob ein Dokumentfreigabespeicherort einen authentifizierten Benutzer erfordert. 
  
```XML
<AnonymousAccessAllowed /> 
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Stellt Standort- und Metadateninformationen für einen Speicherort für die Dokumentfreigabe dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der boolesche Wert des **AnonymousAccessAllowed-Elements** gibt an, ob für den Freigabespeicherort ein authentifizierter Benutzer erforderlich ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

