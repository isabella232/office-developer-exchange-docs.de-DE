---
title: AddDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 646fb994-229e-4d90-8b95-6541191cb3ae
description: Das AddDelegate-Element definiert eine Anforderung an ein Postfach Stellvertretungen hinzugefügt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: d1cb0ff3ea68904bf88e346f68afe7c349ae4394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757226"
---
# <a name="adddelegate"></a><span data-ttu-id="019ac-104">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="019ac-104">AddDelegate</span></span>

<span data-ttu-id="019ac-105">Das **AddDelegate** -Element definiert eine Anforderung an ein Postfach Stellvertretungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="019ac-105">The **AddDelegate** element defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="019ac-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="019ac-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 <span data-ttu-id="019ac-107">**AddDelegateType**</span><span class="sxs-lookup"><span data-stu-id="019ac-107">**AddDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="019ac-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="019ac-108">Attributes and elements</span></span>

<span data-ttu-id="019ac-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="019ac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="019ac-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="019ac-110">Attributes</span></span>

<span data-ttu-id="019ac-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="019ac-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="019ac-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="019ac-112">Child elements</span></span>

|<span data-ttu-id="019ac-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="019ac-113">**Element**</span></span>|<span data-ttu-id="019ac-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="019ac-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="019ac-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="019ac-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="019ac-116">Enthält die Identitäten von Delegaten zum Hinzufügen oder aktualisieren in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="019ac-116">Contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="019ac-117">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="019ac-117">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="019ac-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="019ac-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="019ac-119">Definiert, wie Besprechungsanfragen zwischen den Delegaten und dem Prinzipalnamen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="019ac-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="019ac-120">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="019ac-120">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="019ac-121">Postfach</span><span class="sxs-lookup"><span data-stu-id="019ac-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="019ac-122">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="019ac-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="019ac-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="019ac-123">Parent elements</span></span>

<span data-ttu-id="019ac-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="019ac-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="019ac-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="019ac-125">Remarks</span></span>

<span data-ttu-id="019ac-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="019ac-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="019ac-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="019ac-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="019ac-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="019ac-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="019ac-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="019ac-129">Schema Name</span></span>  <br/> |<span data-ttu-id="019ac-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="019ac-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="019ac-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="019ac-131">Validation File</span></span>  <br/> |<span data-ttu-id="019ac-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="019ac-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="019ac-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="019ac-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="019ac-134">False</span><span class="sxs-lookup"><span data-stu-id="019ac-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="019ac-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="019ac-135">See also</span></span>

- [<span data-ttu-id="019ac-136">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="019ac-136">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="019ac-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="019ac-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="019ac-138">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="019ac-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)
