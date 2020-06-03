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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467648"
---
# <a name="serverversioninfo-soap"></a><span data-ttu-id="20bf8-103">ServerVersionInfo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-103">ServerVersionInfo (SOAP)</span></span>

<span data-ttu-id="20bf8-104">Das **ServerVersionInfo** -Element enthält die Version des Servers, der die Anforderung verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="20bf8-104">The **ServerVersionInfo** element contains the version of the server that processed the request.</span></span> 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 <span data-ttu-id="20bf8-105">**ServerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="20bf8-105">**ServerVersionInfo**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20bf8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="20bf8-106">Attributes and elements</span></span>

<span data-ttu-id="20bf8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="20bf8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20bf8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="20bf8-108">Attributes</span></span>

<span data-ttu-id="20bf8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="20bf8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20bf8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20bf8-110">Child elements</span></span>

|<span data-ttu-id="20bf8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="20bf8-111">**Element**</span></span>|<span data-ttu-id="20bf8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20bf8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20bf8-113">MajorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-113">MajorVersion (SOAP)</span></span>](majorversion-soap.md) <br/> |<span data-ttu-id="20bf8-114">Die Hauptversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="20bf8-114">The major version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="20bf8-115">MinorVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-115">MinorVersion (SOAP)</span></span>](minorversion-soap.md) <br/> |<span data-ttu-id="20bf8-116">Die Nebenversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="20bf8-116">The minor version number for the server.</span></span>  <br/> |
|[<span data-ttu-id="20bf8-117">MajorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-117">MajorBuildNumber (SOAP)</span></span>](majorbuildnumber-soap.md) <br/> |<span data-ttu-id="20bf8-118">Die Hauptnummer des Builds für den Server.</span><span class="sxs-lookup"><span data-stu-id="20bf8-118">The major build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="20bf8-119">MinorBuildNumber (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-119">MinorBuildNumber (SOAP)</span></span>](minorbuildnumber-soap.md) <br/> |<span data-ttu-id="20bf8-120">Die Nebenversionsnummer für den Server.</span><span class="sxs-lookup"><span data-stu-id="20bf8-120">The minor build number for the server.</span></span>  <br/> |
|[<span data-ttu-id="20bf8-121">Version (SOAP)</span><span class="sxs-lookup"><span data-stu-id="20bf8-121">Version (SOAP)</span></span>](version-soap.md) <br/> |<span data-ttu-id="20bf8-122">Eine Beschreibung der Server Produktversion.</span><span class="sxs-lookup"><span data-stu-id="20bf8-122">A description of the server product version.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="20bf8-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20bf8-123">Parent elements</span></span>

<span data-ttu-id="20bf8-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="20bf8-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20bf8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20bf8-125">Remarks</span></span>

<span data-ttu-id="20bf8-126">Dieses Element wird im SOAP-Header zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20bf8-126">This element is returned in the SOAP header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20bf8-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="20bf8-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20bf8-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="20bf8-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="20bf8-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="20bf8-129">Schema Name</span></span>  <br/> |<span data-ttu-id="20bf8-130">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="20bf8-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="20bf8-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="20bf8-131">Validation File</span></span>  <br/> |<span data-ttu-id="20bf8-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="20bf8-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20bf8-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="20bf8-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="20bf8-134">True</span><span class="sxs-lookup"><span data-stu-id="20bf8-134">True</span></span>  <br/> |
   

