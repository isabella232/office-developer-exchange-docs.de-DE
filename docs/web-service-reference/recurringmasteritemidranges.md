---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: Das RecurringMasterItemIdRanges-Element gibt ein Array von Ereignis Bereichen an.
ms.openlocfilehash: 784676844c5c58c65b8cc6177843bf26d351b7d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528755"
---
# <a name="recurringmasteritemidranges"></a>RecurringMasterItemIdRanges

Das **RecurringMasterItemIdRanges** -Element gibt ein Array von Ereignis Bereichen an. 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 **RecurringMasterItemIdRangesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Der Textwert des **ID-** Attributs ist die eindeutige ID eines wiederkehrenden Hauptelements. Dies ist ein **String** -Wert.  <br/> |
|**ChangeKey** <br/> |Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel des wiederkehrenden Hauptelements. Dies ist ein **String** -Wert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Ranges](ranges.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Itemids](itemids.md)  |  [GlobalItemIds](globalitemids.md)  |  [DraftItemIds](draftitemids.md)  |  [ContactIds](contactids.md) Die  |  [GroupIds](groupids.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

