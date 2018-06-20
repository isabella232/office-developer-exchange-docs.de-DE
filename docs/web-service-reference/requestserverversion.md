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
description: Das RequestServerVersion-Element enthält die Versionsinformationen, die die Schemaversion als Ziel für eine Anforderung identifiziert.
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831143"
---
# <a name="requestserverversion"></a><span data-ttu-id="86310-103">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="86310-103">RequestServerVersion</span></span>

<span data-ttu-id="86310-104">Das **RequestServerVersion** -Element enthält die Versionsinformationen, die die Schemaversion als Ziel für eine Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="86310-104">The **RequestServerVersion** element contains the versioning information that identifies the schema version to target for a request.</span></span> 
  
```XML
<RequestServerVersion Version=""/>
```

 <span data-ttu-id="86310-105">**ExchangeVersionType**</span><span class="sxs-lookup"><span data-stu-id="86310-105">**ExchangeVersionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86310-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86310-106">Attributes and elements</span></span>

<span data-ttu-id="86310-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86310-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86310-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="86310-108">Attributes</span></span>

|<span data-ttu-id="86310-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="86310-109">**Attribute**</span></span>|<span data-ttu-id="86310-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86310-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86310-111">Version</span><span class="sxs-lookup"><span data-stu-id="86310-111">Version</span></span>  <br/> |<span data-ttu-id="86310-112">Beschreibt die Version als Ziel für die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="86310-112">Describes the version to target for the request.</span></span> <span data-ttu-id="86310-113">Dieses Attribut ist erforderlich, wenn die Zielversion Server eine Version von Exchange, beginnend mit Exchange Server 2010 ist.</span><span class="sxs-lookup"><span data-stu-id="86310-113">This attribute is required when the target server version is a version of Exchange starting with Exchange Server 2010.</span></span>  <br/> |
   
#### <a name="version-attribute-values"></a><span data-ttu-id="86310-114">Version-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="86310-114">Version attribute values</span></span>

|<span data-ttu-id="86310-115">**Wert**</span><span class="sxs-lookup"><span data-stu-id="86310-115">**Value**</span></span>|<span data-ttu-id="86310-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86310-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86310-117">Exchange2007</span><span class="sxs-lookup"><span data-stu-id="86310-117">Exchange2007</span></span>  <br/> |<span data-ttu-id="86310-118">Ziel der ursprünglich freigegebenen Version von Exchange 2007-Schemadateien.</span><span class="sxs-lookup"><span data-stu-id="86310-118">Target the schema files for the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="86310-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="86310-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="86310-120">Ziel: die Schemadateien für Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) und Exchange 2007 Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="86310-120">Target the schema files for Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2), and Exchange 2007 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="86310-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="86310-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="86310-122">Ziel: die Schemadateien für Exchange 2010 ein.</span><span class="sxs-lookup"><span data-stu-id="86310-122">Target the schema files for Exchange 2010.</span></span>  <br/> |
|<span data-ttu-id="86310-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="86310-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="86310-124">Ziel: die Schemadateien für Exchange 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="86310-124">Target the schema files for Exchange 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="86310-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="86310-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="86310-126">Ziel: die Schemadateien für Exchange 2010 Service Pack 2 (SP2) und Exchange 2010 Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="86310-126">Target the schema files for Exchange 2010 Service Pack 2 (SP2) and Exchange 2010 Service Pack 3 (SP3).</span></span>  <br/> |
|<span data-ttu-id="86310-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="86310-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="86310-128">Ziel: die Schemadateien für Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="86310-128">Target the schema files for Exchange 2013.</span></span>  <br/> |
|<span data-ttu-id="86310-129">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="86310-129">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="86310-130">Ziel: die Schemadateien für Exchange 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="86310-130">Target the schema files for Exchange 2013 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86310-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86310-131">Child elements</span></span>

<span data-ttu-id="86310-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="86310-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="86310-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86310-133">Parent elements</span></span>

<span data-ttu-id="86310-134">Das Element **RequestServerVersion** befindet sich die SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="86310-134">The **RequestServerVersion** element is located in the SOAP header.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="86310-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86310-135">Remarks</span></span>

<span data-ttu-id="86310-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86310-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86310-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="86310-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86310-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="86310-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86310-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86310-139">Schema Name</span></span>  <br/> |<span data-ttu-id="86310-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="86310-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="86310-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86310-141">Validation File</span></span>  <br/> |<span data-ttu-id="86310-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="86310-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86310-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="86310-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="86310-144">False</span><span class="sxs-lookup"><span data-stu-id="86310-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86310-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86310-145">See also</span></span>



- [<span data-ttu-id="86310-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="86310-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="86310-147">Versioning Anfragen</span><span class="sxs-lookup"><span data-stu-id="86310-147">Versioning Requests</span></span>](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

