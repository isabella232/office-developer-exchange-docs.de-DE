---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: Das getdelegate-Element definiert eine Anforderung zum Abrufen von Informationen zu Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: bd7fb55800b51eb2d69184bc4e04cdef3e6b9a89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461030"
---
# <a name="getdelegate"></a><span data-ttu-id="e11d7-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="e11d7-104">GetDelegate</span></span>

<span data-ttu-id="e11d7-105">Das **getdelegate** -Element definiert eine Anforderung zum Abrufen von Informationen zu Delegaten an ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="e11d7-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="e11d7-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e11d7-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="e11d7-107">**Getdelegattype**</span><span class="sxs-lookup"><span data-stu-id="e11d7-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e11d7-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e11d7-108">Attributes and elements</span></span>

<span data-ttu-id="e11d7-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e11d7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e11d7-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e11d7-110">Attributes</span></span>

|<span data-ttu-id="e11d7-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e11d7-111">**Attribute**</span></span>|<span data-ttu-id="e11d7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e11d7-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e11d7-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="e11d7-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="e11d7-114">Gibt an, ob die Antwort Berechtigungseinstellungen für jeden Delegate-Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="e11d7-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="e11d7-115">IncludePermissions-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="e11d7-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="e11d7-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e11d7-116">**Value**</span></span>|<span data-ttu-id="e11d7-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e11d7-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e11d7-118">**True**</span><span class="sxs-lookup"><span data-stu-id="e11d7-118">**True**</span></span> <br/> |<span data-ttu-id="e11d7-119">Stellvertreter Benutzerberechtigungen werden zusätzlich zu den Delegate-Benutzerinformationen zurückgegeben, die im [UserID](userid.md) -Element zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e11d7-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="e11d7-120">**False**</span><span class="sxs-lookup"><span data-stu-id="e11d7-120">**False**</span></span> <br/> |<span data-ttu-id="e11d7-121">[UserID](userid.md) -Informationen werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e11d7-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e11d7-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e11d7-122">Child elements</span></span>

|<span data-ttu-id="e11d7-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="e11d7-123">**Element**</span></span>|<span data-ttu-id="e11d7-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e11d7-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e11d7-125">Postfach</span><span class="sxs-lookup"><span data-stu-id="e11d7-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e11d7-126">Identifiziert das Postfach des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="e11d7-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e11d7-127">UserIds</span><span class="sxs-lookup"><span data-stu-id="e11d7-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="e11d7-128">Enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e11d7-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="e11d7-129">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e11d7-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e11d7-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e11d7-130">Parent elements</span></span>

<span data-ttu-id="e11d7-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="e11d7-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e11d7-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e11d7-132">Remarks</span></span>

<span data-ttu-id="e11d7-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e11d7-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e11d7-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e11d7-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e11d7-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="e11d7-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e11d7-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e11d7-136">Schema Name</span></span>  <br/> |<span data-ttu-id="e11d7-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e11d7-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e11d7-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e11d7-138">Validation File</span></span>  <br/> |<span data-ttu-id="e11d7-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e11d7-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e11d7-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e11d7-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="e11d7-141">False</span><span class="sxs-lookup"><span data-stu-id="e11d7-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e11d7-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e11d7-142">See also</span></span>



[<span data-ttu-id="e11d7-143">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e11d7-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="e11d7-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e11d7-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

