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
description: Das GetPhoneCallInformation-Element gibt eine Anforderung zum Abrufen von Telefonanruf Informationen an.
ms.openlocfilehash: b835cd301b1c243e88034d1057026ef1305b9038
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530197"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="6ee6f-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="6ee6f-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="6ee6f-104">Das **GetPhoneCallInformation** -Element gibt eine Anforderung zum Abrufen von Telefonanruf Informationen an.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="6ee6f-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="6ee6f-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ee6f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ee6f-106">Attributes and elements</span></span>

<span data-ttu-id="6ee6f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ee6f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ee6f-108">Attributes</span></span>

<span data-ttu-id="6ee6f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ee6f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ee6f-110">Child elements</span></span>

|<span data-ttu-id="6ee6f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ee6f-111">**Element**</span></span>|<span data-ttu-id="6ee6f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ee6f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ee6f-113">Anrufer</span><span class="sxs-lookup"><span data-stu-id="6ee6f-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="6ee6f-114">Gibt den Bezeichner eines Telefonanrufs an.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ee6f-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ee6f-115">Parent elements</span></span>

<span data-ttu-id="6ee6f-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6ee6f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6ee6f-117">Text value</span></span>

<span data-ttu-id="6ee6f-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ee6f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ee6f-119">Remarks</span></span>

<span data-ttu-id="6ee6f-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6ee6f-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ee6f-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6ee6f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ee6f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ee6f-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ee6f-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ee6f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="6ee6f-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6ee6f-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ee6f-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ee6f-125">Validation File</span></span>  <br/> |<span data-ttu-id="6ee6f-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ee6f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ee6f-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6ee6f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ee6f-128">False</span><span class="sxs-lookup"><span data-stu-id="6ee6f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ee6f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ee6f-129">See also</span></span>



- [<span data-ttu-id="6ee6f-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6ee6f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

