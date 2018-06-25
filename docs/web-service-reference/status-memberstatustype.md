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
description: Status-Element enthält Informationen über den Status der Verteilung Listenmitglieder auf dem Server.
ms.openlocfilehash: ef062433c80f0cca413c33012e1164b17e226faf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831580"
---
# <a name="status-memberstatustype"></a><span data-ttu-id="26b7a-103">Status (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="26b7a-103">Status (MemberStatusType)</span></span>

<span data-ttu-id="26b7a-104">**Status** -Element enthält Informationen über den Status der Verteilung Listenmitglieder auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="26b7a-104">The **Status** element provides information about the status of a distribution list member on the server.</span></span> 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 <span data-ttu-id="26b7a-105">**MemberStatusType**</span><span class="sxs-lookup"><span data-stu-id="26b7a-105">**MemberStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26b7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26b7a-106">Attributes and elements</span></span>

<span data-ttu-id="26b7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="26b7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26b7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="26b7a-108">Attributes</span></span>

<span data-ttu-id="26b7a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="26b7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26b7a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26b7a-110">Child elements</span></span>

<span data-ttu-id="26b7a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="26b7a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26b7a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26b7a-112">Parent elements</span></span>

|<span data-ttu-id="26b7a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26b7a-113">**Element**</span></span>|<span data-ttu-id="26b7a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26b7a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26b7a-115">Member</span><span class="sxs-lookup"><span data-stu-id="26b7a-115">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="26b7a-116">Stellt ein Element einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="26b7a-116">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26b7a-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="26b7a-117">Text value</span></span>

<span data-ttu-id="26b7a-118">Die folgende Tabelle enthält die möglichen Werte für die **Status** -Element.</span><span class="sxs-lookup"><span data-stu-id="26b7a-118">The following table lists the possible values for the **Status** element.</span></span> 
  
<span data-ttu-id="26b7a-119">**Status-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="26b7a-119">**Status element values**</span></span>

|<span data-ttu-id="26b7a-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="26b7a-120">**Value**</span></span>|<span data-ttu-id="26b7a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26b7a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26b7a-122">Unbekannte</span><span class="sxs-lookup"><span data-stu-id="26b7a-122">Unrecognized</span></span>  <br/> |<span data-ttu-id="26b7a-123">Informationen zu Mitgliedern ist ungültig oder nicht erkannte.</span><span class="sxs-lookup"><span data-stu-id="26b7a-123">Member information is invalid or unrecognized.</span></span>  <br/> |
|<span data-ttu-id="26b7a-124">Standard</span><span class="sxs-lookup"><span data-stu-id="26b7a-124">Normal</span></span>  <br/> |<span data-ttu-id="26b7a-125">Memberinformationen in einer Verteilerliste ist Synchronisierung mit dem Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="26b7a-125">Member information in a distribution list is in sync with the referenced object.</span></span>  <br/> |
|<span data-ttu-id="26b7a-126">Tiefer gestuft</span><span class="sxs-lookup"><span data-stu-id="26b7a-126">Demoted</span></span>  <br/> |<span data-ttu-id="26b7a-127">Das Objekt verwiesen wird, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26b7a-127">Referenced object is not available.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26b7a-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26b7a-128">Remarks</span></span>

<span data-ttu-id="26b7a-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="26b7a-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26b7a-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="26b7a-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26b7a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="26b7a-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26b7a-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26b7a-132">Schema Name</span></span>  <br/> |<span data-ttu-id="26b7a-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="26b7a-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="26b7a-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26b7a-134">Validation File</span></span>  <br/> |<span data-ttu-id="26b7a-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26b7a-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26b7a-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26b7a-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="26b7a-137">False</span><span class="sxs-lookup"><span data-stu-id="26b7a-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26b7a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26b7a-138">See also</span></span>



- [<span data-ttu-id="26b7a-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="26b7a-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

