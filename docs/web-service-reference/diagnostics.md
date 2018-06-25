---
title: Diagnose
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Diagnostics
api_type:
- schema
ms.assetid: fecea440-970a-49da-9796-534ca470cbd6
description: Das Diagnose-Element enthält Timing und Leistung, die für die berichterstellung in einem Rechenzentrum verwendet wird.
ms.openlocfilehash: 2b9cac54a683967ec274b8681fb9a0c8a844205e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757970"
---
# <a name="diagnostics"></a><span data-ttu-id="f814c-103">Diagnose</span><span class="sxs-lookup"><span data-stu-id="f814c-103">Diagnostics</span></span>

<span data-ttu-id="f814c-104">Das **Diagnose** -Element enthält Timing und Leistung, die für die berichterstellung in einem Rechenzentrum verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f814c-104">The **Diagnostics** element provides timing and performance information that is used for reporting in a DataCenter.</span></span> 
  
```XML
<Diagnostics>
   <String/>
</Diagnostics>

```

 <span data-ttu-id="f814c-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="f814c-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f814c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f814c-106">Attributes and elements</span></span>

<span data-ttu-id="f814c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f814c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f814c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f814c-108">Attributes</span></span>

<span data-ttu-id="f814c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f814c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f814c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f814c-110">Child elements</span></span>

|<span data-ttu-id="f814c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f814c-111">**Element**</span></span>|<span data-ttu-id="f814c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f814c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f814c-113">String</span><span class="sxs-lookup"><span data-stu-id="f814c-113">String</span></span>](string.md) <br/> |<span data-ttu-id="f814c-114">Enthält eine Zeichenfolge, die von Elementen, Kontakte, Aufgaben und Unterhaltungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f814c-114">Contains a string that is used by items, contacts, tasks, and conversations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f814c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f814c-115">Parent elements</span></span>

|<span data-ttu-id="f814c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f814c-116">**Element**</span></span>|<span data-ttu-id="f814c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f814c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f814c-118">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="f814c-118">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="f814c-119">Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="f814c-119">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="f814c-120">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="f814c-120">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="f814c-121">Enthält die Antwort für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f814c-121">Contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f814c-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="f814c-122">Text value</span></span>

<span data-ttu-id="f814c-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="f814c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f814c-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f814c-124">Remarks</span></span>

<span data-ttu-id="f814c-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f814c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f814c-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f814c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f814c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f814c-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f814c-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f814c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f814c-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f814c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f814c-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f814c-130">Validation File</span></span>  <br/> |<span data-ttu-id="f814c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f814c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f814c-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f814c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="f814c-133">False</span><span class="sxs-lookup"><span data-stu-id="f814c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f814c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f814c-134">See also</span></span>

- [<span data-ttu-id="f814c-135">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f814c-135">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="f814c-136">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f814c-136">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="f814c-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f814c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

