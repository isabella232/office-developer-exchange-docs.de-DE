---
title: Bereich (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Das Scope-Element gibt den Bereich des Nachrichtenverfolgungsberichts an.
ms.openlocfilehash: 036ff1007c9e7ec9cc385f8df81c045b7b9335b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546126"
---
# <a name="scope-nonemptystringtype"></a>Bereich (NonEmptyStringType)

Das  Scope-Element gibt den Bereich des Nachrichtenverfolgungsberichts an. 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindMessageTrackingReport](findmessagetrackingreport.md)  |  [GetMessageTrackingReport](getmessagetrackingreport.md)
  
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **Scope-Element** aufgeführt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Organization (Organisation)  <br/> |Die Nachrichtenverfolgungsbereiche umfassen eine Organisation.  <br/> |
|Gesamtstruktur  <br/> |Die Nachrichtenverfolgungsbereiche umfassen eine Gesamtstruktur.  <br/> |
|Website  <br/> |Die Nachrichtenverfolgungsbereiche erstrecken sich über eine Website.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

