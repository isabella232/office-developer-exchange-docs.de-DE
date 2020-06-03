---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: Das GetPasswordExpirationDate-Element definiert eine Anforderung zum Abrufen des Kennwortablauf Datums für ein e-Mail-Konto. Dieses Element ist das Basiselement für den GetPasswordExpirationDate-Vorgangs Vorgang.
ms.openlocfilehash: ececbf51f71c7d87705d727229fce2314d922efb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456493"
---
# <a name="getpasswordexpirationdate"></a>GetPasswordExpirationDate

Das **GetPasswordExpirationDate** -Element definiert eine Anforderung zum Abrufen des Kennwortablauf Datums für ein e-Mail-Konto. Dieses Element ist das Basiselement für den [GetPasswordExpirationDate-Vorgangs](getpasswordexpirationdate-operation.md) Vorgang. 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 **GetPasswordExpirationDateType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Stellt die e-Mail-Adresse des e-Mail-Kontos dar, für das das Ablaufdatum des Kennworts zurückgegeben werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

