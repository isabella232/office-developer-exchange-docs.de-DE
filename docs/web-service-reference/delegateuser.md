---
title: Beauftragte Benutzer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: Das Element Beauftragte Benutzer identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach oder eine Stellvertretung, die in einer Antwort der Stellvertretung Management zurückgegeben. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 72ddc313a5a76cd0345918cad63b7775ff85026b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757896"
---
# <a name="delegateuser"></a><span data-ttu-id="d404d-104">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="d404d-104">DelegateUser</span></span>

<span data-ttu-id="d404d-105">Das Element **Beauftragte Benutzer** identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach oder eine Stellvertretung, die in einer Antwort der Stellvertretung Management zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d404d-105">The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response.</span></span> <span data-ttu-id="d404d-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

<span data-ttu-id="d404d-107">**DelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="d404d-107">**DelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d404d-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d404d-108">Attributes and elements</span></span>

<span data-ttu-id="d404d-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d404d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d404d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d404d-110">Attributes</span></span>

<span data-ttu-id="d404d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d404d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d404d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d404d-112">Child elements</span></span>

|<span data-ttu-id="d404d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d404d-113">**Element**</span></span>|<span data-ttu-id="d404d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d404d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d404d-115">Benutzer-ID</span><span class="sxs-lookup"><span data-stu-id="d404d-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="d404d-116">Identifiziert den Delegaten.</span><span class="sxs-lookup"><span data-stu-id="d404d-116">Identifies the delegate.</span></span> <span data-ttu-id="d404d-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d404d-118">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="d404d-118">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="d404d-119">Die Ebene Delegaten berechtigungseinstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d404d-119">Contains the delegate permission level settings.</span></span> <span data-ttu-id="d404d-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d404d-121">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="d404d-121">ReceiveCopiesOfMeetingMessages</span></span>](receivecopiesofmeetingmessages.md) <br/> |<span data-ttu-id="d404d-122">Gibt an, ob eine Stellvertretung Kopien der Nachrichten empfängt, die dem Prinzipal adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="d404d-122">Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="d404d-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d404d-124">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="d404d-124">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="d404d-125">Gibt an, ob eine Stellvertretung über die Berechtigung zum Anzeigen von privaten Kalenderelementen in den Prinzipal Postfach verfügt.</span><span class="sxs-lookup"><span data-stu-id="d404d-125">Indicates whether a delegate has permission to view private calendar items in the principal's mailbox.</span></span> <span data-ttu-id="d404d-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d404d-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d404d-127">Parent elements</span></span>

|<span data-ttu-id="d404d-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="d404d-128">**Element**</span></span>|<span data-ttu-id="d404d-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d404d-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d404d-130">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="d404d-130">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="d404d-131">Die Identität der Stellvertretungen hinzufügen oder aktualisieren in einem Postfach enthält.</span><span class="sxs-lookup"><span data-stu-id="d404d-131">Contains the identities of delegates to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d404d-132">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="d404d-132">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="d404d-133">Antwortnachrichten für Verwaltungsvorgänge Stellvertreter enthält.</span><span class="sxs-lookup"><span data-stu-id="d404d-133">Contains response messages for delegate management operations.</span></span> <span data-ttu-id="d404d-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d404d-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d404d-135">Remarks</span></span>

<span data-ttu-id="d404d-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d404d-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d404d-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d404d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d404d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d404d-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d404d-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d404d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d404d-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d404d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="d404d-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d404d-141">Validation File</span></span>  <br/> |<span data-ttu-id="d404d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d404d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d404d-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d404d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d404d-144">False</span><span class="sxs-lookup"><span data-stu-id="d404d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d404d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d404d-145">See also</span></span>

- [<span data-ttu-id="d404d-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d404d-146">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="d404d-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d404d-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="d404d-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d404d-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d404d-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="d404d-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

