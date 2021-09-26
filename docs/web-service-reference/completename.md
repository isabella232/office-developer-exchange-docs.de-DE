---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: Das CompleteName-Element stellt den vollständigen Namen eines Kontakts dar.
ms.openlocfilehash: 873d372657089d21e86025cdf7812659ac505491
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543555"
---
# <a name="completename"></a>CompleteName

Das **CompleteName-Element** stellt den vollständigen Namen eines Kontakts dar. 
  
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
|[Title](title.md) <br/> |Stellt den Titel eines Kontakts dar.  <br/> |
|[FirstName](firstname.md) <br/> |Stellt den Vornamen des Kontakts dar.  <br/> |
|[MiddleName](middlename.md) <br/> |Stellt den Vornamen eines Kontakts dar.  <br/> |
|[LastName](lastname.md) <br/> |Stellt den Nachnamen eines Kontakts dar.  <br/> |
|[Suffix](suffix.md) <br/> |Stellt ein Suffix für den Namen eines Kontakts dar.  <br/> |
|[Initialen](initials.md) <br/> |Stellt die Initialen eines Kontakts dar.  <br/> |
|[FullName](fullname.md) <br/> |Stellt den vollständigen Namen eines Kontakts dar.  <br/> |
|[Spitzname](nickname.md) <br/> |Stellt den Spitznamen eines Kontakts dar.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Stellt den Namen dar, der in Japan für die durchsuchbare oder phonetische Schreibweise eines japanischen Vornamens verwendet wird.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Stellt den Namen dar, der in Japan für die durchsuchbare oder phonetische Schreibweise eines japanischen Nachnamens verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die CompleteName-Eigenschaft ist [](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) Teil des Standard-Shapes. In der ersten Version von Microsoft Exchange Server 2007 wird die CompleteName-Eigenschaft vom [GetItem-Vorgang](getitem-operation.md)zurückgegeben, aber nicht vom [FindItem-Vorgang.](finditem-operation.md) Ab Exchange Server 2007 Service Pack 1 (SP1) gibt der [FindItem-Vorgang](finditem-operation.md) auch die CompleteName-Eigenschaft mit dem [Standard-Shape](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) zurück. Diese Änderung wirkt sich nicht auf das Schema aus. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

