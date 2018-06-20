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
description: Das GetDelegate-Element definiert eine Anforderung zum Abrufen von Informationen über Delegaten an ein Postfach. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758629"
---
# <a name="getdelegate"></a><span data-ttu-id="907cb-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="907cb-104">GetDelegate</span></span>

<span data-ttu-id="907cb-105">Das **GetDelegate** -Element definiert eine Anforderung zum Abrufen von Informationen über Delegaten an ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="907cb-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="907cb-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="907cb-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="907cb-107">**GetDelegateType**</span><span class="sxs-lookup"><span data-stu-id="907cb-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="907cb-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="907cb-108">Attributes and elements</span></span>

<span data-ttu-id="907cb-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="907cb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="907cb-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="907cb-110">Attributes</span></span>

|<span data-ttu-id="907cb-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="907cb-111">**Attribute**</span></span>|<span data-ttu-id="907cb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="907cb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="907cb-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="907cb-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="907cb-114">Gibt an, ob die Antwort berechtigungseinstellungen für jeden Benutzer Stellvertreter enthält.</span><span class="sxs-lookup"><span data-stu-id="907cb-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="907cb-115">Attributwerte IncludePermissions</span><span class="sxs-lookup"><span data-stu-id="907cb-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="907cb-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="907cb-116">**Value**</span></span>|<span data-ttu-id="907cb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="907cb-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="907cb-118">**True**</span><span class="sxs-lookup"><span data-stu-id="907cb-118">**True**</span></span> <br/> |<span data-ttu-id="907cb-119">Delegieren der Benutzer, den Berechtigungen zusätzlich zu den Delegaten Benutzerinformationen zurückgegeben werden, die im [UserId](userid.md) -Element zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="907cb-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="907cb-120">**False**</span><span class="sxs-lookup"><span data-stu-id="907cb-120">**False**</span></span> <br/> |<span data-ttu-id="907cb-121">[Benutzer-ID](userid.md) -Informationen werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="907cb-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="907cb-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="907cb-122">Child elements</span></span>

|<span data-ttu-id="907cb-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="907cb-123">**Element**</span></span>|<span data-ttu-id="907cb-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="907cb-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="907cb-125">Postfach</span><span class="sxs-lookup"><span data-stu-id="907cb-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="907cb-126">Identifiziert den Prinzipal Postfach an.</span><span class="sxs-lookup"><span data-stu-id="907cb-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="907cb-127">Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="907cb-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="907cb-128">Enthält ein Array von Delegaten Benutzern von einem Prinzipal Postfach abgerufen.</span><span class="sxs-lookup"><span data-stu-id="907cb-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="907cb-129">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="907cb-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="907cb-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="907cb-130">Parent elements</span></span>

<span data-ttu-id="907cb-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="907cb-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="907cb-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="907cb-132">Remarks</span></span>

<span data-ttu-id="907cb-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="907cb-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="907cb-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="907cb-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="907cb-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="907cb-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="907cb-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="907cb-136">Schema Name</span></span>  <br/> |<span data-ttu-id="907cb-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="907cb-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="907cb-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="907cb-138">Validation File</span></span>  <br/> |<span data-ttu-id="907cb-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="907cb-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="907cb-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="907cb-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="907cb-141">False</span><span class="sxs-lookup"><span data-stu-id="907cb-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="907cb-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="907cb-142">See also</span></span>



[<span data-ttu-id="907cb-143">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="907cb-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="907cb-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="907cb-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

