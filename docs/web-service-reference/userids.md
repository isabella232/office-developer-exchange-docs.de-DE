---
title: UserIds
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
description: Das userids-Element enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen oder daraus entfernt werden sollen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: de4661226c154ef0d2d5ac55c57405e20c4d2aee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459777"
---
# <a name="userids"></a><span data-ttu-id="30b04-104">UserIds</span><span class="sxs-lookup"><span data-stu-id="30b04-104">UserIds</span></span>

<span data-ttu-id="30b04-105">Das **userids** -Element enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen oder daraus entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30b04-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="30b04-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="30b04-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="30b04-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="30b04-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30b04-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="30b04-108">Attributes and elements</span></span>

<span data-ttu-id="30b04-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="30b04-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30b04-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="30b04-110">Attributes</span></span>

<span data-ttu-id="30b04-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="30b04-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30b04-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30b04-112">Child elements</span></span>

|<span data-ttu-id="30b04-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="30b04-113">**Element**</span></span>|<span data-ttu-id="30b04-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30b04-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30b04-115">UserId</span><span class="sxs-lookup"><span data-stu-id="30b04-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="30b04-116">Bezeichnet einen Delegaten, der aus dem Postfach eines Prinzipals abgerufen oder daraus entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30b04-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="30b04-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="30b04-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="30b04-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="30b04-118">Parent elements</span></span>

|<span data-ttu-id="30b04-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="30b04-119">**Element**</span></span>|<span data-ttu-id="30b04-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30b04-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30b04-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="30b04-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="30b04-122">Definiert eine Anforderung zum Abrufen von Informationen zu Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="30b04-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="30b04-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="30b04-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="30b04-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="30b04-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="30b04-125">Definiert eine Anforderung zum Entfernen von Stellvertretern aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="30b04-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="30b04-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="30b04-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30b04-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30b04-127">Remarks</span></span>

<span data-ttu-id="30b04-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="30b04-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30b04-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="30b04-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b04-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="30b04-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="30b04-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="30b04-131">Schema Name</span></span>  <br/> |<span data-ttu-id="30b04-132">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="30b04-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="30b04-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="30b04-133">Validation File</span></span>  <br/> |<span data-ttu-id="30b04-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="30b04-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="30b04-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="30b04-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="30b04-136">False</span><span class="sxs-lookup"><span data-stu-id="30b04-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30b04-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30b04-137">See also</span></span>



[<span data-ttu-id="30b04-138">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30b04-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="30b04-139">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30b04-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="30b04-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="30b04-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

