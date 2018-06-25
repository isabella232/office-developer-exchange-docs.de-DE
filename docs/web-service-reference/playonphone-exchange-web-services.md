---
title: PlayOnPhone (Exchange Web Services)
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
description: Das PlayOnPhone-Element eine Anforderung darstellt, auf einem Telefon ein Element gelesen.
ms.openlocfilehash: 75493a31940ea609fd6cf454e91ca5881fb7e678
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830816"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="4ff58-103">PlayOnPhone (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="4ff58-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="4ff58-104">Das **PlayOnPhone** -Element eine Anforderung darstellt, auf einem Telefon ein Element gelesen.</span><span class="sxs-lookup"><span data-stu-id="4ff58-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="4ff58-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="4ff58-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ff58-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ff58-106">Attributes and elements</span></span>

<span data-ttu-id="4ff58-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ff58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ff58-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ff58-108">Attributes</span></span>

<span data-ttu-id="4ff58-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ff58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ff58-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ff58-110">Child elements</span></span>

|<span data-ttu-id="4ff58-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ff58-111">**Element**</span></span>|<span data-ttu-id="4ff58-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ff58-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ff58-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="4ff58-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4ff58-114">Stellt die ID eines Elements auf einem Telefon wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="4ff58-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="4ff58-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ff58-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="4ff58-116">DialString (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="4ff58-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="4ff58-117">Stellt die Wählzeichenfolge der Telefonnummer an, die aufgerufen wird, um die Wiedergabe eines Elements per Telefon.</span><span class="sxs-lookup"><span data-stu-id="4ff58-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="4ff58-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ff58-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ff58-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ff58-119">Parent elements</span></span>

<span data-ttu-id="4ff58-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ff58-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ff58-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ff58-121">Remarks</span></span>

<span data-ttu-id="4ff58-122">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ff58-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ff58-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ff58-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ff58-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ff58-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4ff58-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ff58-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4ff58-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4ff58-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4ff58-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ff58-127">Validation File</span></span>  <br/> |<span data-ttu-id="4ff58-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4ff58-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4ff58-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ff58-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ff58-130">False</span><span class="sxs-lookup"><span data-stu-id="4ff58-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ff58-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ff58-131">See also</span></span>



- [<span data-ttu-id="4ff58-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ff58-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

