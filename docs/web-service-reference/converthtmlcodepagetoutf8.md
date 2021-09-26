---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: Das ConvertHtmlCodePageToUTF8-Element gibt an, ob der HTML-Textkörper des Elements in UTF8 konvertiert wird.
ms.openlocfilehash: e43de22b6d8050c14eb18d0fdd5a72f463335189
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545573"
---
# <a name="converthtmlcodepagetoutf8"></a>ConvertHtmlCodePageToUTF8

Das **ConvertHtmlCodePageToUTF8-Element** gibt an, ob der HTML-Textkörper des Elements in UTF8 konvertiert wird. 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 **xs:boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert einen Satz von Eigenschaften, die in einer Antwort zurückgegeben werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **ConvertHtmlCodePageToUTF8-Element** gibt an, dass der HTML-Textkörper in UTF8 konvertiert wird. Der Textwert **"false"** gibt an, dass der HTML-Textkörper nicht in UTF8 konvertiert wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Standardwert **"true"** wird verwendet, wenn das **ConvertHtmlCodePageToUTF8-Element** nicht in einer Anforderung angegeben ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

