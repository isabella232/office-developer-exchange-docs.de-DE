---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: Das AdditionalInfo-Element gibt zusätzliche Informationen zum Aufbewahrungsstatus eines Postfachs an.
ms.openlocfilehash: d8b707fb04ffe91d5c7aa793c6b56c8bb048f160
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544318"
---
# <a name="additionalinfo"></a>AdditionalInfo

Das **AdditionalInfo-Element** gibt zusätzliche Informationen zum Aufbewahrungsstatus eines Postfachs an. 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 **xs:string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxHoldStatus](mailboxholdstatus.md) <br/> |Gibt den Aufbewahrungsstatus des Postfachs an.  <br/> |
|[NonIndexableItemDetail](nonindexableitemdetail.md) <br/> |Gibt Details für ein Element an, das nicht indiziert werden kann.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des AdditionalInfo-Elements sind zusätzliche Informationen zum Haltestatus eines Postfachs.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist optional.
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

