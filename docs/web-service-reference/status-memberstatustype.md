---
title: Status (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: Das Status-Element enthält Informationen zum Status eines Verteilerlisten Elements auf dem Server.
ms.openlocfilehash: bfa0c349d6af51c1b2238c9749d2656541d31906
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465464"
---
# <a name="status-memberstatustype"></a><span data-ttu-id="1ad4c-103">Status (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="1ad4c-103">Status (MemberStatusType)</span></span>

<span data-ttu-id="1ad4c-104">Das **Status** -Element enthält Informationen zum Status eines Verteilerlisten Elements auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-104">The **Status** element provides information about the status of a distribution list member on the server.</span></span> 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 <span data-ttu-id="1ad4c-105">**MemberStatusType**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-105">**MemberStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ad4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ad4c-106">Attributes and elements</span></span>

<span data-ttu-id="1ad4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ad4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ad4c-108">Attributes</span></span>

<span data-ttu-id="1ad4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ad4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ad4c-110">Child elements</span></span>

<span data-ttu-id="1ad4c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ad4c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ad4c-112">Parent elements</span></span>

|<span data-ttu-id="1ad4c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-113">**Element**</span></span>|<span data-ttu-id="1ad4c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ad4c-115">Member</span><span class="sxs-lookup"><span data-stu-id="1ad4c-115">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1ad4c-116">Stellt ein Element einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-116">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ad4c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1ad4c-117">Text value</span></span>

<span data-ttu-id="1ad4c-118">In der folgenden Tabelle sind die möglichen Werte für das **Status** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-118">The following table lists the possible values for the **Status** element.</span></span> 
  
<span data-ttu-id="1ad4c-119">**Status-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-119">**Status element values**</span></span>

|<span data-ttu-id="1ad4c-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-120">**Value**</span></span>|<span data-ttu-id="1ad4c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ad4c-122">Unbekannte</span><span class="sxs-lookup"><span data-stu-id="1ad4c-122">Unrecognized</span></span>  <br/> |<span data-ttu-id="1ad4c-123">Mitgliedsinformationen sind ungültig oder nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-123">Member information is invalid or unrecognized.</span></span>  <br/> |
|<span data-ttu-id="1ad4c-124">Normal</span><span class="sxs-lookup"><span data-stu-id="1ad4c-124">Normal</span></span>  <br/> |<span data-ttu-id="1ad4c-125">Elementinformationen in einer Verteilerliste werden mit dem referenzierten Objekt synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-125">Member information in a distribution list is in sync with the referenced object.</span></span>  <br/> |
|<span data-ttu-id="1ad4c-126">Herabgestufte</span><span class="sxs-lookup"><span data-stu-id="1ad4c-126">Demoted</span></span>  <br/> |<span data-ttu-id="1ad4c-127">Das Objekt, auf das verwiesen wird, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-127">Referenced object is not available.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ad4c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ad4c-128">Remarks</span></span>

<span data-ttu-id="1ad4c-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ad4c-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1ad4c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad4c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ad4c-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ad4c-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ad4c-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1ad4c-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1ad4c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ad4c-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ad4c-134">Validation File</span></span>  <br/> |<span data-ttu-id="1ad4c-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ad4c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ad4c-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ad4c-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ad4c-137">False</span><span class="sxs-lookup"><span data-stu-id="1ad4c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ad4c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ad4c-138">See also</span></span>



- [<span data-ttu-id="1ad4c-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ad4c-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

