---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: Das PhoneCallInformation-Element gibt die Zustandsinformationen für einen Telefonanruf an.
ms.openlocfilehash: 75370bccb841818a8302bdd055ad96fd16b2e8df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468845"
---
# <a name="phonecallinformation"></a><span data-ttu-id="9fd4f-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="9fd4f-103">PhoneCallInformation</span></span>

<span data-ttu-id="9fd4f-104">Das **PhoneCallInformation** -Element gibt die Zustandsinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="9fd4f-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="9fd4f-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fd4f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fd4f-106">Attributes and elements</span></span>

<span data-ttu-id="9fd4f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fd4f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fd4f-108">Attributes</span></span>

<span data-ttu-id="9fd4f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fd4f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fd4f-110">Child elements</span></span>

|<span data-ttu-id="9fd4f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fd4f-111">**Element**</span></span>|<span data-ttu-id="9fd4f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fd4f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fd4f-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="9fd4f-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="9fd4f-114">Gibt den Status für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="9fd4f-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="9fd4f-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="9fd4f-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="9fd4f-117">Gibt die Ursache eines Verbindungsfehlers an.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="9fd4f-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="9fd4f-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="9fd4f-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="9fd4f-120">Gibt den SIP-Antworttext an.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-120">Specifies the SIP response text.</span></span> <span data-ttu-id="9fd4f-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9fd4f-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="9fd4f-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="9fd4f-123">Gibt den SIP-Antwortcode an.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-123">Specifies the SIP response code.</span></span> <span data-ttu-id="9fd4f-124">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9fd4f-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fd4f-125">Parent elements</span></span>

|<span data-ttu-id="9fd4f-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fd4f-126">**Element**</span></span>|<span data-ttu-id="9fd4f-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fd4f-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fd4f-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="9fd4f-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="9fd4f-129">Definiert eine Antwort auf eine [GetPhoneCallInformation-Vorgangs](getphonecallinformation-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fd4f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fd4f-130">Remarks</span></span>

<span data-ttu-id="9fd4f-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9fd4f-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fd4f-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9fd4f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fd4f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fd4f-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fd4f-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fd4f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="9fd4f-135">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9fd4f-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fd4f-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fd4f-136">Validation File</span></span>  <br/> |<span data-ttu-id="9fd4f-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9fd4f-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fd4f-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fd4f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fd4f-139">False</span><span class="sxs-lookup"><span data-stu-id="9fd4f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fd4f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fd4f-140">See also</span></span>



- [<span data-ttu-id="9fd4f-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fd4f-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

