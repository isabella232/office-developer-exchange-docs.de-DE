---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: Das ConvertHtmlCodePageToUTF8-Element gibt an, ob das Element HTML-Textkörper UTF8 konvertiert wird.
ms.openlocfilehash: aff6579835097a273101188c02a9919003b71b58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757715"
---
# <a name="converthtmlcodepagetoutf8"></a><span data-ttu-id="669c0-103">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="669c0-103">ConvertHtmlCodePageToUTF8</span></span>

<span data-ttu-id="669c0-104">Das **ConvertHtmlCodePageToUTF8** -Element gibt an, ob das Element HTML-Textkörper UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="669c0-104">The **ConvertHtmlCodePageToUTF8** element indicates whether the item HTML body is converted to UTF8.</span></span> 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 <span data-ttu-id="669c0-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="669c0-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="669c0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="669c0-106">Attributes and elements</span></span>

<span data-ttu-id="669c0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="669c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="669c0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="669c0-108">Attributes</span></span>

<span data-ttu-id="669c0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="669c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="669c0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="669c0-110">Child elements</span></span>

<span data-ttu-id="669c0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="669c0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="669c0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="669c0-112">Parent elements</span></span>

|<span data-ttu-id="669c0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="669c0-113">**Element**</span></span>|<span data-ttu-id="669c0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="669c0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="669c0-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="669c0-115">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="669c0-116">Identifiziert eine Reihe von Eigenschaften in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="669c0-116">Identifies a set of properties to return in a response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="669c0-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="669c0-117">Text value</span></span>

<span data-ttu-id="669c0-118">Der Textwert **true** für das **ConvertHtmlCodePageToUTF8** -Element gibt an, dass der HTML-Textkörper in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="669c0-118">A text value of **true** for the **ConvertHtmlCodePageToUTF8** element indicates that the HTML body is converted to UTF8.</span></span> <span data-ttu-id="669c0-119">Der Textwert **false** gibt an, dass der HTML-Textkörper in UTF8 nicht konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="669c0-119">A text value of **false** indicates that the HTML body is not converted to UTF8.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="669c0-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="669c0-120">Remarks</span></span>

<span data-ttu-id="669c0-121">Wenn das **ConvertHtmlCodePageToUTF8** -Element in einer Anforderung nicht angegeben ist, wird der Standardwert **true** verwendet.</span><span class="sxs-lookup"><span data-stu-id="669c0-121">The default value of **true** is used if the **ConvertHtmlCodePageToUTF8** element is not specified in a request.</span></span> 
  
<span data-ttu-id="669c0-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="669c0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="669c0-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="669c0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="669c0-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="669c0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="669c0-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="669c0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="669c0-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="669c0-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="669c0-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="669c0-127">Validation File</span></span>  <br/> |<span data-ttu-id="669c0-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="669c0-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="669c0-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="669c0-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="669c0-130">False</span><span class="sxs-lookup"><span data-stu-id="669c0-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="669c0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="669c0-131">See also</span></span>



- [<span data-ttu-id="669c0-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="669c0-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

