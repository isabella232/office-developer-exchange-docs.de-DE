---
title: AttendeeLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1344a087-88ea-472a-bebf-9b45245592fb
description: Das AttendeeLocation-Element gibt die Position eines Teilnehmers für ein Kalenderelement an.
ms.openlocfilehash: 34a4ee8ea5f4c59cce6eebd8977bd4733f7c7134
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460344"
---
# <a name="attendeelocation"></a><span data-ttu-id="c7c5a-103">AttendeeLocation</span><span class="sxs-lookup"><span data-stu-id="c7c5a-103">AttendeeLocation</span></span>

<span data-ttu-id="c7c5a-104">Das **AttendeeLocation** -Element gibt die Position eines Teilnehmers für ein Kalenderelement an.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-104">The **AttendeeLocation** element specifies the location of an attendee for a calendar item.</span></span> 
  
```XML
<AttendeeLocation></AttendeeLocation>
```

 <span data-ttu-id="c7c5a-105">**xs: Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7c5a-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7c5a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c7c5a-106">Attributes and elements</span></span>

<span data-ttu-id="c7c5a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7c5a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c7c5a-108">Attributes</span></span>

<span data-ttu-id="c7c5a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7c5a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7c5a-110">Child elements</span></span>

<span data-ttu-id="c7c5a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7c5a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7c5a-112">Parent elements</span></span>

|<span data-ttu-id="c7c5a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7c5a-113">**Element**</span></span>|<span data-ttu-id="c7c5a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7c5a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7c5a-115">LocationBasedStateDefinition</span><span class="sxs-lookup"><span data-stu-id="c7c5a-115">LocationBasedStateDefinition</span></span>](locationbasedstatedefinition.md) <br/> |<span data-ttu-id="c7c5a-116">Gibt den Status an, wenn er auf dem Standort basiert.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-116">Specifies the state when it is based on location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7c5a-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c7c5a-117">Text value</span></span>

<span data-ttu-id="c7c5a-118">Der Textwert des AttendeeLocation-Elements ist der attendess-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-118">The text value of the AttendeeLocation element is the attendess location.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7c5a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7c5a-119">Remarks</span></span>

<span data-ttu-id="c7c5a-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c7c5a-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7c5a-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c7c5a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7c5a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7c5a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7c5a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c7c5a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c7c5a-125">Typschema</span><span class="sxs-lookup"><span data-stu-id="c7c5a-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="c7c5a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c7c5a-126">Validation File</span></span>  <br/> |<span data-ttu-id="c7c5a-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c7c5a-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7c5a-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c7c5a-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c7c5a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c5a-129">See also</span></span>

- [<span data-ttu-id="c7c5a-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c7c5a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

