---
title: Token (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cddd6075-06b6-4858-9ffa-9db4d9d9b030
description: Das Token-Element gibt ein Zugriffstoken für den Client an.
ms.openlocfilehash: 2e1f401141aef07a57a214968f6a6bafdf71f0dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839227"
---
# <a name="token-clientaccesstokentype"></a><span data-ttu-id="99dc2-103">Token (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="99dc2-103">Token (ClientAccessTokenType)</span></span>

<span data-ttu-id="99dc2-104">Das **Token** -Element gibt ein Zugriffstoken für den Client an.</span><span class="sxs-lookup"><span data-stu-id="99dc2-104">The **Token** element specifies a client access token.</span></span> 
  
```XML
<Token>
   <Id/>
   <TokenType/>
   <TokenValue/>
   <TTL/>
</Token>
```

 <span data-ttu-id="99dc2-105">**ClientAccessTokenType**</span><span class="sxs-lookup"><span data-stu-id="99dc2-105">**ClientAccessTokenType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99dc2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99dc2-106">Attributes and elements</span></span>

<span data-ttu-id="99dc2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99dc2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99dc2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="99dc2-108">Attributes</span></span>

<span data-ttu-id="99dc2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="99dc2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99dc2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99dc2-110">Child elements</span></span>

<span data-ttu-id="99dc2-111">[ID (Zeichenfolge)](id-string.md) | ["TokenType"](tokentype.md) | [TokenValue](tokenvalue.md) | [TTL](ttl.md)</span><span class="sxs-lookup"><span data-stu-id="99dc2-111">[ID (String)](id-string.md) | [TokenType](tokentype.md) | [TokenValue](tokenvalue.md) | [TTL](ttl.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="99dc2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99dc2-112">Parent elements</span></span>

[<span data-ttu-id="99dc2-113">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99dc2-113">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="99dc2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99dc2-114">Remarks</span></span>

<span data-ttu-id="99dc2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99dc2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="99dc2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="99dc2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99dc2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="99dc2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99dc2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="99dc2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99dc2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99dc2-119">Schema name</span></span>  <br/> |<span data-ttu-id="99dc2-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="99dc2-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="99dc2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99dc2-121">Validation file</span></span>  <br/> |<span data-ttu-id="99dc2-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99dc2-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99dc2-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="99dc2-123">Can be empty</span></span>  <br/> ||
   

