---
title: EndWallClock
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc04e44e-e6d1-4355-a2b1-feb6663dc647
description: Das EndWallClock-Element gibt die Endzeit der Besprechung in der Zeitzone des Speicherorts, in dem die Besprechung stattfindet.
ms.openlocfilehash: 10e4a2bde50354b2f2752751c01a6a70aa084d05
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758240"
---
# <a name="endwallclock"></a><span data-ttu-id="22caf-103">EndWallClock</span><span class="sxs-lookup"><span data-stu-id="22caf-103">EndWallClock</span></span>

<span data-ttu-id="22caf-104">Das **EndWallClock** -Element gibt die Endzeit der Besprechung in der Zeitzone des Speicherorts, in dem die Besprechung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="22caf-104">The **EndWallClock** element specifies the end time of a meeting in the time zone of the location in which the meeting takes place.</span></span> 
  
```XML
<EndWallClock></EndWallClock>
```

 <span data-ttu-id="22caf-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="22caf-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22caf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="22caf-106">Attributes and elements</span></span>

<span data-ttu-id="22caf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="22caf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22caf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="22caf-108">Attributes</span></span>

<span data-ttu-id="22caf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="22caf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22caf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22caf-110">Child elements</span></span>

<span data-ttu-id="22caf-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="22caf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22caf-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22caf-112">Parent elements</span></span>

|<span data-ttu-id="22caf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="22caf-113">**Element**</span></span>|<span data-ttu-id="22caf-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22caf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22caf-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="22caf-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="22caf-116">Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22caf-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22caf-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="22caf-117">Text value</span></span>

<span data-ttu-id="22caf-118">Der Textwert der **EndWallClock** -Element ist ein Zeichenfolgenwert, der Bezeichner der Zeitzone angibt.</span><span class="sxs-lookup"><span data-stu-id="22caf-118">The text value of the **EndWallClock** element is a string value that specifies the time zone identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="22caf-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22caf-119">Remarks</span></span>

<span data-ttu-id="22caf-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="22caf-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="22caf-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="22caf-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22caf-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="22caf-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22caf-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="22caf-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22caf-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="22caf-124">Schema Name</span></span>  <br/> |<span data-ttu-id="22caf-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="22caf-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="22caf-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="22caf-126">Validation File</span></span>  <br/> |<span data-ttu-id="22caf-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22caf-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="22caf-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="22caf-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="22caf-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22caf-129">See also</span></span>



- [<span data-ttu-id="22caf-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="22caf-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

