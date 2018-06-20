---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: Das RequestServerVersion-Element enthält die Versionsinformationen, die die Schemaversion als Ziel für eine Anforderung identifiziert.
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831143"
---
# <a name="requestserverversion"></a>RequestServerVersion

Das **RequestServerVersion** -Element enthält die Versionsinformationen, die die Schemaversion als Ziel für eine Anforderung identifiziert. 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Version  <br/> |Beschreibt die Version als Ziel für die Anforderung. Dieses Attribut ist erforderlich, wenn die Zielversion Server eine Version von Exchange, beginnend mit Exchange Server 2010 ist.  <br/> |
   
#### <a name="version-attribute-values"></a>Version-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007  <br/> |Ziel der ursprünglich freigegebenen Version von Exchange 2007-Schemadateien.  <br/> |
|Exchange2007_SP1  <br/> |Ziel: die Schemadateien für Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) und Exchange 2007 Service Pack 3 (SP3).  <br/> |
|Exchange2010  <br/> |Ziel: die Schemadateien für Exchange 2010 ein.  <br/> |
|Exchange2010_SP1  <br/> |Ziel: die Schemadateien für Exchange 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Ziel: die Schemadateien für Exchange 2010 Service Pack 2 (SP2) und Exchange 2010 Service Pack 3 (SP3).  <br/> |
|Exchange2013  <br/> |Ziel: die Schemadateien für Exchange 2013.  <br/> |
|Exchange2013_SP1  <br/> |Ziel: die Schemadateien für Exchange 2013 Service Pack 1 (SP1).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Das Element **RequestServerVersion** befindet sich die SOAP-Header. 
  
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



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Versioning Anfragen](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

