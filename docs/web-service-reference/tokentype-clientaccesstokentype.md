---
title: TokenType (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: Das TokenType-Element identifiziert den Typ des Clientzugriffstokens, das in der GetClientAccessToken-Antwort zurückgegeben wird.
ms.openlocfilehash: 967d64796799147876ef6443b40b16154b55c01a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523356"
---
# <a name="tokentype-clientaccesstokentype"></a>TokenType (ClientAccessTokenType)

Das **TokenType-Element** identifiziert den Typ des Clientzugriffstokens, das in der **GetClientAccessToken-Antwort** zurückgegeben wird. 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[TokenRequest](tokenrequest.md)  |  [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>Textwert

Ein Textwert von **CallerIdentity** bedeutet, dass ein Clientzugriffstoken für die Anruferidentität zurückgegeben wird. Ein Textwert von **ExtensionCallback** gibt an, dass ein Clientzugriffstoken für den Erweiterungsrückruf zurückgegeben wird. Ein Textwert von **ScopedToken** gibt an, dass das Clientzugriffstoken ein bereichsbezogenes Token ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

