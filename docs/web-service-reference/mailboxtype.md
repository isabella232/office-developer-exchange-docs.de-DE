---
title: MailboxType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxType
api_type:
- schema
ms.assetid: 696e5fdb-d8c5-40f0-9e79-885eae65dfa4
description: Das Element MailboxType stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.
ms.openlocfilehash: d7232377951e8d9c8f191ac856058bc28467cadd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830305"
---
# <a name="mailboxtype"></a><span data-ttu-id="e5913-103">MailboxType</span><span class="sxs-lookup"><span data-stu-id="e5913-103">MailboxType</span></span>

<span data-ttu-id="e5913-104">Das Element **MailboxType** stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5913-104">The **MailboxType** element represents the type of mailbox that is represented by the e-mail address.</span></span> 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

<span data-ttu-id="e5913-105">**MailboxTypeType**</span><span class="sxs-lookup"><span data-stu-id="e5913-105">**MailboxTypeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e5913-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5913-106">Attributes and elements</span></span>

<span data-ttu-id="e5913-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e5913-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5913-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5913-108">Attributes</span></span>

<span data-ttu-id="e5913-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5913-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5913-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5913-110">Child elements</span></span>

<span data-ttu-id="e5913-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5913-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e5913-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5913-112">Parent elements</span></span>

|<span data-ttu-id="e5913-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5913-113">**Element**</span></span>|<span data-ttu-id="e5913-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5913-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5913-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="e5913-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e5913-116">Identifiziert eine vollständig aufgelöster E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5913-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="e5913-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="e5913-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="e5913-118">Eine Liste der Besprechungsräumen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5913-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e5913-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="e5913-119">Text value</span></span>

<span data-ttu-id="e5913-120">Die folgende Tabelle enthält die möglichen Werte für das **MailboxType** -Element.</span><span class="sxs-lookup"><span data-stu-id="e5913-120">The following table lists the possible values for the **MailboxType** element.</span></span> 
  
|<span data-ttu-id="e5913-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e5913-121">**Value**</span></span>|<span data-ttu-id="e5913-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5913-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5913-123">Postfach</span><span class="sxs-lookup"><span data-stu-id="e5913-123">Mailbox</span></span>  <br/> |<span data-ttu-id="e5913-124">Ein e-Mail-aktivierte Active Directory-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5913-124">Represents a mail-enabled Active Directory object.</span></span>  <br/> |
|<span data-ttu-id="e5913-125">PublicDL</span><span class="sxs-lookup"><span data-stu-id="e5913-125">PublicDL</span></span>  <br/> |<span data-ttu-id="e5913-126">Stellt eine öffentliche Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="e5913-126">Represents a public distribution list.</span></span>  <br/> |
|<span data-ttu-id="e5913-127">PrivateDL</span><span class="sxs-lookup"><span data-stu-id="e5913-127">PrivateDL</span></span>  <br/> |<span data-ttu-id="e5913-128">Stellt eine private Verteilerliste im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="e5913-128">Represents a private distribution list in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="e5913-129">Kontakt</span><span class="sxs-lookup"><span data-stu-id="e5913-129">Contact</span></span>  <br/> |<span data-ttu-id="e5913-130">Stellt einen Kontakt im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="e5913-130">Represents a contact in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="e5913-131">Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="e5913-131">PublicFolder</span></span>  <br/> |<span data-ttu-id="e5913-132">Stellt einen öffentlichen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="e5913-132">Represents a public folder.</span></span>  <br/> |
|<span data-ttu-id="e5913-133">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="e5913-133">Unknown</span></span>  <br/> |<span data-ttu-id="e5913-134">Stellt einen unbekannten Typ des Postfachs an.</span><span class="sxs-lookup"><span data-stu-id="e5913-134">Represents an unknown type of mailbox.</span></span>  <br/> |
|<span data-ttu-id="e5913-135">OneOff</span><span class="sxs-lookup"><span data-stu-id="e5913-135">OneOff</span></span>  <br/> |<span data-ttu-id="e5913-136">Stellt einen einmaligen Member einer persönlichen Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="e5913-136">Represents a one-off member of a personal distribution list.</span></span>  <br/> |
|<span data-ttu-id="e5913-137">GroupMailbox</span><span class="sxs-lookup"><span data-stu-id="e5913-137">GroupMailbox</span></span>  <br/> |<span data-ttu-id="e5913-138">Stellt eine Gruppenpostfach an.</span><span class="sxs-lookup"><span data-stu-id="e5913-138">Represents a group mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5913-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5913-139">Remarks</span></span>

<span data-ttu-id="e5913-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e5913-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5913-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e5913-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5913-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5913-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5913-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e5913-143">Schema Name</span></span>  <br/> |<span data-ttu-id="e5913-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e5913-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5913-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e5913-145">Validation File</span></span>  <br/> |<span data-ttu-id="e5913-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e5913-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5913-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e5913-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="e5913-148">False</span><span class="sxs-lookup"><span data-stu-id="e5913-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5913-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5913-149">See also</span></span>

- [<span data-ttu-id="e5913-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5913-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

