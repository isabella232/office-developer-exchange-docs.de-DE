---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: Das RequestServerVersion-Element enthält die Versionsverwaltungsinformationen, die die Schemaversion für eine Anforderung angeben.
ms.openlocfilehash: 4f01d5fcc2a2e08d426efc8d1f0a193d6139a038
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541875"
---
# <a name="requestserverversion"></a>RequestServerVersion

Das **RequestServerVersion-Element** enthält die Versionsverwaltungsinformationen, die die Schemaversion für eine Anforderung angeben. 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Version  <br/> |Beschreibt die Version, auf die die Anforderung ausgerichtet werden soll. Dieses Attribut ist erforderlich, wenn die Zielserverversion eine Version von Exchange ab Exchange Server 2010 ist.  <br/> |
   
#### <a name="version-attribute-values"></a>Versionsattributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007  <br/> |Richten Sie die Schemadateien für die erste Version von Exchange 2007 ein.  <br/> |
|Exchange2007_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) und Exchange 2007 Service Pack 3 (SP3) ein.  <br/> |
|Exchange2010  <br/> |Richten Sie die Schemadateien für Exchange 2010 als Ziel ein.  <br/> |
|Exchange2010_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2010 Service Pack 1 (SP1) ein.  <br/> |
|Exchange2010_SP2  <br/> |Richten Sie die Schemadateien für Exchange 2010 Service Pack 2 (SP2) und Exchange 2010 Service Pack 3 (SP3) ein.  <br/> |
|Exchange2013  <br/> |Richten Sie die Schemadateien für Exchange 2013 als Ziel ein.  <br/> |
|Exchange2013_SP1  <br/> |Richten Sie die Schemadateien für Exchange 2013 Service Pack 1 (SP1) ein.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Das **RequestServerVersion-Element** befindet sich im SOAP-Header. 
  
## <a name="remarks"></a>HinwBemerkungeneise

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


[Versionsverwaltungsanforderungen](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

