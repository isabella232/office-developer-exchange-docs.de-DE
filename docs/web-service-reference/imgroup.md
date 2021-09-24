---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: Das ImGroup-Element stellt eine Chatgruppe dar.
ms.openlocfilehash: 6bcf3a8c587ba1c14aadfaa792cbd2f9405c69ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533111"
---
# <a name="imgroup"></a>ImGroup

Das **ImGroup-Element** stellt eine Chatgruppe dar. 
  
```XML
<ImGroup>
   <DisplayName/>
   <GroupType/>
   <ExchangeStoreId/>
   <MemberCorrelationKey/>
   <ExtendedProperties/>
   <SmtpAddress/>
</ImGroup>
```

 **ImGroupType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)  |  [GroupType](grouptype.md)  |  [ExchangeStoreId](exchangestoreid.md)  |  [MemberCorrelationKey](membercorrelationkey.md)  |  [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [SmtpAddress](smtpaddress.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Gruppen (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)  |  [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  |  [AddImGroupResponse](addimgroupresponse.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

