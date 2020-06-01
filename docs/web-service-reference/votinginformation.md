---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: Das VotingInformation-Element gibt Abstimmungsinformationen in einer Abstimmungs Nachricht und einer Genehmigungs Anforderungsnachricht whereApproveandRejectare den Abstimmungsoptionen an.
ms.openlocfilehash: d946ba8c71d19c8cbb1befbe8c4e43e93590ccae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467746"
---
# <a name="votinginformation"></a><span data-ttu-id="58aaa-103">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="58aaa-103">VotingInformation</span></span>

<span data-ttu-id="58aaa-104">Das **VotingInformation** -Element gibt Abstimmungsinformationen in einer Abstimmungs Nachricht und einer Genehmigungs Anforderungsnachricht an, wobei "genehmigen" und "ablehnen" die Abstimmungsoptionen sind.</span><span class="sxs-lookup"><span data-stu-id="58aaa-104">The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options.</span></span> 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 <span data-ttu-id="58aaa-105">**VotingInformationType**</span><span class="sxs-lookup"><span data-stu-id="58aaa-105">**VotingInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58aaa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="58aaa-106">Attributes and elements</span></span>

<span data-ttu-id="58aaa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="58aaa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58aaa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="58aaa-108">Attributes</span></span>

<span data-ttu-id="58aaa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="58aaa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58aaa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58aaa-110">Child elements</span></span>

<span data-ttu-id="58aaa-111">[USEROPTIONS](useroptions.md)  |  [VotingResponse](votingresponse.md)</span><span class="sxs-lookup"><span data-stu-id="58aaa-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58aaa-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="58aaa-112">Parent elements</span></span>

[<span data-ttu-id="58aaa-113">Nachricht</span><span class="sxs-lookup"><span data-stu-id="58aaa-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="58aaa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58aaa-114">Remarks</span></span>

<span data-ttu-id="58aaa-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="58aaa-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="58aaa-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="58aaa-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58aaa-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="58aaa-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58aaa-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="58aaa-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58aaa-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="58aaa-119">Schema Name</span></span>  <br/> |<span data-ttu-id="58aaa-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="58aaa-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="58aaa-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="58aaa-121">Validation File</span></span>  <br/> |<span data-ttu-id="58aaa-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58aaa-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58aaa-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="58aaa-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="58aaa-124">True</span><span class="sxs-lookup"><span data-stu-id="58aaa-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58aaa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58aaa-125">See also</span></span>



[<span data-ttu-id="58aaa-126">Nachricht</span><span class="sxs-lookup"><span data-stu-id="58aaa-126">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="58aaa-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="58aaa-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

