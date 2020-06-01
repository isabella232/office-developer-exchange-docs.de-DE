---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: Das Address-Element definiert die primäre SMTP-Adresse eines Postfachbenutzers.
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463132"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="9e62e-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="9e62e-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="9e62e-104">Das Address **-Element definiert die primäre** SMTP-Adresse eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="9e62e-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="9e62e-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="9e62e-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e62e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e62e-106">Attributes and elements</span></span>

<span data-ttu-id="9e62e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e62e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e62e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e62e-108">Attributes</span></span>

<span data-ttu-id="9e62e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e62e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e62e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e62e-110">Child elements</span></span>

<span data-ttu-id="9e62e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e62e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e62e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e62e-112">Parent elements</span></span>

|<span data-ttu-id="9e62e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e62e-113">**Element**</span></span>|<span data-ttu-id="9e62e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e62e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e62e-115">Actingies</span><span class="sxs-lookup"><span data-stu-id="9e62e-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="9e62e-116">Gibt an, wen der Anrufer sendet.</span><span class="sxs-lookup"><span data-stu-id="9e62e-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="9e62e-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="9e62e-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="9e62e-118">Identifiziert eine vollständig aufgelöste e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9e62e-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="9e62e-119">Im folgenden finden Sie einige XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9e62e-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="9e62e-120">Im folgenden sind zusätzliche übergeordnete Elemente des Mailbox-Elements angegeben:</span><span class="sxs-lookup"><span data-stu-id="9e62e-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="9e62e-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="9e62e-122">- [ReplyTo](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="9e62e-123">- [Absender](sender.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="9e62e-124">- [Von](from.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-124">- [From](from.md)</span></span> <br/><span data-ttu-id="9e62e-125">- [Organisator](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="9e62e-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="9e62e-127">- [Lösung](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="9e62e-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="9e62e-129">- [Teilnehmer](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="9e62e-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="9e62e-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="9e62e-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="9e62e-131">Identifiziert eine Liste von Besprechungsräumen per e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9e62e-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9e62e-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="9e62e-132">Text value</span></span>

<span data-ttu-id="9e62e-133">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e62e-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e62e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e62e-134">Remarks</span></span>

<span data-ttu-id="9e62e-135">Das **Address** -Element kann SMTP-oder Legacy-Exchange Distinguished Name (auch als DN bekannt)-Adressen darstellen.</span><span class="sxs-lookup"><span data-stu-id="9e62e-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="9e62e-136">Das Element " **Email** " ist das einzige erforderliche [Post Fach](mailbox.md) Element.</span><span class="sxs-lookup"><span data-stu-id="9e62e-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="9e62e-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9e62e-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e62e-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9e62e-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e62e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e62e-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e62e-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9e62e-140">Schema Name</span></span>  <br/> |<span data-ttu-id="9e62e-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9e62e-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e62e-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9e62e-142">Validation File</span></span>  <br/> |<span data-ttu-id="9e62e-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e62e-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e62e-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9e62e-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e62e-145">False</span><span class="sxs-lookup"><span data-stu-id="9e62e-145">False</span></span>  <br/> |
   

