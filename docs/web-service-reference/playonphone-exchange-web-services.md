---
title: PlayOnPhone (Exchange Webdienste)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 486612be-470c-4f99-929a-f2b283e055c1
description: Das PlayOnPhone-Element stellt eine Anforderung zum Lesen eines Elements auf einem Telefon dar.
ms.openlocfilehash: e2c09a67255106ad9afddb86fa19b7a4a5762ee5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466248"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="6ef38-103">PlayOnPhone (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="6ef38-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="6ef38-104">Das **PlayOnPhone** -Element stellt eine Anforderung zum Lesen eines Elements auf einem Telefon dar.</span><span class="sxs-lookup"><span data-stu-id="6ef38-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="6ef38-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="6ef38-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ef38-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6ef38-106">Attributes and elements</span></span>

<span data-ttu-id="6ef38-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6ef38-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ef38-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6ef38-108">Attributes</span></span>

<span data-ttu-id="6ef38-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ef38-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ef38-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ef38-110">Child elements</span></span>

|<span data-ttu-id="6ef38-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ef38-111">**Element**</span></span>|<span data-ttu-id="6ef38-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ef38-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ef38-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="6ef38-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6ef38-114">Stellt den Bezeichner eines Elements dar, das auf einem Telefon wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ef38-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="6ef38-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ef38-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="6ef38-116">Dialtype (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="6ef38-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="6ef38-117">Stellt die Wählzeichenfolge der Telefonnummer dar, die aufgerufen wird, um ein Element per Telefon wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="6ef38-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="6ef38-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ef38-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ef38-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6ef38-119">Parent elements</span></span>

<span data-ttu-id="6ef38-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="6ef38-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ef38-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ef38-121">Remarks</span></span>

<span data-ttu-id="6ef38-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ef38-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ef38-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6ef38-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ef38-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ef38-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ef38-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6ef38-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6ef38-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6ef38-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ef38-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6ef38-127">Validation File</span></span>  <br/> |<span data-ttu-id="6ef38-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ef38-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ef38-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6ef38-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ef38-130">False</span><span class="sxs-lookup"><span data-stu-id="6ef38-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ef38-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ef38-131">See also</span></span>



- [<span data-ttu-id="6ef38-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6ef38-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

