---
title: TokenType (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: Das TokenType-Element gibt den Typ des Clientzugriffs Tokens an, der in der GetClientAccessToken-Antwort zurückgegeben wird.
ms.openlocfilehash: 49ba2973967b12396e0c7f56129c89c40ccbcf97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466052"
---
# <a name="tokentype-clientaccesstokentype"></a><span data-ttu-id="dfbb5-103">TokenType (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="dfbb5-103">TokenType (ClientAccessTokenType)</span></span>

<span data-ttu-id="dfbb5-104">Das **TokenType** -Element gibt den Typ des Clientzugriffs Tokens an, der in der **GetClientAccessToken** -Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-104">The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response.</span></span> 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 <span data-ttu-id="dfbb5-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="dfbb5-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dfbb5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dfbb5-106">Attributes and elements</span></span>

<span data-ttu-id="dfbb5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfbb5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dfbb5-108">Attributes</span></span>

<span data-ttu-id="dfbb5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfbb5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfbb5-110">Child elements</span></span>

<span data-ttu-id="dfbb5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dfbb5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dfbb5-112">Parent elements</span></span>

<span data-ttu-id="dfbb5-113">[TokenRequest](tokenrequest.md)  |  [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span><span class="sxs-lookup"><span data-stu-id="dfbb5-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="dfbb5-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="dfbb5-114">Text value</span></span>

<span data-ttu-id="dfbb5-115">Der Textwert **CallerIdentity** bedeutet, dass ein Clientzugriffs Token für die Anrufer-ID zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-115">A text value of **CallerIdentity** means a caller identity client access token is returned.</span></span> <span data-ttu-id="dfbb5-116">Der Textwert **ExtensionCallback** gibt an, dass ein Clientzugriffs Token für Durchwahl Rückrufe zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-116">A text value of **ExtensionCallback** indicates that an extension callback client access token is returned.</span></span> <span data-ttu-id="dfbb5-117">Der Textwert **ScopedToken** gibt an, dass das Clientzugriffs Token ein Bereichs basiertes Token ist.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-117">A text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dfbb5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfbb5-118">Remarks</span></span>

<span data-ttu-id="dfbb5-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dfbb5-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dfbb5-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfbb5-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dfbb5-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfbb5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="dfbb5-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dfbb5-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dfbb5-123">Schema name</span></span>  <br/> |<span data-ttu-id="dfbb5-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dfbb5-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="dfbb5-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dfbb5-125">Validation file</span></span>  <br/> |<span data-ttu-id="dfbb5-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dfbb5-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dfbb5-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dfbb5-127">Can be empty</span></span>  <br/> |<span data-ttu-id="dfbb5-128">False</span><span class="sxs-lookup"><span data-stu-id="dfbb5-128">false</span></span>  <br/> |
   

