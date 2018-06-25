---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: Das PhoneCallState-Element gibt den aktuellen Status für einen Telefonanruf.
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830761"
---
# <a name="phonecallstate"></a><span data-ttu-id="3b178-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="3b178-103">PhoneCallState</span></span>

<span data-ttu-id="3b178-104">Das **PhoneCallState** -Element gibt den aktuellen Status für einen Telefonanruf.</span><span class="sxs-lookup"><span data-stu-id="3b178-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="3b178-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="3b178-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b178-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b178-106">Attributes and elements</span></span>

<span data-ttu-id="3b178-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b178-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b178-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b178-108">Attributes</span></span>

<span data-ttu-id="3b178-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b178-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b178-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b178-110">Child elements</span></span>

<span data-ttu-id="3b178-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b178-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b178-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b178-112">Parent elements</span></span>

|<span data-ttu-id="3b178-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b178-113">**Element**</span></span>|<span data-ttu-id="3b178-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b178-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b178-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="3b178-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="3b178-116">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="3b178-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b178-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3b178-117">Text value</span></span>

<span data-ttu-id="3b178-118">Die folgende Tabelle enthält die möglichen Werte für das **PhoneCallState** -Element.</span><span class="sxs-lookup"><span data-stu-id="3b178-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="3b178-119">**PhoneCallState-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="3b178-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="3b178-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3b178-120">**Value**</span></span>|<span data-ttu-id="3b178-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b178-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b178-122">Im Leerlauf</span><span class="sxs-lookup"><span data-stu-id="3b178-122">Idle</span></span>  <br/> |<span data-ttu-id="3b178-123">Ersten Aufruf Zustand.</span><span class="sxs-lookup"><span data-stu-id="3b178-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="3b178-124">Connecting</span><span class="sxs-lookup"><span data-stu-id="3b178-124">Connecting</span></span>  <br/> |<span data-ttu-id="3b178-125">Das System wird dieses Anrufs einwählen.</span><span class="sxs-lookup"><span data-stu-id="3b178-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="3b178-126">Benachrichtigt</span><span class="sxs-lookup"><span data-stu-id="3b178-126">Alerted</span></span>  <br/> |<span data-ttu-id="3b178-127">Der Anruf wird im Zustand Warnungen (Telefon klingelt).</span><span class="sxs-lookup"><span data-stu-id="3b178-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="3b178-128">Verbunden</span><span class="sxs-lookup"><span data-stu-id="3b178-128">Connected</span></span>  <br/> |<span data-ttu-id="3b178-129">Der Anruf wird in den Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="3b178-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="3b178-130">Verbindung getrennt</span><span class="sxs-lookup"><span data-stu-id="3b178-130">Disconnected</span></span>  <br/> |<span data-ttu-id="3b178-131">Der Anruf wird beendet.</span><span class="sxs-lookup"><span data-stu-id="3b178-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="3b178-132">Eingehend</span><span class="sxs-lookup"><span data-stu-id="3b178-132">Incoming</span></span>  <br/> |<span data-ttu-id="3b178-133">Der Anruf wird eingehende.</span><span class="sxs-lookup"><span data-stu-id="3b178-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="3b178-134">Übertragen von</span><span class="sxs-lookup"><span data-stu-id="3b178-134">Transferring</span></span>  <br/> |<span data-ttu-id="3b178-135">Der Anruf wird an ein anderes Ziel weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3b178-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="3b178-136">Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="3b178-136">Forwarding</span></span>  <br/> |<span data-ttu-id="3b178-137">Der Anruf wird an ein anderes Ziel weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3b178-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b178-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b178-138">Remarks</span></span>

<span data-ttu-id="3b178-139">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /ews/ des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b178-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b178-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3b178-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b178-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b178-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b178-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b178-142">Schema Name</span></span>  <br/> |<span data-ttu-id="3b178-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b178-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b178-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b178-144">Validation File</span></span>  <br/> |<span data-ttu-id="3b178-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b178-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b178-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b178-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b178-147">False</span><span class="sxs-lookup"><span data-stu-id="3b178-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b178-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b178-148">See also</span></span>



- [<span data-ttu-id="3b178-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3b178-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

