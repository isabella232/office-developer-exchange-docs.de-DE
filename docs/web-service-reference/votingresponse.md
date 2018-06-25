---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: Das VotingResponse-Element gibt gesendete stimmen. Dieses Element ist nur für Antworten auf Abstimmungsoptionen Anforderungsnachrichten, nicht für Antworten auf Genehmigungen vorhanden.
ms.openlocfilehash: 865b24a4f7ec1cc7b53d4928b04f071cddf5fbfc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839508"
---
# <a name="votingresponse"></a><span data-ttu-id="f8e81-104">VotingResponse</span><span class="sxs-lookup"><span data-stu-id="f8e81-104">VotingResponse</span></span>

<span data-ttu-id="f8e81-105">Das **VotingResponse** -Element gibt gesendete stimmen.</span><span class="sxs-lookup"><span data-stu-id="f8e81-105">The **VotingResponse** element specifies the submitted vote.</span></span> <span data-ttu-id="f8e81-106">Dieses Element ist nur für Antworten auf Abstimmungsoptionen Anforderungsnachrichten, nicht für Antworten auf Genehmigungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f8e81-106">This element is only present on responses to voting request messages, not on responses to approvals.</span></span> 
  
```XML
<VotingResponse />
```

 <span data-ttu-id="f8e81-107">**string**</span><span class="sxs-lookup"><span data-stu-id="f8e81-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8e81-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f8e81-108">Attributes and elements</span></span>

<span data-ttu-id="f8e81-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f8e81-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8e81-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f8e81-110">Attributes</span></span>

<span data-ttu-id="f8e81-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f8e81-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8e81-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8e81-112">Child elements</span></span>

<span data-ttu-id="f8e81-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f8e81-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f8e81-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f8e81-114">Parent elements</span></span>

[<span data-ttu-id="f8e81-115">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="f8e81-115">VotingInformation</span></span>](votinginformation.md)
  
## <a name="text-value"></a><span data-ttu-id="f8e81-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="f8e81-116">Text value</span></span>

<span data-ttu-id="f8e81-117">Der Textwert der **VotingResponse** -Element ist der Abstimmung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f8e81-117">The text value of the **VotingResponse** element is the vote submitted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8e81-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8e81-118">Remarks</span></span>

<span data-ttu-id="f8e81-119">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f8e81-119">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="f8e81-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f8e81-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8e81-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f8e81-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8e81-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8e81-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8e81-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f8e81-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f8e81-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f8e81-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8e81-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f8e81-125">Validation File</span></span>  <br/> |<span data-ttu-id="f8e81-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8e81-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8e81-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f8e81-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8e81-128">True</span><span class="sxs-lookup"><span data-stu-id="f8e81-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8e81-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8e81-129">See also</span></span>



[<span data-ttu-id="f8e81-130">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="f8e81-130">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="f8e81-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f8e81-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

