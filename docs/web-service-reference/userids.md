---
title: Benutzer-IDs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: Die Benutzer-IDs enthaltenen Element ein Array von delegieren Benutzer erhalten oder aus einem Prinzipal Postfach entfernen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 277ae96fdbc30f1b39ef20553e10ff1de3ff7a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839448"
---
# <a name="userids"></a><span data-ttu-id="39060-104">Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="39060-104">UserIds</span></span>

<span data-ttu-id="39060-105">Das **Benutzer-IDs** -Element enthält ein Array von Benutzer als Stellvertreter zum Abrufen oder aus einem Prinzipal Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="39060-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="39060-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39060-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="39060-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="39060-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39060-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39060-108">Attributes and elements</span></span>

<span data-ttu-id="39060-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39060-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39060-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="39060-110">Attributes</span></span>

<span data-ttu-id="39060-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="39060-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39060-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39060-112">Child elements</span></span>

|<span data-ttu-id="39060-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="39060-113">**Element**</span></span>|<span data-ttu-id="39060-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39060-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39060-115">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="39060-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="39060-116">Identifiziert eine Stellvertretung zum Abrufen oder aus einem Prinzipal Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="39060-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="39060-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39060-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39060-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39060-118">Parent elements</span></span>

|<span data-ttu-id="39060-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="39060-119">**Element**</span></span>|<span data-ttu-id="39060-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39060-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39060-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="39060-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="39060-122">Definiert eine Anforderung zum Abrufen von Informationen zu Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="39060-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="39060-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39060-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39060-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="39060-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="39060-125">Definiert eine Anforderung zum Entfernen von Stellvertretern aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="39060-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="39060-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="39060-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39060-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39060-127">Remarks</span></span>

<span data-ttu-id="39060-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="39060-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39060-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="39060-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39060-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="39060-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39060-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39060-131">Schema Name</span></span>  <br/> |<span data-ttu-id="39060-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="39060-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39060-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39060-133">Validation File</span></span>  <br/> |<span data-ttu-id="39060-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="39060-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39060-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39060-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="39060-136">False</span><span class="sxs-lookup"><span data-stu-id="39060-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39060-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39060-137">See also</span></span>



[<span data-ttu-id="39060-138">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39060-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="39060-139">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39060-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="39060-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="39060-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

