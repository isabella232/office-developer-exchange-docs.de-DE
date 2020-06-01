---
title: Eingabe (Faxnummer)
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
description: Das Entry-Element stellt eine Telefonnummer für einen Kontakt dar.
ms.openlocfilehash: 62f7091bb750dc7ca74b1e5637a437e2cdad4f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459637"
---
# <a name="entry-phonenumber"></a>Eingabe (Faxnummer)

Das **Entry** -Element stellt eine Telefonnummer für einen Kontakt dar. 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Gibt die Telefonnummer an. Das Key-Attribut ist vom Typ **PhoneNumberKeyType**.<br/><br/> Es folgen die möglichen Werte für dieses Attribut.<br/><br/>- AssistantPhone  <br/>- BusinessFax  <br/>-Businessphone  <br/>- BusinessPhone2  <br/>-Callback  <br/>-CarPhone  <br/>- CompanyMainPhone  <br/>- HomeFax  <br/>-HomePhone  <br/>- HomePhone2  <br/>-ISDN  <br/>-MobilePhone  <br/>-OtherFax  <br/>-OtherTelephone  <br/>-Pager  <br/>- PrimaryPhone  <br/>-RadioPhone  <br/>-Telex  <br/>- TtyTddPhone  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine Telefonnummer darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

