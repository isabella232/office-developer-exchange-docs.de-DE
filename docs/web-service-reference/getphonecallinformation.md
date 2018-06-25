---
title: GetPhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 5f4ee71c-bde0-4b0d-b426-0c24dfe67585
description: Das GetPhoneCallInformation-Element gibt eine Anforderung zum Abrufen von Informationen entgegengenommen wurde.
ms.openlocfilehash: 2084a8b5e13b3fa03e0bf62439978bbe81d86ce9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758777"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="b5ca3-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="b5ca3-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="b5ca3-104">Das **GetPhoneCallInformation** -Element gibt eine Anforderung zum Abrufen von Informationen entgegengenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="b5ca3-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="b5ca3-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5ca3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca3-106">Attributes and elements</span></span>

<span data-ttu-id="b5ca3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5ca3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5ca3-108">Attributes</span></span>

<span data-ttu-id="b5ca3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5ca3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca3-110">Child elements</span></span>

|<span data-ttu-id="b5ca3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5ca3-111">**Element**</span></span>|<span data-ttu-id="b5ca3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b5ca3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5ca3-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="b5ca3-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="b5ca3-114">Gibt den Bezeichner eines Telefonanrufs.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5ca3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5ca3-115">Parent elements</span></span>

<span data-ttu-id="b5ca3-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b5ca3-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b5ca3-117">Text value</span></span>

<span data-ttu-id="b5ca3-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5ca3-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5ca3-119">Remarks</span></span>

<span data-ttu-id="b5ca3-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b5ca3-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5ca3-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5ca3-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5ca3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5ca3-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5ca3-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5ca3-123">Schema Name</span></span>  <br/> |<span data-ttu-id="b5ca3-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b5ca3-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b5ca3-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5ca3-125">Validation File</span></span>  <br/> |<span data-ttu-id="b5ca3-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5ca3-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5ca3-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b5ca3-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5ca3-128">False</span><span class="sxs-lookup"><span data-stu-id="b5ca3-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5ca3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5ca3-129">See also</span></span>



- [<span data-ttu-id="b5ca3-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b5ca3-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

