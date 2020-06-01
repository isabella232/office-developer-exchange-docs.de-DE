---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: Das AdditionalInfo-Element gibt zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs an.
ms.openlocfilehash: 1911ff3ac0baf7a8854c0609e08959a54cc27b6d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455821"
---
# <a name="additionalinfo"></a>AdditionalInfo

Das **AdditionalInfo** -Element gibt zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs an. 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 **xs: Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxHoldStatus](mailboxholdstatus.md) <br/> |Gibt den Aufbewahrungs Status des Postfachs an.  <br/> |
|[NonIndexableItemDetail](nonindexableitemdetail.md) <br/> |Gibt Details für ein Element an, das nicht indiziert werden kann.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des AdditionalInfo-Elements ist zusätzliche Informationen zum Aufbewahrungs Status eines Postfachs.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element ist optional.
  
Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

