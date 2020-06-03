---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: Das RequestServerVersion-Element enthält die Versions Verwaltungsinformationen, die die Schemaversion identifiziert, die für eine Anforderung als Ziel festgelegt werden soll.
ms.openlocfilehash: c4ae59a03c812d21153e4338734185d933d914ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468320"
---
# <a name="requestserverversion"></a><span data-ttu-id="a0539-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a0539-103">RequestServerVersion</span></span>

<span data-ttu-id="a0539-104">Das **RequestServerVersion** -Element enthält die Versions Verwaltungsinformationen, die die Schemaversion identifiziert, die für eine Anforderung als Ziel festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0539-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="a0539-105">**Einfachen exchangeversiontype**</span><span class="sxs-lookup"><span data-stu-id="a0539-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0539-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0539-106">Attributes and elements</span></span>

<span data-ttu-id="a0539-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0539-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0539-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0539-108">Attributes</span></span>

|<span data-ttu-id="a0539-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a0539-109">**Attribute**</span></span>|<span data-ttu-id="a0539-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0539-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0539-111">Version</span><span class="sxs-lookup"><span data-stu-id="a0539-111">Version</span></span>  <br/> |<span data-ttu-id="a0539-112">Beschreibt die Zielversion für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a0539-112">Describes the version to target for the request.</span></span> <span data-ttu-id="a0539-113">Dieses Attribut ist erforderlich, wenn die Zielserver Version eine Version von Exchange ist, die mit Exchange Server 2010 beginnt.</span><span class="sxs-lookup"><span data-stu-id="a0539-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="a0539-114">Version-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="a0539-114">Version attribute values</span></span>

|<span data-ttu-id="a0539-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a0539-115">**Value**</span></span>|<span data-ttu-id="a0539-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0539-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0539-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="a0539-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="a0539-118">Richten Sie die Schemadateien für die erste Version von Exchange 2007 ein.</span><span class="sxs-lookup"><span data-stu-id="a0539-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="a0539-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="a0539-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="a0539-120">Richten Sie die Schemadateien für Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) und Exchange 2007 Service Pack 3 (SP3) aus.</span><span class="sxs-lookup"><span data-stu-id="a0539-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="a0539-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="a0539-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="a0539-122">Richten Sie die Schemadateien für Exchange 2010 ein.</span><span class="sxs-lookup"><span data-stu-id="a0539-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="a0539-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="a0539-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="a0539-124">Richten Sie die Schemadateien für Exchange 2010 Service Pack 1 (SP1) ein.</span><span class="sxs-lookup"><span data-stu-id="a0539-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="a0539-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="a0539-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="a0539-126">Richten Sie die Schemadateien für Exchange 2010 Service Pack 2 (SP2) und Exchange 2010 Service Pack 3 (SP3) aus.</span><span class="sxs-lookup"><span data-stu-id="a0539-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="a0539-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="a0539-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="a0539-128">Richten Sie die Schemadateien für Exchange 2013 ein.</span><span class="sxs-lookup"><span data-stu-id="a0539-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="a0539-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="a0539-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="a0539-130">Richten Sie die Schemadateien für Exchange 2013 Service Pack 1 (SP1) ein.</span><span class="sxs-lookup"><span data-stu-id="a0539-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0539-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0539-131">Child elements</span></span>

<span data-ttu-id="a0539-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0539-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0539-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0539-133">Parent elements</span></span>

<span data-ttu-id="a0539-134">Das **RequestServerVersion** -Element befindet sich im SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="a0539-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a0539-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0539-135">Remarks</span></span>

<span data-ttu-id="a0539-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a0539-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0539-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a0539-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0539-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0539-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a0539-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a0539-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a0539-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a0539-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="a0539-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a0539-141">Validation File</span></span>  <br/> |<span data-ttu-id="a0539-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a0539-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a0539-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a0539-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a0539-144">False</span><span class="sxs-lookup"><span data-stu-id="a0539-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0539-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0539-145">See also</span></span>



- [<span data-ttu-id="a0539-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a0539-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="a0539-147">Anforderungen für die Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="a0539-147">Versioning Requests</span></span>](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

