---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: Das ApprovalDecision-Element gibt die Entscheidung an, die in einer Genehmigungs Anforderungsnachricht getroffen wurde.
ms.openlocfilehash: a8dc168edec882ba97cdea764f8d20c71ed85f8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463447"
---
# <a name="approvaldecision"></a><span data-ttu-id="eb1a7-103">ApprovalDecision</span><span class="sxs-lookup"><span data-stu-id="eb1a7-103">ApprovalDecision</span></span>

<span data-ttu-id="eb1a7-104">Das **ApprovalDecision** -Element gibt die Entscheidung an, die in einer Genehmigungs Anforderungsnachricht getroffen wurde.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-104">The **ApprovalDecision** element specifies the decision made on an approval request message.</span></span> 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 <span data-ttu-id="eb1a7-105">**int**</span><span class="sxs-lookup"><span data-stu-id="eb1a7-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb1a7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eb1a7-106">Attributes and elements</span></span>

<span data-ttu-id="eb1a7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb1a7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eb1a7-108">Attributes</span></span>

<span data-ttu-id="eb1a7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb1a7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb1a7-110">Child elements</span></span>

<span data-ttu-id="eb1a7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb1a7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb1a7-112">Parent elements</span></span>

[<span data-ttu-id="eb1a7-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="eb1a7-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="eb1a7-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="eb1a7-114">Text value</span></span>

<span data-ttu-id="eb1a7-115">Der Textwert des **ApprovalDecision** -Elements ist 1, wenn genehmigt, und 2, wenn er abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-115">The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eb1a7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb1a7-116">Remarks</span></span>

<span data-ttu-id="eb1a7-117">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="eb1a7-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="eb1a7-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb1a7-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="eb1a7-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb1a7-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb1a7-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb1a7-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eb1a7-121">Schema Name</span></span>  <br/> |<span data-ttu-id="eb1a7-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eb1a7-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb1a7-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eb1a7-123">Validation File</span></span>  <br/> |<span data-ttu-id="eb1a7-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb1a7-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb1a7-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eb1a7-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb1a7-126">True</span><span class="sxs-lookup"><span data-stu-id="eb1a7-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb1a7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb1a7-127">See also</span></span>

- [<span data-ttu-id="eb1a7-128">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="eb1a7-128">ApprovalRequestData</span></span>](approvalrequestdata.md)
- [<span data-ttu-id="eb1a7-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eb1a7-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

