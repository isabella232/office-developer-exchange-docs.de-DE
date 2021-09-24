---
title: FileAsMapping
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FileAsMapping
api_type:
- schema
ms.assetid: 2c98e7c6-09b0-47b3-bbf7-8c4ef9510280
description: Das FileAsMapping-Element definiert, wie erstellt wird, was für einen Kontakt angezeigt wird.
ms.openlocfilehash: 35397ebd5cb9235ad55093b43bde89eef466e672
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518505"
---
# <a name="fileasmapping"></a>FileAsMapping

Das **FileAsMapping-Element** definiert, wie erstellt wird, was für einen Kontakt angezeigt wird. 
  
```xml
<FileAsMapping/>
```

 **FileAsMappingType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist auf einen der folgenden Zeichenfolgenwerte beschränkt:
  
- Keines
    
- LastCommaFirst
    
- FirstSpaceLast
    
- Company
    
- LastCommaFirstCompany
    
- CompanyLastFirst
    
- LastFirst
    
- LastFirstCompany
    
- CompanyLastCommaFirst
    
- LastFirstSuffix
    
- LastSpaceFirstCompany
    
- CompanyLastSpaceFirst
    
- LastSpaceFirst
    
- DisplayName
    
- FirstName
    
- LastFirstMiddleSuffix
    
- LastName
    
- Empty
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

