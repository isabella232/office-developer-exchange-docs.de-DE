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
description: Das ServerVersionInfo-Element enthält die Version des Servers, der die Anforderung verarbeitet hat.
ms.openlocfilehash: b54b4833361ec78c7f8213473af4638965c7ddae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467648"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="41c20-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="41c20-104">Das **ServerVersionInfo** -Element enthält die Version des Servers, der die Anforderung verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="41c20-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="41c20-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="41c20-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41c20-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="41c20-106">Attributes and elements</span></span>

<span data-ttu-id="41c20-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="41c20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41c20-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="41c20-108">Attributes</span></span>

<span data-ttu-id="41c20-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="41c20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41c20-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41c20-110">Child elements</span></span>

|<span data-ttu-id="41c20-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="41c20-111">**Element**</span></span>|<span data-ttu-id="41c20-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41c20-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41c20-113">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="41c20-114">Die Hauptversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="41c20-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41c20-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="41c20-116">Die Nebenversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="41c20-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41c20-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="41c20-118">Die Hauptnummer des Builds für den Server.</span><span class="sxs-lookup"><span data-stu-id="41c20-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41c20-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="41c20-120">Die Nebenversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="41c20-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="41c20-121">Version (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41c20-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="41c20-122">Eine Beschreibung der Server Produktversion.</span><span class="sxs-lookup"><span data-stu-id="41c20-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41c20-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41c20-123">Parent elements</span></span>

<span data-ttu-id="41c20-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="41c20-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41c20-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41c20-125">Remarks</span></span>

<span data-ttu-id="41c20-126">Dieses Element wird im SOAP-Header zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41c20-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41c20-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="41c20-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41c20-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="41c20-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41c20-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="41c20-129">Schema Name</span></span>  <br/> |<span data-ttu-id="41c20-130">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="41c20-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41c20-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="41c20-131">Validation File</span></span>  <br/> |<span data-ttu-id="41c20-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="41c20-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41c20-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="41c20-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="41c20-134">True</span><span class="sxs-lookup"><span data-stu-id="41c20-134">True</span></span>  <br/> |
   

