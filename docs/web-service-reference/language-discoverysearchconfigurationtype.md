---
title: Sprache (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Das Sprachelement (DiscoverySearchConfigurationType) gibt die Kultur für das kulturspezifische Format der Datumsbereiche verwendet werden. Es gibt auch die Sprache, die in einer Suchabfrage verwendet.
ms.openlocfilehash: 1e904ac4d7f525b2d12cfe83f0da33b9ed474066
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830197"
---
# <a name="language-discoverysearchconfigurationtype"></a><span data-ttu-id="23ee9-104">Sprache (DiscoverySearchConfigurationType)</span><span class="sxs-lookup"><span data-stu-id="23ee9-104">Language (DiscoverySearchConfigurationType)</span></span>

<span data-ttu-id="23ee9-105">Das Sprachelement **(DiscoverySearchConfigurationType)** gibt die Kultur für das kulturspezifische Format der Datumsbereiche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23ee9-105">The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges.</span></span> <span data-ttu-id="23ee9-106">Es gibt auch die Sprache, die in einer Suchabfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="23ee9-106">It also specifies the language used in a search query.</span></span> 
  
```XML
<Language />
```

 <span data-ttu-id="23ee9-107">**string**</span><span class="sxs-lookup"><span data-stu-id="23ee9-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23ee9-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee9-108">Attributes and elements</span></span>

<span data-ttu-id="23ee9-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="23ee9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23ee9-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="23ee9-110">Attributes</span></span>

<span data-ttu-id="23ee9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="23ee9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23ee9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee9-112">Child elements</span></span>

<span data-ttu-id="23ee9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="23ee9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="23ee9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee9-114">Parent elements</span></span>

[<span data-ttu-id="23ee9-115">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ee9-115">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="23ee9-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="23ee9-116">Text value</span></span>

<span data-ttu-id="23ee9-117">Der Textwert der Sprachelement **(DiscoverySearchConfigurationType)** ist ein Kultur oder Sprache.</span><span class="sxs-lookup"><span data-stu-id="23ee9-117">The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="23ee9-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23ee9-118">Remarks</span></span>

<span data-ttu-id="23ee9-119">Dieses Element gibt das Format der Datumsbereiche in den [SearchMailboxes Vorgang](searchmailboxes-operation.md) oder die [SetHoldOnMailboxes Operation](setholdonmailboxes-operation.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="23ee9-119">This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).</span></span>
  
<span data-ttu-id="23ee9-120">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="23ee9-120">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="23ee9-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="23ee9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23ee9-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="23ee9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23ee9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="23ee9-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23ee9-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="23ee9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="23ee9-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="23ee9-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="23ee9-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="23ee9-126">Validation File</span></span>  <br/> |<span data-ttu-id="23ee9-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23ee9-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23ee9-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="23ee9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="23ee9-129">True</span><span class="sxs-lookup"><span data-stu-id="23ee9-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23ee9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23ee9-130">See also</span></span>



[<span data-ttu-id="23ee9-131">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ee9-131">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)


- [<span data-ttu-id="23ee9-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="23ee9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

