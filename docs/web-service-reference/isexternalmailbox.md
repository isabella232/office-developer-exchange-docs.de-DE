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
ms.openlocfilehash: 9be702b05e89857913023a8ec34b78ea4c309274
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455289"
---
# <a name="isexternalmailbox"></a><span data-ttu-id="b4049-103">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="b4049-103">IsExternalMailbox</span></span>

<span data-ttu-id="b4049-104">Das **IsExternalMailbox** -Element gibt an, ob das Postfach befindet sich außerhalb des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="b4049-104">The **IsExternalMailbox** element indicates whether the mailbox is external to the organization.</span></span> 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 <span data-ttu-id="b4049-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b4049-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4049-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b4049-106">Attributes and elements</span></span>

<span data-ttu-id="b4049-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b4049-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4049-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b4049-108">Attributes</span></span>

<span data-ttu-id="b4049-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4049-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4049-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4049-110">Child elements</span></span>

<span data-ttu-id="b4049-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b4049-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4049-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b4049-112">Parent elements</span></span>

[<span data-ttu-id="b4049-113">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="b4049-113">SearchableMailbox</span></span>](searchablemailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="b4049-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b4049-114">Text value</span></span>

<span data-ttu-id="b4049-p101">Der Textwert **true** für das **IsExternalMailbox** -Element gibt an, dass das Postfach in einer externen Organisation ist. Der Wert **false** gibt an, dass das Postfach in der Organisation ist.</span><span class="sxs-lookup"><span data-stu-id="b4049-p101">A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization. A value of **false** indicates that the mailbox is in the organization.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b4049-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4049-117">Remarks</span></span>

<span data-ttu-id="b4049-118">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b4049-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b4049-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b4049-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4049-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b4049-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4049-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4049-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4049-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b4049-122">Schema name</span></span>  <br/> |<span data-ttu-id="b4049-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b4049-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4049-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b4049-124">Validation file</span></span>  <br/> |<span data-ttu-id="b4049-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4049-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4049-126">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b4049-126">Can be empty</span></span>  <br/> |<span data-ttu-id="b4049-127">False</span><span class="sxs-lookup"><span data-stu-id="b4049-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4049-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4049-128">See also</span></span>



- [<span data-ttu-id="b4049-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b4049-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

