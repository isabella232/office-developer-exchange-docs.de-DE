---
title: ProposeNewTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6d5977ac-484e-4e53-92ba-58a868eb3395
description: Das ProposeNewTime-Element gibt eine Antwortobjekt, der angibt, dass der Besprechungsteilnehmer eine neue Besprechungszeit vorschlagen kann.
ms.openlocfilehash: 4a0238d94b29993def8009fae62380bb2c02e8b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830904"
---
# <a name="proposenewtime"></a><span data-ttu-id="21871-103">ProposeNewTime</span><span class="sxs-lookup"><span data-stu-id="21871-103">ProposeNewTime</span></span>

<span data-ttu-id="21871-104">Das **ProposeNewTime** -Element gibt eine Antwortobjekt, der angibt, dass der Besprechungsteilnehmer eine neue Besprechungszeit vorschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="21871-104">The **ProposeNewTime** element specifies a response object that indicates that the meeting attendee can propose a new meeting time.</span></span> 
  
```XML
<ProposeNewTime ObjectName=""></ProposeNewTime>
```

 <span data-ttu-id="21871-105">**ProposeNewTimeType**</span><span class="sxs-lookup"><span data-stu-id="21871-105">**ProposeNewTimeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21871-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21871-106">Attributes and elements</span></span>

<span data-ttu-id="21871-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21871-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21871-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="21871-108">Attributes</span></span>

****

|<span data-ttu-id="21871-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="21871-109">**Attribute**</span></span>|<span data-ttu-id="21871-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21871-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21871-111">Objektname</span><span class="sxs-lookup"><span data-stu-id="21871-111">ObjectName</span></span>  <br/> |<span data-ttu-id="21871-112">Der Name der im Response-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21871-112">The name of the response object.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21871-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21871-113">Child elements</span></span>

<span data-ttu-id="21871-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="21871-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21871-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21871-115">Parent elements</span></span>

[<span data-ttu-id="21871-116">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="21871-116">ResponseObjects</span></span>](responseobjects.md)
  
## <a name="remarks"></a><span data-ttu-id="21871-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21871-117">Remarks</span></span>

<span data-ttu-id="21871-118">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="21871-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="21871-119">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="21871-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21871-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="21871-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21871-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="21871-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21871-122">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21871-122">Schema Name</span></span>  <br/> |<span data-ttu-id="21871-123">Schematypen</span><span class="sxs-lookup"><span data-stu-id="21871-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="21871-124">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21871-124">Validation File</span></span>  <br/> |<span data-ttu-id="21871-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21871-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21871-126">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="21871-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="21871-127">True</span><span class="sxs-lookup"><span data-stu-id="21871-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21871-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21871-128">See also</span></span>



[<span data-ttu-id="21871-129">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="21871-129">ResponseObjects</span></span>](responseobjects.md)


- [<span data-ttu-id="21871-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="21871-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

