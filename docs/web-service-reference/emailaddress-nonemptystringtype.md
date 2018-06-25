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
description: Das EmailAddress-Element definiert die primäre SMTP-Adresse eines Postfachbenutzers an.
ms.openlocfilehash: fcf2839c1e2e40a22d6b6a856608f52f2c9c2a1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758165"
---
# <a name="emailaddress-nonemptystringtype"></a><span data-ttu-id="b617a-103">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="b617a-103">EmailAddress (NonEmptyStringType)</span></span>

<span data-ttu-id="b617a-104">Das **EmailAddress** -Element definiert die primäre SMTP-Adresse eines Postfachbenutzers an.</span><span class="sxs-lookup"><span data-stu-id="b617a-104">The **EmailAddress** element defines the primary SMTP address of a mailbox user.</span></span> 
  
```XML
<EmailAddress/>
```

 <span data-ttu-id="b617a-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="b617a-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b617a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b617a-106">Attributes and elements</span></span>

<span data-ttu-id="b617a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b617a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b617a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b617a-108">Attributes</span></span>

<span data-ttu-id="b617a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b617a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b617a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b617a-110">Child elements</span></span>

<span data-ttu-id="b617a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b617a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b617a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b617a-112">Parent elements</span></span>

|<span data-ttu-id="b617a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b617a-113">**Element**</span></span>|<span data-ttu-id="b617a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b617a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b617a-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="b617a-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="b617a-116">Identifiziert, die der Anrufer als sendet.</span><span class="sxs-lookup"><span data-stu-id="b617a-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="b617a-117">Postfach</span><span class="sxs-lookup"><span data-stu-id="b617a-117">Mailbox</span></span>](mailbox.md) <br/> | <span data-ttu-id="b617a-118">Identifiziert eine vollständig aufgelöster E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b617a-118">Identifies a fully resolved e-mail address.</span></span>  <br/><br/><span data-ttu-id="b617a-119">Im folgenden sind einige XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b617a-119">The following are some XPath expressions to this element:</span></span><br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/><span data-ttu-id="b617a-120">Im folgenden sind zusätzliche übergeordnete Elemente des Postfach-Elements:</span><span class="sxs-lookup"><span data-stu-id="b617a-120">The following are additional parent elements of the Mailbox element:</span></span><br/><br/><span data-ttu-id="b617a-121">- [BccRecipients](bccrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-121">- [BccRecipients](bccrecipients.md)</span></span> <br/><span data-ttu-id="b617a-122">- [ReplyTo](replyto.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-122">- [ReplyTo](replyto.md)</span></span> <br/><span data-ttu-id="b617a-123">- [Absender](sender.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-123">- [Sender](sender.md)</span></span> <br/><span data-ttu-id="b617a-124">- [Von](from.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-124">- [From](from.md)</span></span> <br/><span data-ttu-id="b617a-125">- [Organizer](organizer.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-125">- [Organizer](organizer.md)</span></span> <br/><span data-ttu-id="b617a-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-126">- [DistinguishedFolderId](distinguishedfolderid.md)</span></span> <br/><span data-ttu-id="b617a-127">- [Lösung](resolution.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-127">- [Resolution](resolution.md)</span></span> <br/><span data-ttu-id="b617a-128">- [DLExpansion](dlexpansion.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-128">- [DLExpansion](dlexpansion.md)</span></span> <br/><span data-ttu-id="b617a-129">- [Teilnehmer](attendee.md)</span><span class="sxs-lookup"><span data-stu-id="b617a-129">- [Attendee](attendee.md)</span></span> <br/> |
|[<span data-ttu-id="b617a-130">RoomList</span><span class="sxs-lookup"><span data-stu-id="b617a-130">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="b617a-131">Eine Liste der Besprechungsräumen von e-Mail-Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b617a-131">Identifies a list of meeting rooms by email address.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b617a-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="b617a-132">Text value</span></span>

<span data-ttu-id="b617a-133">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b617a-133">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b617a-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b617a-134">Remarks</span></span>

<span data-ttu-id="b617a-135">Das **EmailAddress** -Element kann SMTP darstellen oder legacy-Exchange-distinguished Name (DN)-Adressen.</span><span class="sxs-lookup"><span data-stu-id="b617a-135">The **EmailAddress** element can represent SMTP or legacy Exchange distinguished name (also known as DN) addresses.</span></span> <span data-ttu-id="b617a-136">Das **EmailAddress** -Element ist das einzige erforderliche [Postfach](mailbox.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="b617a-136">The **EmailAddress** element is the only required [Mailbox](mailbox.md) element.</span></span> 
  
<span data-ttu-id="b617a-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b617a-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b617a-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b617a-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b617a-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="b617a-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b617a-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b617a-140">Schema Name</span></span>  <br/> |<span data-ttu-id="b617a-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b617a-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="b617a-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b617a-142">Validation File</span></span>  <br/> |<span data-ttu-id="b617a-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b617a-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b617a-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b617a-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="b617a-145">False</span><span class="sxs-lookup"><span data-stu-id="b617a-145">False</span></span>  <br/> |
   

