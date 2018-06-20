---
title: Domäne
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 7e45a061-856f-4b44-b053-a7c4d5ad569e
description: Das Domäne-Element identifiziert eine einzelne SMTP-Domäne.
ms.openlocfilehash: 78eb1edfd347a513b84b9c15d143d76425041e85
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758090"
---
# <a name="domain"></a><span data-ttu-id="b9b5c-103">Domäne</span><span class="sxs-lookup"><span data-stu-id="b9b5c-103">Domain</span></span>

<span data-ttu-id="b9b5c-104">Das **Domäne** -Element identifiziert eine einzelne SMTP-Domäne.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-104">The **Domain** element identifies a single SMTP domain.</span></span> 
  
```xml
<Domain Name="" IncludeSubdomains="" />
```

 <span data-ttu-id="b9b5c-105">**StmpDomain**</span><span class="sxs-lookup"><span data-stu-id="b9b5c-105">**StmpDomain**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9b5c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b9b5c-106">Attributes and elements</span></span>

<span data-ttu-id="b9b5c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9b5c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9b5c-108">Attributes</span></span>

|<span data-ttu-id="b9b5c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b9b5c-109">**Attribute**</span></span>|<span data-ttu-id="b9b5c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9b5c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9b5c-111">Name</span><span class="sxs-lookup"><span data-stu-id="b9b5c-111">Name</span></span>  <br/> |<span data-ttu-id="b9b5c-112">Gibt den Namen einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-112">Identifies the name of a domain.</span></span> <span data-ttu-id="b9b5c-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="b9b5c-114">IncludeSubdomains</span><span class="sxs-lookup"><span data-stu-id="b9b5c-114">IncludeSubdomains</span></span>  <br/> |<span data-ttu-id="b9b5c-115">Gibt an, ob Unterdomänen der durch das **Name** -Attribut identifiziert Domäne als interne betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-115">Indicates whether subdomains of the domain identified by the **Name** attribute are considered internal.</span></span> <span data-ttu-id="b9b5c-116">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-116">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9b5c-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9b5c-117">Child elements</span></span>

<span data-ttu-id="b9b5c-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9b5c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9b5c-119">Parent elements</span></span>

|<span data-ttu-id="b9b5c-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9b5c-120">**Element**</span></span>|<span data-ttu-id="b9b5c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9b5c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9b5c-122">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="b9b5c-122">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="b9b5c-123">Gibt die Liste der internen SMTP-Domänen der Organisation.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-123">Identifies the list of internal SMTP domains of the organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b9b5c-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="b9b5c-124">Text value</span></span>

<span data-ttu-id="b9b5c-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9b5c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9b5c-126">Remarks</span></span>

<span data-ttu-id="b9b5c-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b9b5c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9b5c-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b9b5c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9b5c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9b5c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9b5c-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b9b5c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b9b5c-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b9b5c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9b5c-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b9b5c-132">Validation File</span></span>  <br/> |<span data-ttu-id="b9b5c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9b5c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9b5c-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b9b5c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9b5c-135">False</span><span class="sxs-lookup"><span data-stu-id="b9b5c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9b5c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9b5c-136">See also</span></span>

- [<span data-ttu-id="b9b5c-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b9b5c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

