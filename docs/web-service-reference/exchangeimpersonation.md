---
title: "\"ExchangeImpersonation\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: Das Element "ExchangeImpersonation" wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der "ExchangeImpersonation"-Element enthalten ist.
ms.openlocfilehash: aedeff22cda865ce1eec80dab9760d49fdc178f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758299"
---
# <a name="exchangeimpersonation"></a>"ExchangeImpersonation"

Das Element **"ExchangeImpersonation"** wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der **"ExchangeImpersonation"** -Element enthalten ist. 
  
["ExchangeImpersonation"](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 **ExchangeImpersonationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das aufrufende Konto muss die **ms-Exch-Impersonation** direkt auf dem Clientzugriffsserver und das **ms-Exch-MayImpersonate** Recht auf entweder haben die Postfachdatenbank, die das Postfach Identität enthält oder den Active Directory-Benutzer/Kontakt -Objekt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Server-zu-Server-Autorisierung in Exchange-Webdienste](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

