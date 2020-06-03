---
title: Anrufer
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
description: Das Anruf-ID-Element gibt den Bezeichner eines Telefonanrufs an. Dieses Element ist erforderlich.
ms.openlocfilehash: 3e4b9dba5e8be6e45a0c16508531fbc6cf91c170
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459700"
---
# <a name="phonecallid"></a><span data-ttu-id="fa164-104">Anrufer</span><span class="sxs-lookup"><span data-stu-id="fa164-104">PhoneCallId</span></span>

<span data-ttu-id="fa164-105">Das **Anruf** -ID-Element gibt den Bezeichner eines Telefonanrufs an.</span><span class="sxs-lookup"><span data-stu-id="fa164-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="fa164-106">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa164-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="fa164-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="fa164-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa164-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa164-108">Attributes and elements</span></span>

<span data-ttu-id="fa164-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa164-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa164-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa164-110">Attributes</span></span>

|<span data-ttu-id="fa164-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fa164-111">**Attribute**</span></span>|<span data-ttu-id="fa164-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa164-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa164-113">Id</span><span class="sxs-lookup"><span data-stu-id="fa164-113">Id</span></span>  <br/> |<span data-ttu-id="fa164-114">Gibt den Telefonanruf an, der getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa164-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="fa164-115">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa164-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fa164-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa164-116">Child elements</span></span>

<span data-ttu-id="fa164-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa164-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa164-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa164-118">Parent elements</span></span>

|<span data-ttu-id="fa164-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa164-119">**Element**</span></span>|<span data-ttu-id="fa164-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa164-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa164-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="fa164-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="fa164-122">Stellt eine Anforderung zum Trennen eines Anrufs dar.</span><span class="sxs-lookup"><span data-stu-id="fa164-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="fa164-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="fa164-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="fa164-124">Stellt eine Anforderung zum Abrufen von Telefonanruf Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="fa164-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="fa164-125">PlayOnPhoneResponse (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="fa164-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="fa164-126">Definiert eine Antwort auf eine PlayOnPhone-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fa164-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa164-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa164-127">Remarks</span></span>

<span data-ttu-id="fa164-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fa164-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa164-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fa164-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa164-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa164-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa164-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa164-131">Schema Name</span></span>  <br/> |<span data-ttu-id="fa164-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fa164-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fa164-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa164-133">Validation File</span></span>  <br/> |<span data-ttu-id="fa164-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fa164-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa164-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fa164-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa164-136">False</span><span class="sxs-lookup"><span data-stu-id="fa164-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa164-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa164-137">See also</span></span>



- [<span data-ttu-id="fa164-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fa164-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

