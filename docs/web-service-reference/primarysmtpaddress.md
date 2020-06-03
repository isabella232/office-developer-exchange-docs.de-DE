---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: Das PrimarySmtpAddress-Element stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Stellvertretungszugriff verwendet werden soll.
ms.openlocfilehash: eea995b3e546d7e94e65cf9b230b639a781c4928
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467963"
---
# <a name="primarysmtpaddress"></a>PrimarySmtpAddress

Das **PrimarySmtpAddress** -Element stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung oder den Stellvertretungszugriff verwendet werden soll. 
  
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
|[ConnectingSID](connectingsid.md) <br/> |Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[SerializedSecurityContext](serializedsecuritycontext.md) <br/> |Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>Bemerkungen

Exchange Webdienste erfordert, dass Postfächer von der primären SMTP-Adresse des Postfachs identifiziert werden. Proxy-oder alternative Adressen werden nicht akzeptiert.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
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

