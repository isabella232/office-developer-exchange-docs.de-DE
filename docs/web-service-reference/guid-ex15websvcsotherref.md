---
title: Guid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: Das Guid-Element gibt den global eindeutigen Bezeichner des Postfachs an.
ms.openlocfilehash: 35307a706523fc5c2916767c7508dec07deb8d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829799"
---
# <a name="guid"></a><span data-ttu-id="7cf0a-103">Guid</span><span class="sxs-lookup"><span data-stu-id="7cf0a-103">Guid</span></span>

<span data-ttu-id="7cf0a-104">Das **Guid** -Element gibt den global eindeutigen Bezeichner des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-104">The **Guid** element specifies the globally unique identifier of the mailbox.</span></span> 
  
```XML
<Guid></Guid>
```

 <span data-ttu-id="7cf0a-105">**GuidType**</span><span class="sxs-lookup"><span data-stu-id="7cf0a-105">**GuidType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cf0a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf0a-106">Attributes and elements</span></span>

<span data-ttu-id="7cf0a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cf0a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7cf0a-108">Attributes</span></span>

<span data-ttu-id="7cf0a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cf0a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf0a-110">Child elements</span></span>

<span data-ttu-id="7cf0a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7cf0a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7cf0a-112">Parent elements</span></span>

|<span data-ttu-id="7cf0a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cf0a-113">**Element**</span></span>|<span data-ttu-id="7cf0a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7cf0a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cf0a-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="7cf0a-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="7cf0a-116">Gibt ein Postfach aus einer Anforderung **GetSearchableMailboxes** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7cf0a-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="7cf0a-117">Text value</span></span>

<span data-ttu-id="7cf0a-118">Der Textwert der **Guid** -Element ist ein GUID-Wert, der ein Postfach eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-118">The text value of the **Guid** element is a GUID value that uniquely identifies a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7cf0a-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7cf0a-119">Remarks</span></span>

<span data-ttu-id="7cf0a-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7cf0a-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7cf0a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cf0a-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7cf0a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cf0a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cf0a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7cf0a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7cf0a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7cf0a-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="7cf0a-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="7cf0a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7cf0a-126">Validation File</span></span>  <br/> |<span data-ttu-id="7cf0a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7cf0a-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7cf0a-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7cf0a-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7cf0a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cf0a-129">See also</span></span>



- [<span data-ttu-id="7cf0a-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7cf0a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

