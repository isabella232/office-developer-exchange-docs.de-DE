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
description: Das RequestedServerVersion-Element gibt die Serverversion, dass eine Methode für die AutoErmittlung Ziele aufrufen.
ms.openlocfilehash: 6b9d31f3b7bca087652f04e4943becc5ac4e68e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831132"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

Das **RequestedServerVersion** -Element gibt die Serverversion, dass eine Methode **für die AutoErmittlung** Ziele aufrufen. 
  
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

Der Textwert der **RequestedServerVersion** -Element gibt die Serverversion, dass eine Methode **für die AutoErmittlung** Ziele aufrufen. Die folgende Tabelle enthält die gültigen Serverversionen. 
  
|**Textwert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. Das Feld Exchange2013 ist für Clients, die Exchange Online und Exchange beginnend mit Exchange Server 2013-Versionen abzielen.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). Das Feld Exchange2013_SP1 ist für Clients, die Exchange Online und Versionen von Exchange, beginnend mit Exchange Server 2013 SP1 abzielen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **RequestedServerVersion** -Element wird in den SOAP-Header festgelegt. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

