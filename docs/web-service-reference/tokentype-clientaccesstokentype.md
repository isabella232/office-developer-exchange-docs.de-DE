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
# <a name="tokentype-clientaccesstokentype"></a><span data-ttu-id="68c86-103">"TokenType" (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="68c86-103">TokenType (ClientAccessTokenType)</span></span>

<span data-ttu-id="68c86-104">Das Element **"TokenType"** identifiziert den Typ des Client-Zugriffstoken, die in der Antwort **GetClientAccessToken** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68c86-104">The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response.</span></span> 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 <span data-ttu-id="68c86-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="68c86-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68c86-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68c86-106">Attributes and elements</span></span>

<span data-ttu-id="68c86-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68c86-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68c86-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="68c86-108">Attributes</span></span>

<span data-ttu-id="68c86-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="68c86-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68c86-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68c86-110">Child elements</span></span>

<span data-ttu-id="68c86-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="68c86-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68c86-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68c86-112">Parent elements</span></span>

<span data-ttu-id="68c86-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span><span class="sxs-lookup"><span data-stu-id="68c86-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="68c86-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="68c86-114">Text value</span></span>

<span data-ttu-id="68c86-115">Ein Textwert der **CallerIdentity** bedeutet, dass ein Anrufer Identität Client Zugriffstoken zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68c86-115">A text value of **CallerIdentity** means a caller identity client access token is returned.</span></span> <span data-ttu-id="68c86-116">Der Textwert **ExtensionCallback** gibt an, dass ein Erweiterung Rückruf Client Zugriffstoken zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="68c86-116">A text value of **ExtensionCallback** indicates that an extension callback client access token is returned.</span></span> <span data-ttu-id="68c86-117">Der Textwert **ScopedToken** gibt an, dass das Zugriffstoken Client eine bereichsbasierte Token ist.</span><span class="sxs-lookup"><span data-stu-id="68c86-117">A text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="68c86-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68c86-118">Remarks</span></span>

<span data-ttu-id="68c86-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="68c86-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="68c86-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="68c86-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68c86-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68c86-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68c86-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="68c86-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68c86-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68c86-123">Schema name</span></span>  <br/> |<span data-ttu-id="68c86-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="68c86-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="68c86-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68c86-125">Validation file</span></span>  <br/> |<span data-ttu-id="68c86-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68c86-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68c86-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="68c86-127">Can be empty</span></span>  <br/> |<span data-ttu-id="68c86-128">false</span><span class="sxs-lookup"><span data-stu-id="68c86-128">false</span></span>  <br/> |
   

