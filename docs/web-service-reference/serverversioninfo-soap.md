---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: Das ServerVersionInfo-Element enthält die Version des Servers, der die Anforderung verarbeitet.
ms.openlocfilehash: b02071e4997aba91fb538d52df2612fe6fd32800
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831385"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="41751-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="41751-104">Das **ServerVersionInfo** -Element enthält die Version des Servers, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="41751-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="41751-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="41751-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41751-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="41751-106">Attributes and elements</span></span>

<span data-ttu-id="41751-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="41751-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41751-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="41751-108">Attributes</span></span>

<span data-ttu-id="41751-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="41751-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41751-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41751-110">Child elements</span></span>

|<span data-ttu-id="41751-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="41751-111">**Element**</span></span>|<span data-ttu-id="41751-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41751-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41751-113">Hauptversion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="41751-114">Die Nummer der Hauptversion für den Server.</span><span class="sxs-lookup"><span data-stu-id="41751-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41751-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="41751-116">Die Nummer der Nebenversion für den Server.</span><span class="sxs-lookup"><span data-stu-id="41751-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41751-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="41751-118">Die wichtigsten Buildnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="41751-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41751-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="41751-120">Die minor Buildnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="41751-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41751-121">Version (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41751-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="41751-122">Eine Beschreibung der Version des Produkts.</span><span class="sxs-lookup"><span data-stu-id="41751-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41751-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41751-123">Parent elements</span></span>

<span data-ttu-id="41751-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="41751-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41751-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41751-125">Remarks</span></span>

<span data-ttu-id="41751-126">Dieses Element wird in den SOAP-Header zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41751-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41751-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="41751-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41751-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="41751-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41751-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="41751-129">Schema Name</span></span>  <br/> |<span data-ttu-id="41751-130">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="41751-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41751-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="41751-131">Validation File</span></span>  <br/> |<span data-ttu-id="41751-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41751-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41751-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="41751-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="41751-134">True</span><span class="sxs-lookup"><span data-stu-id="41751-134">True</span></span>  <br/> |
   

