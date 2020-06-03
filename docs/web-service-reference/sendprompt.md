---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: Das SendPrompt-Element gibt den Typ der Aktion an, die für eine Abstimmungsoption zulässig ist.
ms.openlocfilehash: 98ffc69cdc94c3f7b9c325bee0c1ebaeb407ee96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462101"
---
# <a name="sendprompt"></a><span data-ttu-id="dc91a-103">SendPrompt</span><span class="sxs-lookup"><span data-stu-id="dc91a-103">SendPrompt</span></span>

<span data-ttu-id="dc91a-104">Das **SendPrompt** -Element gibt den Typ der Aktion an, die für eine Abstimmungsoption zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="dc91a-104">The **SendPrompt** element specifies the type of action allowed for a voting option.</span></span> 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 <span data-ttu-id="dc91a-105">**SendPromptType**</span><span class="sxs-lookup"><span data-stu-id="dc91a-105">**SendPromptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc91a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc91a-106">Attributes and elements</span></span>

<span data-ttu-id="dc91a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc91a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc91a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc91a-108">Attributes</span></span>

<span data-ttu-id="dc91a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc91a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc91a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc91a-110">Child elements</span></span>

<span data-ttu-id="dc91a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc91a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc91a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc91a-112">Parent elements</span></span>

[<span data-ttu-id="dc91a-113">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="dc91a-113">VotingOptionData</span></span>](votingoptiondata.md)
  
## <a name="text-value"></a><span data-ttu-id="dc91a-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="dc91a-114">Text value</span></span>

<span data-ttu-id="dc91a-115">Der Textwert des **SendPrompt** -Elements ist eine Abstimmungs Options Aktion.</span><span class="sxs-lookup"><span data-stu-id="dc91a-115">The text value of the **SendPrompt** element is a voting option action.</span></span> <span data-ttu-id="dc91a-116">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc91a-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="dc91a-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dc91a-117">**Value**</span></span>|<span data-ttu-id="dc91a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc91a-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc91a-119">Keine</span><span class="sxs-lookup"><span data-stu-id="dc91a-119">None</span></span>  <br/> |<span data-ttu-id="dc91a-120">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="dc91a-120">No action.</span></span>  <br/> |
|<span data-ttu-id="dc91a-121">Senden</span><span class="sxs-lookup"><span data-stu-id="dc91a-121">Send</span></span>  <br/> |<span data-ttu-id="dc91a-122">Die Antwort wird sofort gesendet.</span><span class="sxs-lookup"><span data-stu-id="dc91a-122">The response is sent immediately.</span></span>  <br/> |
|<span data-ttu-id="dc91a-123">VotingOption</span><span class="sxs-lookup"><span data-stu-id="dc91a-123">VotingOption</span></span>  <br/> |<span data-ttu-id="dc91a-124">Die genehmigende Person kann Kommentare beim genehmigen oder ablehnen eingeben.</span><span class="sxs-lookup"><span data-stu-id="dc91a-124">The approver can enter comments while approving or rejecting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc91a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc91a-125">Remarks</span></span>

<span data-ttu-id="dc91a-126">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dc91a-126">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="dc91a-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dc91a-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc91a-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dc91a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc91a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc91a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc91a-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc91a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="dc91a-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dc91a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc91a-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc91a-132">Validation File</span></span>  <br/> |<span data-ttu-id="dc91a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc91a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc91a-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dc91a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc91a-135">True</span><span class="sxs-lookup"><span data-stu-id="dc91a-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc91a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc91a-136">See also</span></span>



[<span data-ttu-id="dc91a-137">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="dc91a-137">VotingOptionData</span></span>](votingoptiondata.md)


- [<span data-ttu-id="dc91a-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc91a-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

