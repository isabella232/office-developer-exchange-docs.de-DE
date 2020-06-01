---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: Das VotingResponse-Element gibt die übermittelte Abstimmung an. Dieses Element ist nur bei Antworten auf Abstimmungs Anforderungsnachrichten vorhanden, nicht bei Antworten auf Genehmigungen.
ms.openlocfilehash: ed7caff79d1ff2946800630c167350fe866e29dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466465"
---
# <a name="votingresponse"></a><span data-ttu-id="1cecf-104">VotingResponse</span><span class="sxs-lookup"><span data-stu-id="1cecf-104">VotingResponse</span></span>

<span data-ttu-id="1cecf-105">Das **VotingResponse** -Element gibt die übermittelte Abstimmung an.</span><span class="sxs-lookup"><span data-stu-id="1cecf-105">The **VotingResponse** element specifies the submitted vote.</span></span> <span data-ttu-id="1cecf-106">Dieses Element ist nur bei Antworten auf Abstimmungs Anforderungsnachrichten vorhanden, nicht bei Antworten auf Genehmigungen.</span><span class="sxs-lookup"><span data-stu-id="1cecf-106">This element is only present on responses to voting request messages, not on responses to approvals.</span></span> 
  
```XML
<VotingResponse />
```

 <span data-ttu-id="1cecf-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1cecf-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1cecf-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1cecf-108">Attributes and elements</span></span>

<span data-ttu-id="1cecf-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1cecf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cecf-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="1cecf-110">Attributes</span></span>

<span data-ttu-id="1cecf-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1cecf-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1cecf-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1cecf-112">Child elements</span></span>

<span data-ttu-id="1cecf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1cecf-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1cecf-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1cecf-114">Parent elements</span></span>

[<span data-ttu-id="1cecf-115">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="1cecf-115">VotingInformation</span></span>](votinginformation.md)
  
## <a name="text-value"></a><span data-ttu-id="1cecf-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="1cecf-116">Text value</span></span>

<span data-ttu-id="1cecf-117">Der Textwert des **VotingResponse** -Elements ist die abgegebene Stimme.</span><span class="sxs-lookup"><span data-stu-id="1cecf-117">The text value of the **VotingResponse** element is the vote submitted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1cecf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cecf-118">Remarks</span></span>

<span data-ttu-id="1cecf-119">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1cecf-119">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="1cecf-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1cecf-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1cecf-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1cecf-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cecf-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cecf-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1cecf-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1cecf-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1cecf-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1cecf-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="1cecf-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1cecf-125">Validation File</span></span>  <br/> |<span data-ttu-id="1cecf-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1cecf-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1cecf-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1cecf-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1cecf-128">True</span><span class="sxs-lookup"><span data-stu-id="1cecf-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cecf-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cecf-129">See also</span></span>



[<span data-ttu-id="1cecf-130">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="1cecf-130">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="1cecf-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1cecf-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

