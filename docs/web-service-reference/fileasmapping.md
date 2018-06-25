---
title: FileAsMapping
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAsMapping
api_type:
- schema
ms.assetid: 2c98e7c6-09b0-47b3-bbf7-8c4ef9510280
description: Das FileAsMapping-Element definiert, wie erstellen, was für einen Kontakt angezeigt wird.
ms.openlocfilehash: 1ba0ae0daa56a72c29d8c0ccad64e3edae5f0b84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758428"
---
# <a name="fileasmapping"></a>FileAsMapping

Das **FileAsMapping** -Element definiert, wie erstellen, was für einen Kontakt angezeigt wird. 
  
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

Der Textwert für dieses Element ist auf die folgenden Werte vom Typ String beschränkt:
  
- Keine
    
- LastCommaFirst
    
- FirstSpaceLast
    
- Unternehmen
    
- LastCommaFirstCompany
    
- CompanyLastFirst
    
- Nachn.vorn.
    
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
    
- Leer
    
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Aktualisierung von Kontakten](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Deleting Contacts](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

