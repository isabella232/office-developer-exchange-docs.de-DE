---
title: Sprache (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Das Language (DiscoverySearchConfigurationType)-Element gibt die Kultur an, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll. Außerdem wird die in einer Suchabfrage verwendete Sprache angegeben.
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463286"
---
# <a name="language-discoverysearchconfigurationtype"></a><span data-ttu-id="f6ac4-104">Sprache (DiscoverySearchConfigurationType)</span><span class="sxs-lookup"><span data-stu-id="f6ac4-104">Language (DiscoverySearchConfigurationType)</span></span>

<span data-ttu-id="f6ac4-105">Das **Language (DiscoverySearchConfigurationType)** -Element gibt die Kultur an, die für das kulturspezifische Format von Datumsbereichen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-105">The **Language (DiscoverySearchConfigurationType)** element identifies the culture to be used for the culture-specific format of date ranges.</span></span> <span data-ttu-id="f6ac4-106">Außerdem wird die in einer Suchabfrage verwendete Sprache angegeben.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-106">It also specifies the language used in a search query.</span></span> 
  
```XML
<Language />
```

 <span data-ttu-id="f6ac4-107">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f6ac4-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6ac4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f6ac4-108">Attributes and elements</span></span>

<span data-ttu-id="f6ac4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6ac4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6ac4-110">Attributes</span></span>

<span data-ttu-id="f6ac4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6ac4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6ac4-112">Child elements</span></span>

<span data-ttu-id="f6ac4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f6ac4-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6ac4-114">Parent elements</span></span>

[<span data-ttu-id="f6ac4-115">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6ac4-115">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
  
## <a name="text-value"></a><span data-ttu-id="f6ac4-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="f6ac4-116">Text value</span></span>

<span data-ttu-id="f6ac4-117">Der Textwert des **Language (DiscoverySearchConfigurationType)-** Elements ist eine Kultur oder Sprache.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-117">The text value of the **Language (DiscoverySearchConfigurationType)** element is a culture or language.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f6ac4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6ac4-118">Remarks</span></span>

<span data-ttu-id="f6ac4-119">Dieses Element gibt das Format von Datumsbereichen an, die im [SearchMailboxes-Vorgang](searchmailboxes-operation.md) oder im SetHoldOnMailboxes- [Vorgang](setholdonmailboxes-operation.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-119">This element specifies the format of date ranges specified in the [SearchMailboxes operation](searchmailboxes-operation.md) or the [SetHoldOnMailboxes operation](setholdonmailboxes-operation.md).</span></span>
  
<span data-ttu-id="f6ac4-120">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-120">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="f6ac4-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6ac4-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f6ac4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6ac4-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6ac4-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6ac4-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f6ac4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f6ac4-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f6ac4-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6ac4-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f6ac4-126">Validation File</span></span>  <br/> |<span data-ttu-id="f6ac4-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6ac4-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6ac4-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f6ac4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6ac4-129">True</span><span class="sxs-lookup"><span data-stu-id="f6ac4-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6ac4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ac4-130">See also</span></span>



[<span data-ttu-id="f6ac4-131">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6ac4-131">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)


- [<span data-ttu-id="f6ac4-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f6ac4-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

