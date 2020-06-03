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
description: Das mailboxtype-Element stellt den Typ des Postfachs dar, das durch die e-Mail-Adresse dargestellt wird.
ms.openlocfilehash: 8c322ab8a87730832f5d199698a369656b058a9a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459798"
---
# <a name="mailboxtype"></a><span data-ttu-id="a6643-103">MailboxType</span><span class="sxs-lookup"><span data-stu-id="a6643-103">MailboxType</span></span>

<span data-ttu-id="a6643-104">Das **mailboxtype** -Element stellt den Typ des Postfachs dar, das durch die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a6643-104">The **MailboxType** element represents the type of mailbox that is represented by the e-mail address.</span></span> 
  
```XML
<MailboxType>Mailbox | PublicDL | PrivateDL | Contact | PublicFolder | Unknown | OneOff | GroupMailbox</MailboxType>
```

<span data-ttu-id="a6643-105">**MailboxTypeType**</span><span class="sxs-lookup"><span data-stu-id="a6643-105">**MailboxTypeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a6643-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a6643-106">Attributes and elements</span></span>

<span data-ttu-id="a6643-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6643-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6643-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a6643-108">Attributes</span></span>

<span data-ttu-id="a6643-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6643-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6643-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6643-110">Child elements</span></span>

<span data-ttu-id="a6643-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a6643-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6643-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a6643-112">Parent elements</span></span>

|<span data-ttu-id="a6643-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6643-113">**Element**</span></span>|<span data-ttu-id="a6643-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6643-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6643-115">Postfach</span><span class="sxs-lookup"><span data-stu-id="a6643-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="a6643-116">Identifiziert eine vollständig aufgelöste e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a6643-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="a6643-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="a6643-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="a6643-118">Gibt eine Liste von Besprechungsräumen an.</span><span class="sxs-lookup"><span data-stu-id="a6643-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6643-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="a6643-119">Text value</span></span>

<span data-ttu-id="a6643-120">In der folgenden Tabelle sind die möglichen Werte für das **mailboxtype** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6643-120">The following table lists the possible values for the **MailboxType** element.</span></span> 
  
|<span data-ttu-id="a6643-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6643-121">**Value**</span></span>|<span data-ttu-id="a6643-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6643-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6643-123">Postfach</span><span class="sxs-lookup"><span data-stu-id="a6643-123">Mailbox</span></span>  <br/> |<span data-ttu-id="a6643-124">Stellt ein e-Mail-aktiviertes Active Directory-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-124">Represents a mail-enabled Active Directory object.</span></span>  <br/> |
|<span data-ttu-id="a6643-125">PublicDL</span><span class="sxs-lookup"><span data-stu-id="a6643-125">PublicDL</span></span>  <br/> |<span data-ttu-id="a6643-126">Stellt eine öffentliche Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-126">Represents a public distribution list.</span></span>  <br/> |
|<span data-ttu-id="a6643-127">PrivateDL</span><span class="sxs-lookup"><span data-stu-id="a6643-127">PrivateDL</span></span>  <br/> |<span data-ttu-id="a6643-128">Stellt eine private Verteilerliste im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-128">Represents a private distribution list in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="a6643-129">Kontakt</span><span class="sxs-lookup"><span data-stu-id="a6643-129">Contact</span></span>  <br/> |<span data-ttu-id="a6643-130">Stellt einen Kontakt im Postfach eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-130">Represents a contact in a user's mailbox.</span></span>  <br/> |
|<span data-ttu-id="a6643-131">PublicFolder</span><span class="sxs-lookup"><span data-stu-id="a6643-131">PublicFolder</span></span>  <br/> |<span data-ttu-id="a6643-132">Stellt einen öffentlichen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-132">Represents a public folder.</span></span>  <br/> |
|<span data-ttu-id="a6643-133">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="a6643-133">Unknown</span></span>  <br/> |<span data-ttu-id="a6643-134">Stellt einen unbekannten Typ von Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-134">Represents an unknown type of mailbox.</span></span>  <br/> |
|<span data-ttu-id="a6643-135">OneOff</span><span class="sxs-lookup"><span data-stu-id="a6643-135">OneOff</span></span>  <br/> |<span data-ttu-id="a6643-136">Stellt ein einmaliges Mitglied einer persönlichen Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-136">Represents a one-off member of a personal distribution list.</span></span>  <br/> |
|<span data-ttu-id="a6643-137">GroupMailbox</span><span class="sxs-lookup"><span data-stu-id="a6643-137">GroupMailbox</span></span>  <br/> |<span data-ttu-id="a6643-138">Stellt ein Gruppenpostfach dar.</span><span class="sxs-lookup"><span data-stu-id="a6643-138">Represents a group mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6643-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6643-139">Remarks</span></span>

<span data-ttu-id="a6643-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a6643-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6643-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a6643-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6643-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6643-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6643-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a6643-143">Schema Name</span></span>  <br/> |<span data-ttu-id="a6643-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a6643-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6643-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a6643-145">Validation File</span></span>  <br/> |<span data-ttu-id="a6643-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6643-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6643-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a6643-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6643-148">False</span><span class="sxs-lookup"><span data-stu-id="a6643-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6643-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6643-149">See also</span></span>

- [<span data-ttu-id="a6643-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a6643-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

