---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: Das GroupIdentifier-Element stellt einen einzelnen Sicherheitsbezeichner und ein Attribut für eine Active Directory-Verzeichnisdienst-Objektgruppe dar, in der das Konto Mitglied ist.
ms.openlocfilehash: c96d0ca673d9b488266f08abbbd6546aaeb9f5a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533159"
---
# <a name="groupidentifier"></a>GroupIdentifier

Das **GroupIdentifier-Element** stellt einen einzelnen Sicherheitsbezeichner und ein Attribut für eine Active Directory-Verzeichnisdienst-Objektgruppe dar, in der das Konto Mitglied ist. 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 **SidAndAttributesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Attributes** <br/> |Enthält Gruppenattribute.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Securityidentifier](securityidentifier.md) <br/> |Stellt die SDDL-Form (Security Descriptor Definition Language) eines Sicherheitsbezeichners[(SID)](sid.md)dar, der die Gruppe darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupSids](groupsids.md) <br/> |Stellt eine Auflistung von Sicherheitsbezeichnern des Active Directory-Gruppenobjekts dar, die ein Kontotoken für die Token-Serialisierung bilden. Die Token-Serialisierung wird nicht unterstützt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

