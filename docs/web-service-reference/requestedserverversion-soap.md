---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: Das RequestedServerVersion-Element gibt die Server Version an, die von einer autodiscover-Methode als Ziel bezeichnet wird.
ms.openlocfilehash: ff63c82943bdd3476a4284f5aa2075fc9c0194b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467907"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

Das **RequestedServerVersion** -Element gibt die Server Version an, die von einer **autodiscover** -Methode als Ziel bezeichnet wird. 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Der Textwert des **RequestedServerVersion** -Elements gibt die Server Version an, die von einer **AutoErmittlungs** -Methode als Ziel bezeichnet wird. In der folgenden Tabelle sind die gültigen Server Versionen aufgeführt. 
  
|**Textwert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. Das Feld Exchange2013 gilt für Clients, die auf Exchange Online und Exchange-Versionen, die mit Exchange Server 2013 beginnen, abzielen.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). Das Feld Exchange2013_SP1 gilt für Clients, die auf Exchange Online und Exchange-Versionen ab Exchange Server 2013 SP1 abzielen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **RequestedServerVersion** -Element wird im SOAP-Header festgelegt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

