---
title: Member
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Member
api_type:
- schema
ms.assetid: af9c5ff8-02a4-41fc-876d-14ac05f1ee77
description: Das Member-Element stellt ein Mitglied einer Verteilerliste dar.
ms.openlocfilehash: e84223b7c41846ca2f174293bff46a8825777a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457305"
---
# <a name="member"></a><span data-ttu-id="9ae51-103">Member</span><span class="sxs-lookup"><span data-stu-id="9ae51-103">Member</span></span>

<span data-ttu-id="9ae51-104">Das **Member** -Element stellt ein Mitglied einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="9ae51-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="9ae51-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="9ae51-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9ae51-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9ae51-106">Attributes and elements</span></span>

<span data-ttu-id="9ae51-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9ae51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ae51-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9ae51-108">Attributes</span></span>

|<span data-ttu-id="9ae51-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9ae51-109">**Attribute**</span></span>|<span data-ttu-id="9ae51-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ae51-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ae51-111">Key</span><span class="sxs-lookup"><span data-stu-id="9ae51-111">Key</span></span>  <br/> |<span data-ttu-id="9ae51-112">Stellt einen eindeutigen Bezeichner für das Verteilerlistenelement bereit.</span><span class="sxs-lookup"><span data-stu-id="9ae51-112">Provides a unique identifier for the distribution list member.</span></span> <span data-ttu-id="9ae51-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="9ae51-113">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ae51-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ae51-114">Child elements</span></span>

|<span data-ttu-id="9ae51-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ae51-115">**Element**</span></span>|<span data-ttu-id="9ae51-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ae51-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ae51-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="9ae51-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="9ae51-118">Stellt die e-Mail-Adresse des Verteilerlisten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="9ae51-118">Represents the e-mail address of the distribution list member.</span></span> <span data-ttu-id="9ae51-119">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9ae51-119">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9ae51-120">Status (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="9ae51-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="9ae51-121">Enthält Informationen zum Status eines Verteilerlisten Elements.</span><span class="sxs-lookup"><span data-stu-id="9ae51-121">Provides information about the status of a distribution list member.</span></span> <span data-ttu-id="9ae51-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="9ae51-122">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ae51-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ae51-123">Parent elements</span></span>

|<span data-ttu-id="9ae51-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ae51-124">**Element**</span></span>|<span data-ttu-id="9ae51-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ae51-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ae51-126">Members (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="9ae51-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="9ae51-127">Enthält eine Liste der Mitglieder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="9ae51-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ae51-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ae51-128">Remarks</span></span>

<span data-ttu-id="9ae51-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9ae51-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ae51-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9ae51-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ae51-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ae51-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ae51-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9ae51-132">Schema Name</span></span>  <br/> |<span data-ttu-id="9ae51-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9ae51-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ae51-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9ae51-134">Validation File</span></span>  <br/> |<span data-ttu-id="9ae51-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ae51-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ae51-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9ae51-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ae51-137">False</span><span class="sxs-lookup"><span data-stu-id="9ae51-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ae51-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae51-138">See also</span></span>

- [<span data-ttu-id="9ae51-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9ae51-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

