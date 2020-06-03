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
description: Das PhoneCallState-Element gibt den aktuellen Status für einen Telefonanruf an.
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468530"
---
# <a name="phonecallstate"></a><span data-ttu-id="95a21-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="95a21-103">PhoneCallState</span></span>

<span data-ttu-id="95a21-104">Das **PhoneCallState** -Element gibt den aktuellen Status für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="95a21-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="95a21-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="95a21-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95a21-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="95a21-106">Attributes and elements</span></span>

<span data-ttu-id="95a21-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="95a21-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95a21-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="95a21-108">Attributes</span></span>

<span data-ttu-id="95a21-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="95a21-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95a21-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95a21-110">Child elements</span></span>

<span data-ttu-id="95a21-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="95a21-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95a21-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="95a21-112">Parent elements</span></span>

|<span data-ttu-id="95a21-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="95a21-113">**Element**</span></span>|<span data-ttu-id="95a21-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95a21-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95a21-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="95a21-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="95a21-116">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="95a21-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95a21-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="95a21-117">Text value</span></span>

<span data-ttu-id="95a21-118">In der folgenden Tabelle sind die möglichen Werte für das **PhoneCallState** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="95a21-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="95a21-119">**PhoneCallState-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="95a21-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="95a21-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="95a21-120">**Value**</span></span>|<span data-ttu-id="95a21-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95a21-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95a21-122">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="95a21-122">Idle</span></span>  <br/> |<span data-ttu-id="95a21-123">Anfänglicher Anruf Zustand.</span><span class="sxs-lookup"><span data-stu-id="95a21-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="95a21-124">Verbindung wird hergestellt</span><span class="sxs-lookup"><span data-stu-id="95a21-124">Connecting</span></span>  <br/> |<span data-ttu-id="95a21-125">Das System wählt diesen Anruf aus.</span><span class="sxs-lookup"><span data-stu-id="95a21-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="95a21-126">Alarmiert</span><span class="sxs-lookup"><span data-stu-id="95a21-126">Alerted</span></span>  <br/> |<span data-ttu-id="95a21-127">Der Anruf befindet sich im Warnungsstatus (Telefon klingelt).</span><span class="sxs-lookup"><span data-stu-id="95a21-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="95a21-128">Verbunden</span><span class="sxs-lookup"><span data-stu-id="95a21-128">Connected</span></span>  <br/> |<span data-ttu-id="95a21-129">Der Anruf befindet sich im Zustand Connected.</span><span class="sxs-lookup"><span data-stu-id="95a21-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="95a21-130">Disconnected</span><span class="sxs-lookup"><span data-stu-id="95a21-130">Disconnected</span></span>  <br/> |<span data-ttu-id="95a21-131">Der Anruf wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="95a21-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="95a21-132">Eingehende</span><span class="sxs-lookup"><span data-stu-id="95a21-132">Incoming</span></span>  <br/> |<span data-ttu-id="95a21-133">Der Anruf ist eingehend.</span><span class="sxs-lookup"><span data-stu-id="95a21-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="95a21-134">Transfer</span><span class="sxs-lookup"><span data-stu-id="95a21-134">Transferring</span></span>  <br/> |<span data-ttu-id="95a21-135">Der Anruf wird an ein anderes Ziel übertragen.</span><span class="sxs-lookup"><span data-stu-id="95a21-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="95a21-136">Weiterleitungs</span><span class="sxs-lookup"><span data-stu-id="95a21-136">Forwarding</span></span>  <br/> |<span data-ttu-id="95a21-137">Der Anruf wird an ein anderes Ziel weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="95a21-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a21-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95a21-138">Remarks</span></span>

<span data-ttu-id="95a21-139">Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="95a21-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95a21-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="95a21-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95a21-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="95a21-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95a21-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="95a21-142">Schema Name</span></span>  <br/> |<span data-ttu-id="95a21-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="95a21-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="95a21-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="95a21-144">Validation File</span></span>  <br/> |<span data-ttu-id="95a21-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95a21-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95a21-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="95a21-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="95a21-147">False</span><span class="sxs-lookup"><span data-stu-id="95a21-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95a21-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95a21-148">See also</span></span>



- [<span data-ttu-id="95a21-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="95a21-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

