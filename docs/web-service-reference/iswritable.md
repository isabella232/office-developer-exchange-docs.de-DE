---
title: Isschreibbar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: Das IsWriteable-Element gibt an, ob der zugrunde liegende Kontakt oder Active Directory Empfänger in geschrieben werden kann.
ms.openlocfilehash: 96075adc1772027456f8829eee43bdc734644c09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467571"
---
# <a name="iswritable"></a>Isschreibbar

Das **IsWriteable** -Element gibt an, ob der zugrunde liegende Kontakt oder Active Directory Empfänger in geschrieben werden kann. 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **isschreibbar** -Element gibt an, dass das Kontakt-oder Active Directory Objekt für den Schreibzugriff verfügbar ist. Der Wert **false** gibt an, dass das Kontakt-oder Active Directory Objekt für den Schreibzugriff nicht verfügbar ist. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

