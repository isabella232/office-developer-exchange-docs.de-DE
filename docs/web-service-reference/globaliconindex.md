---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: Das GlobalIconIndex-Element identifiziert den globalen Symbolindex für alle Elemente in einer Unterhaltung.
ms.openlocfilehash: 9900a80136a1a7eaae4634afd31568679f6dba1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459461"
---
# <a name="globaliconindex"></a><span data-ttu-id="53d1d-103">GlobalIconIndex</span><span class="sxs-lookup"><span data-stu-id="53d1d-103">GlobalIconIndex</span></span>

<span data-ttu-id="53d1d-104">Das **GlobalIconIndex** -Element identifiziert den globalen Symbolindex für alle Elemente in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="53d1d-104">The **GlobalIconIndex** element identifies the global icon index for all items in a conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="53d1d-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="53d1d-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53d1d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53d1d-106">Attributes and elements</span></span>

<span data-ttu-id="53d1d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53d1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53d1d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53d1d-108">Attributes</span></span>

<span data-ttu-id="53d1d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53d1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53d1d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53d1d-110">Child elements</span></span>

<span data-ttu-id="53d1d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="53d1d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53d1d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53d1d-112">Parent elements</span></span>

<span data-ttu-id="53d1d-113">Unter [Haltung (conversationtype)](conversation-conversationtype.md)  |  [Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)</span><span class="sxs-lookup"><span data-stu-id="53d1d-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="53d1d-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="53d1d-114">Text value</span></span>

<span data-ttu-id="53d1d-115">Die folgende Tabelle enthält die möglichen Text Werte für das **GlobalIconIndex** -Element.</span><span class="sxs-lookup"><span data-stu-id="53d1d-115">The following table contains the possible text values for the **GlobalIconIndex** element.</span></span> 
  
|<span data-ttu-id="53d1d-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="53d1d-116">**Value**</span></span>|<span data-ttu-id="53d1d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53d1d-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="53d1d-118">Standard</span><span class="sxs-lookup"><span data-stu-id="53d1d-118">Default</span></span>  <br/> |<span data-ttu-id="53d1d-119">Gibt das Standardsymbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-120">PostItem</span><span class="sxs-lookup"><span data-stu-id="53d1d-120">PostItem</span></span>  <br/> |<span data-ttu-id="53d1d-121">Gibt das Symbol für ein Beitrags Element an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="53d1d-122">Mailread</span><span class="sxs-lookup"><span data-stu-id="53d1d-122">MailRead</span></span>  <br/> |<span data-ttu-id="53d1d-123">Gibt das Symbol e-Mail-Lesezugriff an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="53d1d-124">MailUnread</span></span>  <br/> |<span data-ttu-id="53d1d-125">Gibt das Symbol für ungelesene Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-126">Mailantwortete</span><span class="sxs-lookup"><span data-stu-id="53d1d-126">MailReplied</span></span>  <br/> |<span data-ttu-id="53d1d-127">Gibt das Antwort-e-Mail-Symbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-128">Mailforwarded</span><span class="sxs-lookup"><span data-stu-id="53d1d-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="53d1d-129">Gibt das Symbol weitergeleitete e-Mail an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-130">Mailencrypted</span><span class="sxs-lookup"><span data-stu-id="53d1d-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="53d1d-131">Gibt das verschlüsselte e-Mail-Symbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="53d1d-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="53d1d-133">Gibt das Symbol Secure/Multipurpose Internet Mail Extensions (S/MIME) signierten e-Mail an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="53d1d-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="53d1d-135">Gibt das verschlüsselte Antwort-e-Mail-Symbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="53d1d-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="53d1d-137">Gibt das signierte S/MIME-Symbol für Antworten auf e-Mail an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="53d1d-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="53d1d-139">Gibt das Symbol für verschlüsselte weitergeleitete e-Mails an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="53d1d-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="53d1d-141">Gibt das Symbol S/MIME signiert weitergeleitete e-Mails an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="53d1d-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="53d1d-143">Gibt das verschlüsselte Symbol "e-Mail lesen" an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="53d1d-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="53d1d-145">Gibt das Symbol S/MIME signierte Nachrichten lesen an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="53d1d-146">MailIrm</span></span>  <br/> |<span data-ttu-id="53d1d-147">Gibt das Symbol für die Verwaltung von Informationsrechten (IRM)-geschützter e-Mail an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="53d1d-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="53d1d-149">Gibt das Symbol für IRM-geschützte weitergeleitete Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="53d1d-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="53d1d-151">Gibt das IRM-geschützte Antwort-e-Mail-Symbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="53d1d-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="53d1d-153">Gibt das Symbol für e-Mails an, die für das SMS-Routing (Short Message Service) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="53d1d-153">Specifies the icon for mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="53d1d-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="53d1d-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="53d1d-155">Gibt das Symbol für das SMS-Routing an einen externen Zustellungspfad an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="53d1d-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="53d1d-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="53d1d-157">Gibt das Symbol für die SMS-Weiterleitung an ein externes Messagingsystem an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="53d1d-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="53d1d-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="53d1d-159">Gibt das Symbol für die SMS-Zustellung an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="53d1d-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="53d1d-161">Gibt das Standardsymbol für Kontakte an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="53d1d-162">AppointmentItem</span><span class="sxs-lookup"><span data-stu-id="53d1d-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="53d1d-163">Gibt das Symbol für das Terminelement an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="53d1d-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="53d1d-165">Gibt das Symbol für Terminserien Termine an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="53d1d-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="53d1d-167">Gibt das Besprechungssymbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="53d1d-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="53d1d-169">Gibt das Symbol für Besprechungsserien an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="53d1d-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="53d1d-171">Gibt das Symbol für eine vorläufige Antwort an die Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="53d1d-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="53d1d-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="53d1d-173">Gibt das Symbol für die Besprechungs Akzeptanz an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="53d1d-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="53d1d-175">Gibt das Symbol für Besprechungsablehnung an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="53d1d-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="53d1d-177">Gibt das Symbol für eine eventuelle Antwort auf die Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="53d1d-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="53d1d-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="53d1d-179">Gibt das Symbol für das Besprechungs Abbruch an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="53d1d-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="53d1d-181">Gibt das Symbol für die Besprechungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="53d1d-182">TaskItem</span></span>  <br/> |<span data-ttu-id="53d1d-183">Gibt das Aufgabenelement Symbol an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="53d1d-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="53d1d-185">Gibt das Symbol für wiederkehrende Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="53d1d-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="53d1d-187">Gibt das Symbol für den Aufgaben Besitz an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="53d1d-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="53d1d-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="53d1d-189">Gibt das Symbol Aufgabe delegiertes an.</span><span class="sxs-lookup"><span data-stu-id="53d1d-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53d1d-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53d1d-190">Remarks</span></span>

<span data-ttu-id="53d1d-191">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="53d1d-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="53d1d-192">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="53d1d-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53d1d-193">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="53d1d-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53d1d-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="53d1d-194">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53d1d-195">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53d1d-195">Schema name</span></span>  <br/> |<span data-ttu-id="53d1d-196">Schematypen</span><span class="sxs-lookup"><span data-stu-id="53d1d-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="53d1d-197">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53d1d-197">Validation file</span></span>  <br/> |<span data-ttu-id="53d1d-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53d1d-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53d1d-199">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="53d1d-199">Can be empty</span></span>  <br/> |<span data-ttu-id="53d1d-200">false</span><span class="sxs-lookup"><span data-stu-id="53d1d-200">false</span></span>  <br/> |
   

