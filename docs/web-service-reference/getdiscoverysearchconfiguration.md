---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: Das GetDiscoverySearchConfiguration-Element gibt eine Anforderung zum Abrufen der eDiscovery-Suchkonfiguration an.
ms.openlocfilehash: ff84e648e14b79f64cf2a769c83aae28791790ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519688"
---
# <a name="getdiscoverysearchconfiguration"></a>GetDiscoverySearchConfiguration

Das **GetDiscoverySearchConfiguration-Element** gibt eine Anforderung zum Abrufen der eDiscovery-Suchkonfiguration an. 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 **GetDiscoverySearchConfigurationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |Gibt den Bezeichner der Suche an.  <br/> |
|[ExpandGroupMembership](expandgroupmembership.md) <br/> |Enthält einen booleschen Wert, der angibt, ob die Mitgliedschaft der Gruppe erweitert werden soll, die von einer **GetSearchableMailboxes-Anforderung** zurückgegeben wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

