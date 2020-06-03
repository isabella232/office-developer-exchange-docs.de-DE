---
title: Empfängern
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: Das Element "assigners" gibt die Personen an, denen eine Aufgabe zugewiesen ist.
ms.openlocfilehash: 3e98273e859dbe2128b0ad3b4df42c8016fd3bc5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464714"
---
# <a name="assignees"></a><span data-ttu-id="091eb-103">Empfängern</span><span class="sxs-lookup"><span data-stu-id="091eb-103">Assignees</span></span>

<span data-ttu-id="091eb-104">Das Element " **assigners** " gibt die Personen an, denen eine Aufgabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="091eb-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="091eb-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="091eb-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="091eb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="091eb-106">Attributes and elements</span></span>

<span data-ttu-id="091eb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="091eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="091eb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="091eb-108">Attributes</span></span>

<span data-ttu-id="091eb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="091eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="091eb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="091eb-110">Child elements</span></span>

|<span data-ttu-id="091eb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="091eb-111">**Element**</span></span>|<span data-ttu-id="091eb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="091eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="091eb-113">Name (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="091eb-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="091eb-114">Stellt den Anzeigenamen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="091eb-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="091eb-115">UserID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="091eb-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="091eb-116">Gibt die Benutzer-ID eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="091eb-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="091eb-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="091eb-117">Parent elements</span></span>

|<span data-ttu-id="091eb-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="091eb-118">**Element**</span></span>|<span data-ttu-id="091eb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="091eb-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="091eb-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="091eb-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="091eb-121">Gibt eine vorgeschlagene Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="091eb-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="091eb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="091eb-122">Remarks</span></span>

<span data-ttu-id="091eb-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="091eb-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="091eb-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="091eb-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="091eb-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="091eb-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="091eb-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="091eb-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="091eb-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="091eb-127">Schema Name</span></span>  <br/> |<span data-ttu-id="091eb-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="091eb-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="091eb-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="091eb-129">Validation File</span></span>  <br/> |<span data-ttu-id="091eb-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="091eb-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="091eb-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="091eb-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="091eb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="091eb-132">See also</span></span>

- [<span data-ttu-id="091eb-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="091eb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

