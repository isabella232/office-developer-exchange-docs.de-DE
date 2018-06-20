---
title: ExecutedSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExecutedSearchScope
api_type:
- schema
ms.assetid: 2de5f0ad-43f2-4d38-b520-06540066564e
description: Das ExecutedSearchScope-Element enthält den Umfang der Suche, die ausgeführt wurde, um die Suchergebnisse erhalten.
ms.openlocfilehash: ece9fdfc156cedad2a9fa181897145ae4eea20a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758309"
---
# <a name="executedsearchscope"></a><span data-ttu-id="934fd-103">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="934fd-103">ExecutedSearchScope</span></span>

<span data-ttu-id="934fd-104">Das **ExecutedSearchScope** -Element enthält den Umfang der Suche, die ausgeführt wurde, um die Suchergebnisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="934fd-104">The **ExecutedSearchScope** element contains the scope of the search that was performed to get the search results.</span></span> 
  
```xml
<ExecutedSearchScope/>
```

 <span data-ttu-id="934fd-105">**String**</span><span class="sxs-lookup"><span data-stu-id="934fd-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="934fd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="934fd-106">Attributes and elements</span></span>

<span data-ttu-id="934fd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="934fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="934fd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="934fd-108">Attributes</span></span>

<span data-ttu-id="934fd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="934fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="934fd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="934fd-110">Child elements</span></span>

<span data-ttu-id="934fd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="934fd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="934fd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="934fd-112">Parent elements</span></span>

|<span data-ttu-id="934fd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="934fd-113">**Element**</span></span>|<span data-ttu-id="934fd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="934fd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="934fd-115">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="934fd-115">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="934fd-116">Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="934fd-116">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="934fd-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="934fd-117">Text value</span></span>

<span data-ttu-id="934fd-118">Der Textwert ist optional.</span><span class="sxs-lookup"><span data-stu-id="934fd-118">The text value is optional.</span></span> <span data-ttu-id="934fd-119">Diese Informationen werden von der Clientanwendung verwendet, um die Ergebnisse im cache effektiver.</span><span class="sxs-lookup"><span data-stu-id="934fd-119">This information is used by the client application to cache the results more effectively.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="934fd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="934fd-120">Remarks</span></span>

<span data-ttu-id="934fd-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="934fd-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="934fd-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="934fd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="934fd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="934fd-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="934fd-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="934fd-124">Schema Name</span></span>  <br/> |<span data-ttu-id="934fd-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="934fd-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="934fd-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="934fd-126">Validation File</span></span>  <br/> |<span data-ttu-id="934fd-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="934fd-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="934fd-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="934fd-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="934fd-129">False</span><span class="sxs-lookup"><span data-stu-id="934fd-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="934fd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="934fd-130">See also</span></span>



[<span data-ttu-id="934fd-131">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="934fd-131">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="934fd-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="934fd-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

