---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: Das VotingInformation-Element gibt die Abstimmungsoptionen voting Informationen für eine Nachricht Abstimmungsoptionen und Genehmigung Anforderung Nachricht WhereApproveandRejectare.
ms.openlocfilehash: f11c25bb1f3a3c4781cfa6c51e11ff87af40c7f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839502"
---
# <a name="votinginformation"></a><span data-ttu-id="9551d-103">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="9551d-103">VotingInformation</span></span>

<span data-ttu-id="9551d-104">Das **VotingInformation** -Element gibt voting Informationen für eine Nachricht Abstimmungsoptionen und Genehmigung Request-Nachricht, wobei "Genehmigen" und "Ablehnen" die Abstimmungsoptionen sind.</span><span class="sxs-lookup"><span data-stu-id="9551d-104">The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options.</span></span> 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 <span data-ttu-id="9551d-105">**VotingInformationType**</span><span class="sxs-lookup"><span data-stu-id="9551d-105">**VotingInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9551d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9551d-106">Attributes and elements</span></span>

<span data-ttu-id="9551d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9551d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9551d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9551d-108">Attributes</span></span>

<span data-ttu-id="9551d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9551d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9551d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9551d-110">Child elements</span></span>

<span data-ttu-id="9551d-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span><span class="sxs-lookup"><span data-stu-id="9551d-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9551d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9551d-112">Parent elements</span></span>

[<span data-ttu-id="9551d-113">Message</span><span class="sxs-lookup"><span data-stu-id="9551d-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="9551d-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9551d-114">Remarks</span></span>

<span data-ttu-id="9551d-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9551d-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9551d-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9551d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9551d-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9551d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9551d-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9551d-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9551d-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9551d-119">Schema Name</span></span>  <br/> |<span data-ttu-id="9551d-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9551d-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="9551d-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9551d-121">Validation File</span></span>  <br/> |<span data-ttu-id="9551d-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9551d-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9551d-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9551d-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="9551d-124">True</span><span class="sxs-lookup"><span data-stu-id="9551d-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9551d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9551d-125">See also</span></span>



[<span data-ttu-id="9551d-126">Message</span><span class="sxs-lookup"><span data-stu-id="9551d-126">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="9551d-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9551d-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

