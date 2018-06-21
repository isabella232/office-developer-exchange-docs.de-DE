---
title: Element
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
description: Member-Element stellt ein Member einer Verteilerliste.
ms.openlocfilehash: c38e2ed24e78b5199d4d65cce27a00a8e6704037
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19830434"
---
# <a name="member"></a><span data-ttu-id="ad410-103">Element</span><span class="sxs-lookup"><span data-stu-id="ad410-103">Member</span></span>

<span data-ttu-id="ad410-104">**Member** -Element stellt ein Member einer Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="ad410-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="ad410-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="ad410-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ad410-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad410-106">Attributes and elements</span></span>

<span data-ttu-id="ad410-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad410-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad410-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad410-108">Attributes</span></span>

|<span data-ttu-id="ad410-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad410-109">**Attribute**</span></span>|<span data-ttu-id="ad410-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad410-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad410-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ad410-111">Key</span></span>  <br/> |<span data-ttu-id="ad410-112">Stellt einen eindeutigen Bezeichner für den Mitglieds der Verteilerliste bereit.</span><span class="sxs-lookup"><span data-stu-id="ad410-112">Provides a unique identifier for the distribution list member.</span></span> <span data-ttu-id="ad410-113">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="ad410-113">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad410-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad410-114">Child elements</span></span>

|<span data-ttu-id="ad410-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad410-115">**Element**</span></span>|<span data-ttu-id="ad410-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad410-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad410-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="ad410-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="ad410-118">Die e-Mail-Adresse der Mitglieds der Verteilerliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad410-118">Represents the e-mail address of the distribution list member.</span></span> <span data-ttu-id="ad410-119">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ad410-119">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ad410-120">Status (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="ad410-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="ad410-121">Enthält Informationen über den Status des eines Mitglieds der Verteilung.</span><span class="sxs-lookup"><span data-stu-id="ad410-121">Provides information about the status of a distribution list member.</span></span> <span data-ttu-id="ad410-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ad410-122">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad410-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad410-123">Parent elements</span></span>

|<span data-ttu-id="ad410-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad410-124">**Element**</span></span>|<span data-ttu-id="ad410-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad410-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad410-126">Elemente des Objekts (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="ad410-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="ad410-127">Enthält eine Liste der Mitglieder der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="ad410-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad410-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad410-128">Remarks</span></span>

<span data-ttu-id="ad410-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ad410-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad410-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ad410-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad410-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad410-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad410-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad410-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ad410-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ad410-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad410-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad410-134">Validation File</span></span>  <br/> |<span data-ttu-id="ad410-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad410-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad410-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ad410-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad410-137">False</span><span class="sxs-lookup"><span data-stu-id="ad410-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad410-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad410-138">See also</span></span>

- [<span data-ttu-id="ad410-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad410-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

