---
title: RemoveDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: f21c5171-62e7-47c8-99b1-22e1ff5883bb
description: Das RemoveDelegate-Element definiert eine Anforderung an die Stellvertretungen aus einem Postfach entfernen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 27618b1767c99b26a5f4c06e97a20e063b598d9d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831085"
---
# <a name="removedelegate"></a><span data-ttu-id="8bc46-104">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="8bc46-104">RemoveDelegate</span></span>

<span data-ttu-id="8bc46-105">Das **RemoveDelegate** -Element definiert eine Anforderung an die Stellvertretungen aus einem Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="8bc46-105">The **RemoveDelegate** element defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="8bc46-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8bc46-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 <span data-ttu-id="8bc46-107">**RemoveDelegateType**</span><span class="sxs-lookup"><span data-stu-id="8bc46-107">**RemoveDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bc46-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8bc46-108">Attributes and elements</span></span>

<span data-ttu-id="8bc46-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8bc46-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bc46-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8bc46-110">Attributes</span></span>

<span data-ttu-id="8bc46-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bc46-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bc46-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bc46-112">Child elements</span></span>

|<span data-ttu-id="8bc46-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8bc46-113">**Element**</span></span>|<span data-ttu-id="8bc46-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8bc46-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8bc46-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="8bc46-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8bc46-116">Identifiziert den Prinzipal Postfach an.</span><span class="sxs-lookup"><span data-stu-id="8bc46-116">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8bc46-117">Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="8bc46-117">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="8bc46-118">Enthält ein Array von Delegaten Benutzer aus einem Prinzipal Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="8bc46-118">Contains an array of delegate users to remove from a principal's mailbox.</span></span> <span data-ttu-id="8bc46-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8bc46-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8bc46-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8bc46-120">Parent elements</span></span>

<span data-ttu-id="8bc46-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="8bc46-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bc46-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bc46-122">Remarks</span></span>

<span data-ttu-id="8bc46-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8bc46-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bc46-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8bc46-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bc46-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bc46-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8bc46-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8bc46-126">Schema Name</span></span>  <br/> |<span data-ttu-id="8bc46-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8bc46-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8bc46-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8bc46-128">Validation File</span></span>  <br/> |<span data-ttu-id="8bc46-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8bc46-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8bc46-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8bc46-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="8bc46-131">False</span><span class="sxs-lookup"><span data-stu-id="8bc46-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bc46-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bc46-132">See also</span></span>



[<span data-ttu-id="8bc46-133">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8bc46-133">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="8bc46-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8bc46-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

