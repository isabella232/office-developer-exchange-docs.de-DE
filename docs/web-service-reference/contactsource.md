---
title: ContactSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactSource
api_type:
- schema
ms.assetid: 500b0423-864e-4cde-a39b-6b5b06d1aa6a
description: Das ContactSource-Element beschreibt, ob der Kontakt in der Exchange-Speicher oder Active Directory-Domänendienste (AD DS) befindet.
ms.openlocfilehash: a82b766fc81b9397fc707415ea82e2f2d63d952d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757625"
---
# <a name="contactsource"></a><span data-ttu-id="83914-103">ContactSource</span><span class="sxs-lookup"><span data-stu-id="83914-103">ContactSource</span></span>

<span data-ttu-id="83914-104">Das **ContactSource** -Element beschreibt, ob der Kontakt in der Exchange-Speicher oder Active Directory-Domänendienste (AD DS) befindet.</span><span class="sxs-lookup"><span data-stu-id="83914-104">The **ContactSource** element describes whether the contact is located in the Exchange store or Active Directory Domain Services (AD DS).</span></span> 
  
```xml
<ContactSource/>
```

 <span data-ttu-id="83914-105">**ContactSourceType**</span><span class="sxs-lookup"><span data-stu-id="83914-105">**ContactSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83914-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83914-106">Attributes and elements</span></span>

<span data-ttu-id="83914-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83914-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83914-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83914-108">Attributes</span></span>

<span data-ttu-id="83914-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83914-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83914-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83914-110">Child elements</span></span>

<span data-ttu-id="83914-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="83914-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83914-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83914-112">Parent elements</span></span>

|<span data-ttu-id="83914-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83914-113">**Element**</span></span>|<span data-ttu-id="83914-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83914-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83914-115">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="83914-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="83914-116">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="83914-116">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="83914-117">DistributionList</span><span class="sxs-lookup"><span data-stu-id="83914-117">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="83914-118">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="83914-118">Represents a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83914-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="83914-119">Text value</span></span>

<span data-ttu-id="83914-120">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="83914-120">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="83914-121">ActiveDirectory-Umgebung</span><span class="sxs-lookup"><span data-stu-id="83914-121">ActiveDirectory</span></span>
    
- <span data-ttu-id="83914-122">Store</span><span class="sxs-lookup"><span data-stu-id="83914-122">Store</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83914-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83914-123">Remarks</span></span>

<span data-ttu-id="83914-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83914-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83914-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="83914-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83914-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="83914-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83914-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83914-127">Schema name</span></span>  <br/> |<span data-ttu-id="83914-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83914-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="83914-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83914-129">Validation file</span></span>  <br/> |<span data-ttu-id="83914-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83914-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83914-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="83914-131">Can be empty</span></span>  <br/> |<span data-ttu-id="83914-132">False</span><span class="sxs-lookup"><span data-stu-id="83914-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83914-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83914-133">See also</span></span>



- [<span data-ttu-id="83914-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83914-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

