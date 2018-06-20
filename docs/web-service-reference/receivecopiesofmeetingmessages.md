---
title: ReceiveCopiesOfMeetingMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: Das ReceiveCopiesOfMeetingMessages-Element gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e39a5d3255268b418fa956959da5ae0ea062d831
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830967"
---
# <a name="receivecopiesofmeetingmessages"></a><span data-ttu-id="c5a71-104">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="c5a71-104">ReceiveCopiesOfMeetingMessages</span></span>

<span data-ttu-id="c5a71-105">Das **ReceiveCopiesOfMeetingMessages** -Element gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="c5a71-105">The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="c5a71-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c5a71-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
```

 <span data-ttu-id="c5a71-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c5a71-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5a71-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5a71-108">Attributes and elements</span></span>

<span data-ttu-id="c5a71-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5a71-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5a71-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5a71-110">Attributes</span></span>

<span data-ttu-id="c5a71-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5a71-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5a71-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5a71-112">Child elements</span></span>

<span data-ttu-id="c5a71-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5a71-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5a71-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5a71-114">Parent elements</span></span>

|<span data-ttu-id="c5a71-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5a71-115">**Element**</span></span>|<span data-ttu-id="c5a71-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5a71-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5a71-117">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="c5a71-117">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="c5a71-118">Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="c5a71-118">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="c5a71-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c5a71-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5a71-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="c5a71-120">Text value</span></span>

<span data-ttu-id="c5a71-121">Der Textwert **true** gibt an, dass eine Stellvertretung eine Kopie des meeting-Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="c5a71-121">A text value of **true** indicates that a delegate receives a copy of meeting messages.</span></span> <span data-ttu-id="c5a71-122">Der Textwert **false** gibt an, dass eine Stellvertretung keine Kopie der Besprechung Nachrichten erhält.</span><span class="sxs-lookup"><span data-stu-id="c5a71-122">A text value of **false** indicates that a delegate does not receive a copy of meeting messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c5a71-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5a71-123">Remarks</span></span>

<span data-ttu-id="c5a71-124">**ReceiveCopiesOfMeetingMessages** auf **false**festgelegt ist, die Stellvertretung kann weiterhin Senden im Auftrag der Prinzipal, aber erhalten keine Fehlermeldungen bezüglich Besprechungen.</span><span class="sxs-lookup"><span data-stu-id="c5a71-124">When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.</span></span>
  
<span data-ttu-id="c5a71-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c5a71-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5a71-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c5a71-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5a71-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5a71-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5a71-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5a71-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c5a71-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c5a71-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5a71-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5a71-130">Validation File</span></span>  <br/> |<span data-ttu-id="c5a71-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5a71-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5a71-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c5a71-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c5a71-133">False</span><span class="sxs-lookup"><span data-stu-id="c5a71-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5a71-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5a71-134">See also</span></span>



[<span data-ttu-id="c5a71-135">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c5a71-135">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="c5a71-136">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c5a71-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="c5a71-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c5a71-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c5a71-138">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="c5a71-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

