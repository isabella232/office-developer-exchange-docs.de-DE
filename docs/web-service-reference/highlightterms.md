---
title: HighlightTerms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce4a2978-fd0c-41a4-ae65-aa6f5dc9a0f9
description: Das HighlightTerms-Element identifiziert die hervorgehobenen Begriffe, die in einem Vorgang FindItem und einer Antwort auf einen Vorgang FindConversation zurückgegeben.
ms.openlocfilehash: c075e63674bc08773925a2a540a1c2434423926d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829808"
---
# <a name="highlightterms"></a><span data-ttu-id="52953-103">HighlightTerms</span><span class="sxs-lookup"><span data-stu-id="52953-103">HighlightTerms</span></span>

<span data-ttu-id="52953-104">Das **HighlightTerms** -Element identifiziert die hervorgehobenen Begriffe, die in einem Vorgang **FindItem** und einer Antwort auf einen Vorgang **FindConversation** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="52953-104">The **HighlightTerms** element identifies the highlighted terms returned in a **FindItem** operation and a **FindConversation** operation response.</span></span> 
  
```XML
<HighlightTerms>
   <Term/>
</HighlightTerms>
```

 <span data-ttu-id="52953-105">**ArrayOfHighlightTermsType**</span><span class="sxs-lookup"><span data-stu-id="52953-105">**ArrayOfHighlightTermsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52953-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="52953-106">Attributes and elements</span></span>

<span data-ttu-id="52953-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="52953-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52953-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="52953-108">Attributes</span></span>

<span data-ttu-id="52953-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="52953-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52953-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52953-110">Child elements</span></span>

<span data-ttu-id="52953-111">Begriff</span><span class="sxs-lookup"><span data-stu-id="52953-111">Term</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52953-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="52953-112">Parent elements</span></span>

<span data-ttu-id="52953-113">[FindConversationResponse](findconversationresponse.md) | [FindItemResponseMessage](finditemresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="52953-113">[FindConversationResponse](findconversationresponse.md) | [FindItemResponseMessage](finditemresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52953-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52953-114">Remarks</span></span>

<span data-ttu-id="52953-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="52953-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="52953-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="52953-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52953-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="52953-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52953-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="52953-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52953-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="52953-119">Schema name</span></span>  <br/> |<span data-ttu-id="52953-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="52953-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52953-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="52953-121">Validation file</span></span>  <br/> |<span data-ttu-id="52953-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52953-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52953-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="52953-123">Can be empty</span></span>  <br/> ||
   

