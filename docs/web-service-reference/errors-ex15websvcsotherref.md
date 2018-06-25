---
title: Fehler
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Errors
api_type:
- schema
ms.assetid: ea37a2b5-e2d1-4089-960f-7014b9535a50
description: Das Fehler-Element enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.
ms.openlocfilehash: a029492c1e3c11cc31d3501bd4ea0024ef8ecb91
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758275"
---
# <a name="errors"></a><span data-ttu-id="0d1ba-103">Fehler</span><span class="sxs-lookup"><span data-stu-id="0d1ba-103">Errors</span></span>

<span data-ttu-id="0d1ba-104">Das **Fehler** -Element enthält einen Eigenschaftenbehälter zum Speichern von Fehlern, die über den Webdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-104">The **Errors** element contains a property bag to store errors that are returned through the Web service.</span></span> 
  
[<span data-ttu-id="0d1ba-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0d1ba-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
[<span data-ttu-id="0d1ba-106">Fehler</span><span class="sxs-lookup"><span data-stu-id="0d1ba-106">Errors</span></span>](errors-ex15websvcsotherref.md)
  
```xml
<Errors>
   <Properties/>
</Errors>
```

 <span data-ttu-id="0d1ba-107">**ArrayOfArraysOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="0d1ba-107">**ArrayOfArraysOfTrackingPropertiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d1ba-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d1ba-108">Attributes and elements</span></span>

<span data-ttu-id="0d1ba-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d1ba-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d1ba-110">Attributes</span></span>

<span data-ttu-id="0d1ba-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d1ba-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d1ba-112">Child elements</span></span>

|<span data-ttu-id="0d1ba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d1ba-113">**Element**</span></span>|<span data-ttu-id="0d1ba-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d1ba-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d1ba-115">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0d1ba-115">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="0d1ba-116">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-116">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d1ba-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d1ba-117">Parent elements</span></span>

|<span data-ttu-id="0d1ba-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d1ba-118">**Element**</span></span>|<span data-ttu-id="0d1ba-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d1ba-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d1ba-120">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="0d1ba-120">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="0d1ba-121">Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0d1ba-121">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="0d1ba-122">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="0d1ba-122">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="0d1ba-123">Enthält das Ergebnis einer einzelnen Anforderung [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0d1ba-123">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d1ba-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="0d1ba-124">Text value</span></span>

<span data-ttu-id="0d1ba-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d1ba-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d1ba-126">Remarks</span></span>

<span data-ttu-id="0d1ba-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d1ba-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d1ba-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0d1ba-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d1ba-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d1ba-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d1ba-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d1ba-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0d1ba-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0d1ba-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0d1ba-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d1ba-132">Validation File</span></span>  <br/> |<span data-ttu-id="0d1ba-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d1ba-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d1ba-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0d1ba-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d1ba-135">False</span><span class="sxs-lookup"><span data-stu-id="0d1ba-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d1ba-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d1ba-136">See also</span></span>



[<span data-ttu-id="0d1ba-137">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d1ba-137">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="0d1ba-138">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d1ba-138">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="0d1ba-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0d1ba-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

