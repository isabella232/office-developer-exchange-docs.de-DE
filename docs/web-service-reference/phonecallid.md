---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: Das PhoneCallId-Element gibt den Bezeichner der eines Telefonanrufs. Dieses Element ist erforderlich.
ms.openlocfilehash: 1886d9510fe254c016779166efccc9882fd77d2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830757"
---
# <a name="phonecallid"></a><span data-ttu-id="df607-104">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="df607-104">PhoneCallId</span></span>

<span data-ttu-id="df607-105">Das **PhoneCallId** -Element gibt den Bezeichner der eines Telefonanrufs.</span><span class="sxs-lookup"><span data-stu-id="df607-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="df607-106">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df607-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="df607-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="df607-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df607-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="df607-108">Attributes and elements</span></span>

<span data-ttu-id="df607-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="df607-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df607-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="df607-110">Attributes</span></span>

|<span data-ttu-id="df607-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="df607-111">**Attribute**</span></span>|<span data-ttu-id="df607-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df607-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df607-113">Id</span><span class="sxs-lookup"><span data-stu-id="df607-113">Id</span></span>  <br/> |<span data-ttu-id="df607-114">Identifiziert den Anruf zu trennen.</span><span class="sxs-lookup"><span data-stu-id="df607-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="df607-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df607-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df607-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df607-116">Child elements</span></span>

<span data-ttu-id="df607-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="df607-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="df607-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df607-118">Parent elements</span></span>

|<span data-ttu-id="df607-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="df607-119">**Element**</span></span>|<span data-ttu-id="df607-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df607-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df607-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="df607-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="df607-122">Stellt eine Anforderung an eine Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="df607-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="df607-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="df607-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="df607-124">Stellt eine Anforderung zum Abrufen von Informationen entgegengenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="df607-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="df607-125">PlayOnPhoneResponse (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="df607-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="df607-126">Definiert eine Antwort auf eine PlayOnPhone an.</span><span class="sxs-lookup"><span data-stu-id="df607-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df607-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df607-127">Remarks</span></span>

<span data-ttu-id="df607-128">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="df607-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df607-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="df607-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df607-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="df607-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="df607-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="df607-131">Schema Name</span></span>  <br/> |<span data-ttu-id="df607-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="df607-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="df607-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="df607-133">Validation File</span></span>  <br/> |<span data-ttu-id="df607-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="df607-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="df607-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="df607-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="df607-136">False</span><span class="sxs-lookup"><span data-stu-id="df607-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df607-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df607-137">See also</span></span>



- [<span data-ttu-id="df607-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="df607-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

