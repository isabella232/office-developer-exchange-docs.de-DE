---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: Das RecurringMasterItemIdRanges-Element gibt ein Array von Vorkommenbereichen an.
ms.openlocfilehash: 582cbe27d468c1ff7ec22f03ba9f6976d244e234
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529370"
---
# <a name="recurringmasteritemidranges"></a>RecurringMasterItemIdRanges

Das **RecurringMasterItemIdRanges-Element** gibt ein Array von Vorkommenbereichen an. 
  
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
|**Id** <br/> |Der Textwert des **Id-Attributs** ist der eindeutige Bezeichner eines wiederkehrenden Masterelements. Dies ist ein **Zeichenfolgenwert.**  <br/> |
|**ChangeKey** <br/> |Der Textwert des **ChangeKey-Attributs** ist der Änderungsschlüssel des Serienmasterelements. Dies ist ein **Zeichenfolgenwert.**  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Ranges](ranges.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ItemIds](itemids.md)  |  [GlobalItemIds](globalitemids.md)  |  [DraftItemIds](draftitemids.md)  |  [ContactIds](contactids.md)  |  [GroupIds](groupids.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

