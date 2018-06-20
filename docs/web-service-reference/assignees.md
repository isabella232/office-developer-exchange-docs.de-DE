---
title: "\"Assignees\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: Das Element "assignees" gibt die Personen, die eine Aufgabe zugewiesen ist.
ms.openlocfilehash: 5fc301cd77268213e95fd33a2a2f36dbe218b512
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757385"
---
# <a name="assignees"></a><span data-ttu-id="99eca-103">"Assignees"</span><span class="sxs-lookup"><span data-stu-id="99eca-103">Assignees</span></span>

<span data-ttu-id="99eca-104">Das Element **"assignees"** gibt die Personen, die eine Aufgabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="99eca-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="99eca-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="99eca-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99eca-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99eca-106">Attributes and elements</span></span>

<span data-ttu-id="99eca-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99eca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99eca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="99eca-108">Attributes</span></span>

<span data-ttu-id="99eca-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="99eca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99eca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99eca-110">Child elements</span></span>

|<span data-ttu-id="99eca-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="99eca-111">**Element**</span></span>|<span data-ttu-id="99eca-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99eca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99eca-113">Name (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="99eca-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="99eca-114">Stellt den Anzeigenamen des Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="99eca-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="99eca-115">Benutzer-ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="99eca-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="99eca-116">Gibt die Benutzer-ID eines e-Mail-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="99eca-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99eca-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99eca-117">Parent elements</span></span>

|<span data-ttu-id="99eca-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="99eca-118">**Element**</span></span>|<span data-ttu-id="99eca-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99eca-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99eca-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="99eca-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="99eca-121">Gibt einen vorgeschlagenen Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="99eca-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99eca-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99eca-122">Remarks</span></span>

<span data-ttu-id="99eca-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99eca-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="99eca-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="99eca-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99eca-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="99eca-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99eca-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="99eca-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99eca-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99eca-127">Schema Name</span></span>  <br/> |<span data-ttu-id="99eca-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="99eca-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="99eca-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99eca-129">Validation File</span></span>  <br/> |<span data-ttu-id="99eca-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99eca-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="99eca-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="99eca-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="99eca-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99eca-132">See also</span></span>

- [<span data-ttu-id="99eca-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="99eca-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

