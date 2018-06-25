---
title: Eintrag ("PhoneNumber")
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: Entry-Element stellt eine Telefonnummer für einen Kontakt.
ms.openlocfilehash: 3953488fb0b57fcf01c2fb99039478bbe03c7f5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758259"
---
# <a name="entry-phonenumber"></a>Eintrag ("PhoneNumber")

**Entry** -Element stellt eine Telefonnummer für einen Kontakt. 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Gibt die Telefonnummer ein. Das Key-Attribut ist vom Typ **PhoneNumberKeyType**.<br/><br/> Es folgen die möglichen Werte für dieses Attribut.<br/><br/>-Telefon (Sekretariat)  <br/>-Geschäftlich Fax  <br/>-BusinessPhone  <br/>-BusinessPhone2  <br/>-Rückruf  <br/>-CarPhone  <br/>-CompanyMainPhone  <br/>-Fax (privat)  <br/>-HomePhone  <br/>-HomePhone2  <br/>-Isdn  <br/>-Kontaktdetails  <br/>-OtherFax  <br/>-OtherTelephone  <br/>-Pager  <br/>-PrimaryPhone  <br/>-RadioPhone  <br/>-Telex  <br/>-TtyTddPhone  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine Telefonnummer darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [Aktualisierung von Kontakten](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

