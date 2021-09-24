---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: Das RequestedServerVersion-Element gibt die Serverversion an, auf die eine AutoErmittlungsmethode abzielt.
ms.openlocfilehash: 0690481523ab48497c40338a8808dfa2ed9b0e99
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540559"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

Das **RequestedServerVersion-Element** gibt die Serverversion an, auf die eine **AutoErmittlungsmethode** abzielt. 
  
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

Keine
  
## <a name="text-value"></a>Textwert

Der Textwert des **RequestedServerVersion-Elements** gibt die Serverversion an, auf die eine **AutoErmittlungsmethode** abzielt. In der folgenden Tabelle sind die gültigen Serverversionen aufgeführt. 
  
|**Textwert**|**Beschreibung**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. Das Exchange2013-Feld gilt für Clients, die ab Exchange Server 2013 auf Exchange Online und Versionen von Exchange abzielen.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). Das Feld Exchange2013_SP1 gilt für Clients, die ab Exchange Server 2013 SP1 auf Exchange Online und Versionen von Exchange abzielen.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **RequestedServerVersion-Element** wird im SOAP-Header festgelegt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   

