---
title: DisconnectPhoneCall
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCall
api_type:
- schema
ms.assetid: f9252536-9852-4dd9-9ebc-91f5cf281171
description: Das DisconnectPhoneCall-Element stellt eine Anforderung zum Trennen eines Anrufs dar.
ms.openlocfilehash: 8d64ecb9dce1d8b7efcebc70686db8fcbf867217
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529707"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="4ec7a-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="4ec7a-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="4ec7a-104">Das **DisconnectPhoneCall** -Element stellt eine Anforderung zum Trennen eines Anrufs dar.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="4ec7a-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="4ec7a-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ec7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec7a-106">Attributes and elements</span></span>

<span data-ttu-id="4ec7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ec7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ec7a-108">Attributes</span></span>

<span data-ttu-id="4ec7a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ec7a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec7a-110">Child elements</span></span>

|<span data-ttu-id="4ec7a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ec7a-111">**Element**</span></span>|<span data-ttu-id="4ec7a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ec7a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec7a-113">Anrufer</span><span class="sxs-lookup"><span data-stu-id="4ec7a-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="4ec7a-114">Gibt den Bezeichner des Anrufs an, der getrennt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="4ec7a-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ec7a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ec7a-116">Parent elements</span></span>

<span data-ttu-id="4ec7a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4ec7a-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="4ec7a-118">Text value</span></span>

<span data-ttu-id="4ec7a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ec7a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ec7a-120">Remarks</span></span>

<span data-ttu-id="4ec7a-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4ec7a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ec7a-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4ec7a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ec7a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ec7a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ec7a-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ec7a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4ec7a-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4ec7a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ec7a-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ec7a-126">Validation File</span></span>  <br/> |<span data-ttu-id="4ec7a-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4ec7a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ec7a-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ec7a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ec7a-129">False</span><span class="sxs-lookup"><span data-stu-id="4ec7a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ec7a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ec7a-130">See also</span></span>

- [<span data-ttu-id="4ec7a-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ec7a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

