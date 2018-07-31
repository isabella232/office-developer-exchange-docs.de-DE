---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: Das Element CompleteName stellt den vollständigen Namen eines Kontakts.
ms.openlocfilehash: bca6f7e0eb915841673d00b5485da2f0f9794e80
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354260"
---
# <a name="completename"></a>CompleteName

Das Element **CompleteName** stellt den vollständigen Namen eines Kontakts. 
  
```xml
<CompleteName>
   <Title/>
   <FirstName/>
   <MiddleName/>
   <LastName/>
   <Suffix/>
   <Initials/>
   <FullName/>
   <Nickname/>
   <YomiFirstName/>
   <YomiLastName/>
</CompleteName>
```

 **CompleteNameType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Title](title.md) <br/> |Stellt den Titel eines Kontakts an.  <br/> |
|[FirstName](firstname.md) <br/> |Stellt den Vornamen des Kontakts an.  <br/> |
|[MiddleName](middlename.md) <br/> |Stellt den Vornamen eines Kontakts an.  <br/> |
|[LastName](lastname.md) <br/> |Stellt den Nachnamen eines Kontakts an.  <br/> |
|[Suffix](suffix.md) <br/> |Stellt ein Suffix für den Namen eines Kontakts dar.  <br/> |
|[Initialen](initials.md) <br/> |Stellt die Initialen eines Kontakts an.  <br/> |
|[FullName](fullname.md) <br/> |Stellt den vollständigen Namen eines Kontakts an.  <br/> |
|[Spitzname](nickname.md) <br/> |Stellt den Spitznamen eines Kontakts an.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Stellt den Namen für die durchsuchbaren oder die phonetische Schreibweise des japanischen Vorname in Japan verwendet.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Stellt den Namen für die durchsuchbar oder phonetische Schreibweise eines japanischen Nachnamens in Japan verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die CompleteName-Eigenschaft ist Teil des [Standard](https://docs.microsoft.com/en-us/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) -Shapes. In der ursprünglich freigegebenen Version von Microsoft Exchange Server 2007 wird die CompleteName-Eigenschaft durch den [GetItem Operation](getitem-operation.md), aber nicht die [FindItem Vorgang](finditem-operation.md)zurückgegeben. Beginnend mit Exchange Server 2007 Service Pack 1 (SP1), gibt die [FindItem Vorgang](finditem-operation.md) auch die CompleteName-Eigenschaft mit dem [Standard](https://docs.microsoft.com/en-us/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) -Shape zurück. Diese Änderung wirkt sich nicht auf das Schema aus. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

