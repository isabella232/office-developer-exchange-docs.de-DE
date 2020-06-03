---
title: TokenType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: Das TokenType-Element gibt den Typ des Tokens an.
ms.openlocfilehash: a42849dce9ed0253c3c5d4d4e899367b8e105594
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459882"
---
# <a name="tokentype"></a><span data-ttu-id="384c3-103">TokenType</span><span class="sxs-lookup"><span data-stu-id="384c3-103">TokenType</span></span>

<span data-ttu-id="384c3-104">Das **TokenType** -Element gibt den Typ des Tokens an.</span><span class="sxs-lookup"><span data-stu-id="384c3-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="384c3-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="384c3-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="384c3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="384c3-106">Attributes and elements</span></span>

<span data-ttu-id="384c3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="384c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="384c3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="384c3-108">Attributes</span></span>

<span data-ttu-id="384c3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="384c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="384c3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="384c3-110">Child elements</span></span>

<span data-ttu-id="384c3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="384c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="384c3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="384c3-112">Parent elements</span></span>

<span data-ttu-id="384c3-113">[TokenRequest](tokenrequest.md)  |  [Token](token.md)</span><span class="sxs-lookup"><span data-stu-id="384c3-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="384c3-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="384c3-114">Text value</span></span>

<span data-ttu-id="384c3-115">Der Textwert des **TokenType** -Elements ist der Typ des Tokens.</span><span class="sxs-lookup"><span data-stu-id="384c3-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="384c3-116">Der Textwert von **CallerIdentity** gibt an, dass es sich bei dem Token um ein Anrufer-Identitätstoken handelt.</span><span class="sxs-lookup"><span data-stu-id="384c3-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="384c3-117">Der Textwert von **ExtensionCallback** gibt an, dass das Token für einen Durchwahl Rückruf gilt.</span><span class="sxs-lookup"><span data-stu-id="384c3-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="384c3-118">Der Textwert von **ScopedToken** gibt an, dass das Clientzugriffs Token ein Bereichs basiertes Token ist.</span><span class="sxs-lookup"><span data-stu-id="384c3-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="384c3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="384c3-119">Remarks</span></span>

<span data-ttu-id="384c3-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="384c3-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="384c3-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="384c3-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="384c3-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="384c3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="384c3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="384c3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="384c3-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="384c3-124">Schema name</span></span>  <br/> |<span data-ttu-id="384c3-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="384c3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="384c3-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="384c3-126">Validation file</span></span>  <br/> |<span data-ttu-id="384c3-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="384c3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="384c3-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="384c3-128">Can be empty</span></span>  <br/> |<span data-ttu-id="384c3-129">False</span><span class="sxs-lookup"><span data-stu-id="384c3-129">false</span></span>  <br/> |
   

