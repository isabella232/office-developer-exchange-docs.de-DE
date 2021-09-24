---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: Das PrimarySmtpAddress-Element stellt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Delegatenzugriff verwendet werden soll.
ms.openlocfilehash: 7963fbc92de88b38da93e577ebd2c39dbedac009
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523874"
---
# <a name="primarysmtpaddress"></a>PrimarySmtpAddress

Das **PrimarySmtpAddress-Element** stellt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Delegatenzugriff verwendet werden soll. 
  
```xml
<PrimarySmtpAddress/>
```

 **PrimarySmtpAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Stellt ein Konto dar, das bei Verwendung des ExchangeImpersonation-SOAP-Headers als Identitätswechsel verwendet werden soll.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreterbenutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Exchange Webdienste erfordern, dass Postfächer durch die primäre SMTP-Adresse des Postfachs identifiziert werden. Proxyadressen oder alternative Adressen werden nicht akzeptiert.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Server-zu-Server-Autorisierung in EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[Arbeiten mit Stellvertretungszugriff](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

