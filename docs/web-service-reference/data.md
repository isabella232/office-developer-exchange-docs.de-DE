---
title: Daten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: f875e6c2-be18-439a-a7b1-bb49a149b538
description: Data-Element enthält die verschlüsselte Daten, die die freigegebenen Daten darstellt.
ms.openlocfilehash: acd66691f16d11f41dee5efb9de03c129ff416c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757843"
---
# <a name="data"></a>Daten

**Data** -Element enthält die verschlüsselte Daten, die die freigegebenen Daten darstellt. 
  
- [EncryptedSharedFolderData](encryptedsharedfolderdata.md)  
- [Data](data.md)
  
```xml
<Data/>
```

**EncryptedDataContainerType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EncryptedSharedFolderData](encryptedsharedfolderdata.md) <br/> |Enthält die verschlüsselten Daten, die ein Client verwenden können, um die Freigabe von dessen Kalender zu autorisieren, oder wenden Sie Daten mit anderen Clients.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

