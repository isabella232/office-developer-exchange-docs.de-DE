---
title: DelegateUser
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
description: Das DelegateUser-Element identifiziert einen einzelnen Delegaten, der in einem Postfach oder einer Stellvertretung, die in einer Delegate-Verwaltungs Antwort zurückgegeben wird, hinzugefügt oder aktualisiert werden soll. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 40d9dacbd544436a3edf3213cf078cd33f961a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458803"
---
# <a name="delegateuser"></a><span data-ttu-id="0d4ee-104">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="0d4ee-104">DelegateUser</span></span>

<span data-ttu-id="0d4ee-105">Das **DelegateUser** -Element identifiziert einen einzelnen Delegaten, der in einem Postfach oder einer Stellvertretung, die in einer Delegate-Verwaltungs Antwort zurückgegeben wird, hinzugefügt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-105">The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response.</span></span> <span data-ttu-id="0d4ee-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

<span data-ttu-id="0d4ee-107">**DelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="0d4ee-107">**DelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0d4ee-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ee-108">Attributes and elements</span></span>

<span data-ttu-id="0d4ee-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d4ee-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d4ee-110">Attributes</span></span>

<span data-ttu-id="0d4ee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d4ee-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ee-112">Child elements</span></span>

|<span data-ttu-id="0d4ee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d4ee-113">**Element**</span></span>|<span data-ttu-id="0d4ee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d4ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d4ee-115">UserId</span><span class="sxs-lookup"><span data-stu-id="0d4ee-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="0d4ee-116">Identifiziert den Delegaten.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-116">Identifies the delegate.</span></span> <span data-ttu-id="0d4ee-117">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0d4ee-118">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="0d4ee-118">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="0d4ee-119">Enthält die Einstellungen für Stellvertreter-Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-119">Contains the delegate permission level settings.</span></span> <span data-ttu-id="0d4ee-120">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0d4ee-121">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="0d4ee-121">ReceiveCopiesOfMeetingMessages</span></span>](receivecopiesofmeetingmessages.md) <br/> |<span data-ttu-id="0d4ee-122">Gibt an, ob eine Stellvertretung Kopien von Besprechungs bezogenen Nachrichten empfängt, die an den Prinzipal adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-122">Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="0d4ee-123">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0d4ee-124">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="0d4ee-124">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="0d4ee-125">Gibt an, ob eine Stellvertretung über die Berechtigung zum Anzeigen privater Kalenderelemente im Postfach des Prinzipals verfügt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-125">Indicates whether a delegate has permission to view private calendar items in the principal's mailbox.</span></span> <span data-ttu-id="0d4ee-126">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d4ee-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ee-127">Parent elements</span></span>

|<span data-ttu-id="0d4ee-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d4ee-128">**Element**</span></span>|<span data-ttu-id="0d4ee-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d4ee-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d4ee-130">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="0d4ee-130">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="0d4ee-131">Enthält die Identitäten von Stellvertretungen, die in einem Postfach hinzugefügt oder aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-131">Contains the identities of delegates to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0d4ee-132">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="0d4ee-132">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="0d4ee-133">Enthält Antwortnachrichten für Delegate-Verwaltungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-133">Contains response messages for delegate management operations.</span></span> <span data-ttu-id="0d4ee-134">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d4ee-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d4ee-135">Remarks</span></span>

<span data-ttu-id="0d4ee-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0d4ee-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d4ee-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0d4ee-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d4ee-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d4ee-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d4ee-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d4ee-139">Schema Name</span></span>  <br/> |<span data-ttu-id="0d4ee-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0d4ee-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d4ee-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d4ee-141">Validation File</span></span>  <br/> |<span data-ttu-id="0d4ee-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d4ee-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d4ee-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0d4ee-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d4ee-144">False</span><span class="sxs-lookup"><span data-stu-id="0d4ee-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d4ee-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d4ee-145">See also</span></span>

- [<span data-ttu-id="0d4ee-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d4ee-146">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="0d4ee-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d4ee-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="0d4ee-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0d4ee-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0d4ee-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="0d4ee-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

