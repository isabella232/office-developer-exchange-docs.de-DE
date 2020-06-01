---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: Das ConvertHtmlCodePageToUTF8-Element gibt an, ob der Element-HTML-Text in UTF8 konvertiert wird.
ms.openlocfilehash: a714eacd8cc105146a1471f062ec35dc16730d61
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457592"
---
# <a name="converthtmlcodepagetoutf8"></a><span data-ttu-id="914e9-103">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="914e9-103">ConvertHtmlCodePageToUTF8</span></span>

<span data-ttu-id="914e9-104">Das **ConvertHtmlCodePageToUTF8** -Element gibt an, ob der Element-HTML-Text in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="914e9-104">The **ConvertHtmlCodePageToUTF8** element indicates whether the item HTML body is converted to UTF8.</span></span> 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 <span data-ttu-id="914e9-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="914e9-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="914e9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="914e9-106">Attributes and elements</span></span>

<span data-ttu-id="914e9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="914e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="914e9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="914e9-108">Attributes</span></span>

<span data-ttu-id="914e9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="914e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="914e9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="914e9-110">Child elements</span></span>

<span data-ttu-id="914e9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="914e9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="914e9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="914e9-112">Parent elements</span></span>

|<span data-ttu-id="914e9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="914e9-113">**Element**</span></span>|<span data-ttu-id="914e9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="914e9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="914e9-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="914e9-115">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="914e9-116">Gibt eine Reihe von Eigenschaften an, die in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="914e9-116">Identifies a set of properties to return in a response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="914e9-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="914e9-117">Text value</span></span>

<span data-ttu-id="914e9-118">Der Textwert **true** für das **ConvertHtmlCodePageToUTF8** -Element gibt an, dass der HTML-Text in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="914e9-118">A text value of **true** for the **ConvertHtmlCodePageToUTF8** element indicates that the HTML body is converted to UTF8.</span></span> <span data-ttu-id="914e9-119">Der Textwert **false** gibt an, dass der HTML-Text nicht in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="914e9-119">A text value of **false** indicates that the HTML body is not converted to UTF8.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="914e9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="914e9-120">Remarks</span></span>

<span data-ttu-id="914e9-121">Der Standardwert **true** wird verwendet, wenn das **ConvertHtmlCodePageToUTF8** -Element in einer Anforderung nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="914e9-121">The default value of **true** is used if the **ConvertHtmlCodePageToUTF8** element is not specified in a request.</span></span> 
  
<span data-ttu-id="914e9-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="914e9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="914e9-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="914e9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="914e9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="914e9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="914e9-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="914e9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="914e9-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="914e9-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="914e9-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="914e9-127">Validation File</span></span>  <br/> |<span data-ttu-id="914e9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="914e9-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="914e9-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="914e9-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="914e9-130">False</span><span class="sxs-lookup"><span data-stu-id="914e9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="914e9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="914e9-131">See also</span></span>



- [<span data-ttu-id="914e9-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="914e9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

