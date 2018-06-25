---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: Das SendPrompt-Element gibt den Typ der Aktion für ein voting Option zulässig.
ms.openlocfilehash: f3220d957482ea04c46b014cdf1c67025d5ec21a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831346"
---
# <a name="sendprompt"></a><span data-ttu-id="ce49c-103">SendPrompt</span><span class="sxs-lookup"><span data-stu-id="ce49c-103">SendPrompt</span></span>

<span data-ttu-id="ce49c-104">Das **SendPrompt** -Element gibt den Typ der Aktion für ein voting Option zulässig.</span><span class="sxs-lookup"><span data-stu-id="ce49c-104">The **SendPrompt** element specifies the type of action allowed for a voting option.</span></span> 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 <span data-ttu-id="ce49c-105">**SendPromptType**</span><span class="sxs-lookup"><span data-stu-id="ce49c-105">**SendPromptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce49c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ce49c-106">Attributes and elements</span></span>

<span data-ttu-id="ce49c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ce49c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce49c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce49c-108">Attributes</span></span>

<span data-ttu-id="ce49c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce49c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce49c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce49c-110">Child elements</span></span>

<span data-ttu-id="ce49c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce49c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce49c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce49c-112">Parent elements</span></span>

[<span data-ttu-id="ce49c-113">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="ce49c-113">VotingOptionData</span></span>](votingoptiondata.md)
  
## <a name="text-value"></a><span data-ttu-id="ce49c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="ce49c-114">Text value</span></span>

<span data-ttu-id="ce49c-115">Der Textwert des **SendPrompt** -Elements ist eine voting Option Aktion.</span><span class="sxs-lookup"><span data-stu-id="ce49c-115">The text value of the **SendPrompt** element is a voting option action.</span></span> <span data-ttu-id="ce49c-116">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="ce49c-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="ce49c-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ce49c-117">**Value**</span></span>|<span data-ttu-id="ce49c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce49c-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce49c-119">Keine</span><span class="sxs-lookup"><span data-stu-id="ce49c-119">None</span></span>  <br/> |<span data-ttu-id="ce49c-120">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="ce49c-120">No action.</span></span>  <br/> |
|<span data-ttu-id="ce49c-121">Senden</span><span class="sxs-lookup"><span data-stu-id="ce49c-121">Send</span></span>  <br/> |<span data-ttu-id="ce49c-122">Die Antwort wird sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce49c-122">The response is sent immediately.</span></span>  <br/> |
|<span data-ttu-id="ce49c-123">VotingOption</span><span class="sxs-lookup"><span data-stu-id="ce49c-123">VotingOption</span></span>  <br/> |<span data-ttu-id="ce49c-124">Die genehmigende Person kann Eincheckkommentare beim Genehmigen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="ce49c-124">The approver can enter comments while approving or rejecting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce49c-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce49c-125">Remarks</span></span>

<span data-ttu-id="ce49c-126">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ce49c-126">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="ce49c-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ce49c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce49c-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ce49c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce49c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce49c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce49c-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ce49c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ce49c-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ce49c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce49c-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ce49c-132">Validation File</span></span>  <br/> |<span data-ttu-id="ce49c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce49c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce49c-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ce49c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce49c-135">True</span><span class="sxs-lookup"><span data-stu-id="ce49c-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce49c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce49c-136">See also</span></span>



[<span data-ttu-id="ce49c-137">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="ce49c-137">VotingOptionData</span></span>](votingoptiondata.md)


- [<span data-ttu-id="ce49c-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ce49c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

