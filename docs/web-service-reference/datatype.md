---
title: DataType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: Das DataType-Element beschreibt die Art der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.
ms.openlocfilehash: b1adac8e3029abd64df96ab1560706babe4b12f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757862"
---
# <a name="datatype"></a>DataType

Das **DataType** -Element beschreibt die Art der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden. 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

**SharingDataType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für die **DataType** -Element. 
  
**DataType-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Gibt an, dass der freigegebene Ordner Kalenderinformationen enthält.  <br/> |
|Kontakte  <br/> |Gibt an, dass der freigegebene Ordner Kontaktinformationen enthält.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

