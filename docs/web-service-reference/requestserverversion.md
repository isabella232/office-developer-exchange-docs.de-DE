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
description: Das RequestServerVersion-Element enthält die Versions Verwaltungsinformationen, die die Schemaversion identifiziert, die für eine Anforderung als Ziel festgelegt werden soll.
ms.openlocfilehash: c4ae59a03c812d21153e4338734185d933d914ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468320"
---
# <a name="requestserverversion"></a>RequestServerVersion

Das **RequestServerVersion** -Element enthält die Versions Verwaltungsinformationen, die die Schemaversion identifiziert, die für eine Anforderung als Ziel festgelegt werden soll. 
  
```XML
<RequestServerVersion Version=""/>
```

 **Einfachen exchangeversiontype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Version  <br/> |Beschreibt die Zielversion für die Anforderung. Dieses Attribut ist erforderlich, wenn die Zielserver Version eine Version von Exchange ist, die mit Exchange Server 2010 beginnt.  <br/> |
   
#### <a name="version-attribute-values"></a>Version-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007  <br/> |Richten Sie die Schemadateien für die erste Version von Exchange 2007 ein.  <br/> |
|Exchange2007_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) und Exchange 2007 Service Pack 3 (SP3) aus.  <br/> |
|Exchange2010  <br/> |Richten Sie die Schemadateien für Exchange 2010 ein.  <br/> |
|Exchange2010_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2010 Service Pack 1 (SP1) ein.  <br/> |
|Exchange2010_SP2  <br/> |Richten Sie die Schemadateien für Exchange 2010 Service Pack 2 (SP2) und Exchange 2010 Service Pack 3 (SP3) aus.  <br/> |
|Exchange2013  <br/> |Richten Sie die Schemadateien für Exchange 2013 ein.  <br/> |
|Exchange2013_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2013 Service Pack 1 (SP1) ein.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Das **RequestServerVersion** -Element befindet sich im SOAP-Header. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Anforderungen für die Versionsverwaltung](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

