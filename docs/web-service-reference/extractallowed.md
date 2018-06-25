---
title: ExtractAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc213f0e-a655-44e9-9ac9-bc1673bae1fe
description: Das ExtractAllowed-Element gibt an, ob entitätenextraktion aktiviert ist.
ms.openlocfilehash: 48584e50be0ff66d156d9a3c3768729d63a9a3fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758403"
---
# <a name="extractallowed"></a><span data-ttu-id="f27bb-103">ExtractAllowed</span><span class="sxs-lookup"><span data-stu-id="f27bb-103">ExtractAllowed</span></span>

<span data-ttu-id="f27bb-104">Das **ExtractAllowed** -Element gibt an, ob entitätenextraktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f27bb-104">The **ExtractAllowed** element specifies whether entity extraction is enabled.</span></span> 
  
```XML
<ExtractAllowed>true | false</ExtractAllowed
```

 <span data-ttu-id="f27bb-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f27bb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f27bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f27bb-106">Attributes and elements</span></span>

<span data-ttu-id="f27bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f27bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f27bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f27bb-108">Attributes</span></span>

<span data-ttu-id="f27bb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f27bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f27bb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f27bb-110">Child elements</span></span>

<span data-ttu-id="f27bb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f27bb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f27bb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f27bb-112">Parent elements</span></span>

|<span data-ttu-id="f27bb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f27bb-113">**Element**</span></span>|<span data-ttu-id="f27bb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f27bb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f27bb-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="f27bb-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="f27bb-116">Gibt Informationen zu den Rights Management-Lizenz.</span><span class="sxs-lookup"><span data-stu-id="f27bb-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f27bb-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f27bb-117">Text value</span></span>

<span data-ttu-id="f27bb-118">Der Textwert **true** für das **ExtractAllowed** -Element gibt an, dass entitätenextraktion aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f27bb-118">A text value of **true** for the **ExtractAllowed** element indicates that entity extraction is enabled.</span></span> <span data-ttu-id="f27bb-119">Der Wert **false** gibt an, dass entitätenextraktion nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f27bb-119">A value of **false** indicates that entity extraction is not enabled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f27bb-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f27bb-120">Remarks</span></span>

<span data-ttu-id="f27bb-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f27bb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f27bb-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f27bb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f27bb-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f27bb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27bb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f27bb-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f27bb-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f27bb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f27bb-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="f27bb-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f27bb-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f27bb-127">Validation File</span></span>  <br/> |<span data-ttu-id="f27bb-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f27bb-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f27bb-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f27bb-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f27bb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f27bb-130">See also</span></span>



- [<span data-ttu-id="f27bb-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f27bb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

