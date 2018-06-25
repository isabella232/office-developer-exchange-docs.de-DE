---
title: "\"TokenType\" (ClientAccessTokenType)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: Das Element "TokenType" identifiziert den Typ des Client-Zugriffstoken, die in der Antwort GetClientAccessToken zurückgegeben wird.
ms.openlocfilehash: c9adb60acf76fefebd58e2fd3bc899332a63dbee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839237"
---
# <a name="tokentype-clientaccesstokentype"></a>"TokenType" (ClientAccessTokenType)

Das Element **"TokenType"** identifiziert den Typ des Client-Zugriffstoken, die in der Antwort **GetClientAccessToken** zurückgegeben wird. 
  
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

[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>Textwert

Ein Textwert der **CallerIdentity** bedeutet, dass ein Anrufer Identität Client Zugriffstoken zurückgegeben wird. Der Textwert **ExtensionCallback** gibt an, dass ein Erweiterung Rückruf Client Zugriffstoken zurückgegeben wird. Der Textwert **ScopedToken** gibt an, dass das Zugriffstoken Client eine bereichsbasierte Token ist. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

