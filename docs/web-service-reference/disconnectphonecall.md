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
description: Das Element DisconnectPhoneCall stellt eine Anforderung an eine Verbindung zu trennen.
ms.openlocfilehash: 56947ea9ba56c76bb02d6a425ff43b3b846a2f60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758021"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="ec966-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="ec966-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="ec966-104">Das Element **DisconnectPhoneCall** stellt eine Anforderung an eine Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="ec966-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="ec966-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="ec966-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec966-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec966-106">Attributes and elements</span></span>

<span data-ttu-id="ec966-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec966-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec966-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec966-108">Attributes</span></span>

<span data-ttu-id="ec966-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec966-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec966-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec966-110">Child elements</span></span>

|<span data-ttu-id="ec966-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec966-111">**Element**</span></span>|<span data-ttu-id="ec966-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec966-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec966-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="ec966-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="ec966-114">Gibt den Bezeichner des Anrufs zu trennen.</span><span class="sxs-lookup"><span data-stu-id="ec966-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="ec966-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec966-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec966-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec966-116">Parent elements</span></span>

<span data-ttu-id="ec966-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec966-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ec966-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec966-118">Text value</span></span>

<span data-ttu-id="ec966-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec966-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec966-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec966-120">Remarks</span></span>

<span data-ttu-id="ec966-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ec966-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec966-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec966-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec966-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec966-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec966-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec966-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ec966-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ec966-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec966-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec966-126">Validation File</span></span>  <br/> |<span data-ttu-id="ec966-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec966-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec966-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec966-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec966-129">False</span><span class="sxs-lookup"><span data-stu-id="ec966-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec966-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec966-130">See also</span></span>

- [<span data-ttu-id="ec966-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec966-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

