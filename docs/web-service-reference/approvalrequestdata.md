---
title: ApprovalRequestData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6c971cf7-5c3a-4e5e-9a7d-048f4ac0aadb
description: Das ApprovalRequestData-Element gibt den Genehmigungsstatus einer Genehmigungs Anforderungsnachricht an.
ms.openlocfilehash: decbd4d646a56b9810387adcdb6a9049da89bc38
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462304"
---
# <a name="approvalrequestdata"></a><span data-ttu-id="f2175-103">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="f2175-103">ApprovalRequestData</span></span>

<span data-ttu-id="f2175-104">Das **ApprovalRequestData** -Element gibt den Genehmigungsstatus einer Genehmigungs Anforderungsnachricht an.</span><span class="sxs-lookup"><span data-stu-id="f2175-104">The **ApprovalRequestData** element specifies the approval state of an approval request message.</span></span> 
  
```xml
<ApprovalRequestData>
   <IsUndecidedApprovalRequest/>
   <ApprovalDecision/>
   <ApprovalDecisionMaker/>
   <ApprovalDecisionTime/>
</ApprovalRequestData>
```

 <span data-ttu-id="f2175-105">**ApprovalRequestDataType**</span><span class="sxs-lookup"><span data-stu-id="f2175-105">**ApprovalRequestDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2175-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2175-106">Attributes and elements</span></span>

<span data-ttu-id="f2175-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2175-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2175-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2175-108">Attributes</span></span>

<span data-ttu-id="f2175-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2175-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2175-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2175-110">Child elements</span></span>

<span data-ttu-id="f2175-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md)  |  [ApprovalDecision](approvaldecision.md)  |  [ApprovalDecisionMaker](approvaldecisionmaker.md)  |  [ApprovalDecisionTime](approvaldecisiontime.md)</span><span class="sxs-lookup"><span data-stu-id="f2175-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2175-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2175-112">Parent elements</span></span>

[<span data-ttu-id="f2175-113">Meldung</span><span class="sxs-lookup"><span data-stu-id="f2175-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="f2175-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2175-114">Remarks</span></span>

<span data-ttu-id="f2175-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2175-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="f2175-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f2175-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2175-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f2175-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2175-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2175-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2175-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2175-119">Schema Name</span></span>  <br/> |<span data-ttu-id="f2175-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f2175-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2175-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2175-121">Validation File</span></span>  <br/> |<span data-ttu-id="f2175-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2175-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2175-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f2175-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2175-124">True</span><span class="sxs-lookup"><span data-stu-id="f2175-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2175-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2175-125">See also</span></span>

- [<span data-ttu-id="f2175-126">Meldung</span><span class="sxs-lookup"><span data-stu-id="f2175-126">Message</span></span>](message-ex15websvcsotherref.md)
- [<span data-ttu-id="f2175-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2175-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

