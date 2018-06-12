---
title: IsExternalMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: Das IsExternalMailbox -Element gibt an, ob das Postfach befindet sich außerhalb des Unternehmens.
ms.openlocfilehash: cf9f71e9b955cffd1bebefd5f23acba66ba1b894
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830010"
---
# <a name="isexternalmailbox"></a><span data-ttu-id="61420-103">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="61420-103">IsExternalMailbox</span></span>

<span data-ttu-id="61420-104">Das **IsExternalMailbox** -Element gibt an, ob das Postfach befindet sich außerhalb des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="61420-104">The **IsExternalMailbox** element indicates whether the mailbox is external to the organization.</span></span> 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 <span data-ttu-id="61420-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="61420-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61420-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61420-106">Attributes and elements</span></span>

<span data-ttu-id="61420-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61420-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61420-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="61420-108">Attributes</span></span>

<span data-ttu-id="61420-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="61420-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61420-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61420-110">Child elements</span></span>

<span data-ttu-id="61420-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="61420-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61420-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61420-112">Parent elements</span></span>

[<span data-ttu-id="61420-113">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="61420-113">SearchableMailbox</span></span>](searchablemailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="61420-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="61420-114">Text value</span></span>

<span data-ttu-id="61420-p101">Der Textwert **true** für das **IsExternalMailbox** -Element gibt an, dass das Postfach in einer externen Organisation ist. Der Wert **false** gibt an, dass das Postfach in der Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="61420-p101">A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization. A value of **false** indicates that the mailbox is in the organization.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61420-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61420-117">Remarks</span></span>

<span data-ttu-id="61420-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61420-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="61420-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="61420-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61420-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="61420-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61420-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="61420-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61420-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61420-122">Schema name</span></span>  <br/> |<span data-ttu-id="61420-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="61420-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="61420-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61420-124">Validation file</span></span>  <br/> |<span data-ttu-id="61420-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61420-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="61420-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="61420-126">Can be empty</span></span>  <br/> |<span data-ttu-id="61420-127">False</span><span class="sxs-lookup"><span data-stu-id="61420-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61420-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61420-128">See also</span></span>



- [<span data-ttu-id="61420-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="61420-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

