---
title: DelegateUsers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUsers
api_type:
- schema
ms.assetid: f30f80d9-20c8-41cc-afc7-a5eec1e0c5ea
description: Das DelegateUsers-Element enthält die Identitäten von Stellvertretern, die in einem Postfach hinzugefügt oder aktualisiert werden sollen. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 69f5aab65634f41ec0f820da05dee79a300fb32e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457375"
---
# <a name="delegateusers"></a><span data-ttu-id="e1a23-104">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="e1a23-104">DelegateUsers</span></span>

<span data-ttu-id="e1a23-105">Das **DelegateUsers** -Element enthält die Identitäten von Stellvertretern, die in einem Postfach hinzugefügt oder aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1a23-105">The **DelegateUsers** element contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="e1a23-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1a23-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUsers>
   <DelegateUser>
</DelegateUsers>
```

<span data-ttu-id="e1a23-107">**ArrayOfDelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="e1a23-107">**ArrayOfDelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e1a23-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e1a23-108">Attributes and elements</span></span>

<span data-ttu-id="e1a23-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e1a23-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1a23-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e1a23-110">Attributes</span></span>

<span data-ttu-id="e1a23-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e1a23-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1a23-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1a23-112">Child elements</span></span>

|<span data-ttu-id="e1a23-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1a23-113">**Element**</span></span>|<span data-ttu-id="e1a23-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1a23-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1a23-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="e1a23-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="e1a23-116">Bezeichnet einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1a23-116">Identifies a single delegate to add to or update in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e1a23-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1a23-117">Parent elements</span></span>

|<span data-ttu-id="e1a23-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1a23-118">**Element**</span></span>|<span data-ttu-id="e1a23-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1a23-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1a23-120">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="e1a23-120">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="e1a23-121">Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="e1a23-121">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="e1a23-122">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1a23-122">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="e1a23-123">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="e1a23-123">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="e1a23-124">Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="e1a23-124">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="e1a23-125">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1a23-125">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1a23-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1a23-126">Remarks</span></span>

<span data-ttu-id="e1a23-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e1a23-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1a23-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e1a23-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1a23-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1a23-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e1a23-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e1a23-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e1a23-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e1a23-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e1a23-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e1a23-132">Validation File</span></span>  <br/> |<span data-ttu-id="e1a23-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e1a23-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e1a23-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e1a23-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1a23-135">False</span><span class="sxs-lookup"><span data-stu-id="e1a23-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1a23-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1a23-136">See also</span></span>

- [<span data-ttu-id="e1a23-137">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1a23-137">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="e1a23-138">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1a23-138">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="e1a23-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e1a23-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e1a23-140">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="e1a23-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

