---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: Das UpdateDelegate-Element definiert eine Anforderung zum Aktualisieren von Delegaten in einem Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 32322e48acfa5f1058786162565a185a3e565d6e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839342"
---
# <a name="updatedelegate"></a><span data-ttu-id="adf6e-104">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="adf6e-104">UpdateDelegate</span></span>

<span data-ttu-id="adf6e-105">Das **UpdateDelegate** -Element definiert eine Anforderung zum Aktualisieren von Delegaten in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="adf6e-105">The **UpdateDelegate** element defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="adf6e-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="adf6e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 <span data-ttu-id="adf6e-107">**UpdateDelegateType**</span><span class="sxs-lookup"><span data-stu-id="adf6e-107">**UpdateDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="adf6e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="adf6e-108">Attributes and elements</span></span>

<span data-ttu-id="adf6e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="adf6e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="adf6e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="adf6e-110">Attributes</span></span>

<span data-ttu-id="adf6e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="adf6e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="adf6e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="adf6e-112">Child elements</span></span>

|<span data-ttu-id="adf6e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="adf6e-113">**Element**</span></span>|<span data-ttu-id="adf6e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="adf6e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="adf6e-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="adf6e-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="adf6e-116">Enthält ein Array der [Beauftragte Benutzer](delegateuser.md) Elemente, mit denen die Stellvertretungen und die Updates auf die Stellvertretungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="adf6e-116">Contains an array of [DelegateUser](delegateuser.md) elements that identify the delegates and the updates to apply to the delegates.</span></span> <span data-ttu-id="adf6e-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="adf6e-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="adf6e-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="adf6e-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="adf6e-119">Definiert, wie Besprechungsanfragen zwischen den Delegaten und dem Prinzipalnamen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="adf6e-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="adf6e-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="adf6e-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="adf6e-121">Postfach</span><span class="sxs-lookup"><span data-stu-id="adf6e-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="adf6e-122">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="adf6e-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="adf6e-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="adf6e-123">Parent elements</span></span>

<span data-ttu-id="adf6e-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="adf6e-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="adf6e-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="adf6e-125">Remarks</span></span>

<span data-ttu-id="adf6e-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="adf6e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="adf6e-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="adf6e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adf6e-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="adf6e-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="adf6e-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="adf6e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="adf6e-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="adf6e-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="adf6e-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="adf6e-131">Validation File</span></span>  <br/> |<span data-ttu-id="adf6e-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="adf6e-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="adf6e-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="adf6e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="adf6e-134">False</span><span class="sxs-lookup"><span data-stu-id="adf6e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="adf6e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adf6e-135">See also</span></span>



[<span data-ttu-id="adf6e-136">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="adf6e-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="adf6e-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="adf6e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

