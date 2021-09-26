---
title: Token (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cddd6075-06b6-4858-9ffa-9db4d9d9b030
description: Das Token-Element gibt ein Clientzugriffstoken an.
ms.openlocfilehash: b9cd0887d082c2ddd9abe0505ebec993f0261fad
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545734"
---
# <a name="token-clientaccesstokentype"></a>Token (ClientAccessTokenType)

Das **Token-Element** gibt ein Clientzugriffstoken an. 
  
```XML
<Token>
   <Id/>
   <TokenType/>
   <TokenValue/>
   <TTL/>
</Token>
```

 **ClientAccessTokenType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ID (Zeichenfolge)](id-string.md)  |  [TokenType](tokentype.md)  |  [TokenValue](tokenvalue.md)  |  [TTL](ttl.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetClientAccessTokenResponseMessage](getclientaccesstokenresponsemessage.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

