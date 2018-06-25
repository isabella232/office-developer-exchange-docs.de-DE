---
title: "\"TokenType\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: Das Element "TokenType" gibt den Typ des Tokens.
ms.openlocfilehash: 5c8e880f035ed74776a7c77e4b4e60ca46d66d4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839231"
---
# <a name="tokentype"></a><span data-ttu-id="cc901-103">"TokenType"</span><span class="sxs-lookup"><span data-stu-id="cc901-103">TokenType</span></span>

<span data-ttu-id="cc901-104">Das Element **"TokenType"** gibt den Typ des Tokens.</span><span class="sxs-lookup"><span data-stu-id="cc901-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="cc901-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="cc901-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc901-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cc901-106">Attributes and elements</span></span>

<span data-ttu-id="cc901-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cc901-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc901-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cc901-108">Attributes</span></span>

<span data-ttu-id="cc901-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc901-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc901-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc901-110">Child elements</span></span>

<span data-ttu-id="cc901-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cc901-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc901-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cc901-112">Parent elements</span></span>

<span data-ttu-id="cc901-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span><span class="sxs-lookup"><span data-stu-id="cc901-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cc901-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="cc901-114">Text value</span></span>

<span data-ttu-id="cc901-115">Der Textwert des Elements **"TokenType"** ist das token.</span><span class="sxs-lookup"><span data-stu-id="cc901-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="cc901-116">Der Textwert der **CallerIdentity** gibt an, dass das Token ein Identitätstoken Anrufer ist.</span><span class="sxs-lookup"><span data-stu-id="cc901-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="cc901-117">Der Textwert der **ExtensionCallback** gibt an, dass das Token für eine Erweiterung Rückruf ist.</span><span class="sxs-lookup"><span data-stu-id="cc901-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="cc901-118">Der Textwert der **ScopedToken** gibt an, dass das Zugriffstoken Client eine bereichsbasierte Token ist.</span><span class="sxs-lookup"><span data-stu-id="cc901-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc901-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc901-119">Remarks</span></span>

<span data-ttu-id="cc901-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cc901-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cc901-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cc901-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc901-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cc901-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc901-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc901-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc901-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cc901-124">Schema name</span></span>  <br/> |<span data-ttu-id="cc901-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cc901-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc901-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cc901-126">Validation file</span></span>  <br/> |<span data-ttu-id="cc901-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cc901-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc901-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cc901-128">Can be empty</span></span>  <br/> |<span data-ttu-id="cc901-129">false</span><span class="sxs-lookup"><span data-stu-id="cc901-129">false</span></span>  <br/> |
   

