---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: IconIndex-Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung.
ms.openlocfilehash: 8ada9da2df1cf128009c9b153736b434925f1a3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829848"
---
# <a name="iconindex"></a><span data-ttu-id="54ce8-103">IconIndex</span><span class="sxs-lookup"><span data-stu-id="54ce8-103">IconIndex</span></span>

<span data-ttu-id="54ce8-104">**IconIndex** -Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="54ce8-104">The **IconIndex** element identifies the icon index for an item or conversation.</span></span> 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 <span data-ttu-id="54ce8-105">**IconIndexType**</span><span class="sxs-lookup"><span data-stu-id="54ce8-105">**IconIndexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54ce8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="54ce8-106">Attributes and elements</span></span>

<span data-ttu-id="54ce8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="54ce8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54ce8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="54ce8-108">Attributes</span></span>

<span data-ttu-id="54ce8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="54ce8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54ce8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54ce8-110">Child elements</span></span>

<span data-ttu-id="54ce8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="54ce8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54ce8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54ce8-112">Parent elements</span></span>

<span data-ttu-id="54ce8-113">[Unterhaltung (ConversationType)](conversation-conversationtype.md) | [Element](item.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md) | [Nachricht](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe ](task.md)</span><span class="sxs-lookup"><span data-stu-id="54ce8-113">[Conversation (ConversationType)](conversation-conversationtype.md) | [Item](item.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Message](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="54ce8-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="54ce8-114">Text value</span></span>

<span data-ttu-id="54ce8-115">Die folgende Tabelle enthält die möglichen Textwerte für das **IconIndex** -Element.</span><span class="sxs-lookup"><span data-stu-id="54ce8-115">The following table contains the possible text values for the **IconIndex** element.</span></span> 
  
|<span data-ttu-id="54ce8-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="54ce8-116">**Value**</span></span>|<span data-ttu-id="54ce8-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54ce8-117">**Description**</span></span>|
|:-----|:-----|
|||
|<span data-ttu-id="54ce8-118">Standard</span><span class="sxs-lookup"><span data-stu-id="54ce8-118">Default</span></span>  <br/> |<span data-ttu-id="54ce8-119">Gibt das Standardsymbol an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-119">Specifies the default icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-120">PostItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="54ce8-120">PostItem</span></span>  <br/> |<span data-ttu-id="54ce8-121">Gibt das Symbol für ein Post-Element an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-121">Specifies the icon for a post item.</span></span>  <br/> |
|<span data-ttu-id="54ce8-122">MailRead</span><span class="sxs-lookup"><span data-stu-id="54ce8-122">MailRead</span></span>  <br/> |<span data-ttu-id="54ce8-123">Gibt an, dass die Mail Symbol gelesen.</span><span class="sxs-lookup"><span data-stu-id="54ce8-123">Specifies the mail read icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-124">MailUnread</span><span class="sxs-lookup"><span data-stu-id="54ce8-124">MailUnread</span></span>  <br/> |<span data-ttu-id="54ce8-125">Gibt das Symbol Ungelesene Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="54ce8-125">Specifies the unread mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-126">MailReplied</span><span class="sxs-lookup"><span data-stu-id="54ce8-126">MailReplied</span></span>  <br/> |<span data-ttu-id="54ce8-127">Gibt die beantwortete e-Mail-Symbol an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-127">Specifies the replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-128">MailForwarded</span><span class="sxs-lookup"><span data-stu-id="54ce8-128">MailForwarded</span></span>  <br/> |<span data-ttu-id="54ce8-129">Gibt das weitergeleitete e-Mail-Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-129">Specifies the forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-130">MailEncrypted</span><span class="sxs-lookup"><span data-stu-id="54ce8-130">MailEncrypted</span></span>  <br/> |<span data-ttu-id="54ce8-131">Gibt das Symbol für verschlüsselte e-Mails an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-131">Specifies the encrypted mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-132">MailSmimeSigned</span><span class="sxs-lookup"><span data-stu-id="54ce8-132">MailSmimeSigned</span></span>  <br/> |<span data-ttu-id="54ce8-133">Gibt das Secure/Multipurpose Internet Mail Extensions (S/MIME) signierten e-Mail-Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-133">Specifies the Secure/Multipurpose Internet Mail Extensions (S/MIME) signed mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-134">MailEncryptedReplied</span><span class="sxs-lookup"><span data-stu-id="54ce8-134">MailEncryptedReplied</span></span>  <br/> |<span data-ttu-id="54ce8-135">Gibt an, die verschlüsselte e-Mail-Symbol geantwortet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-135">Specifies the encrypted replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-136">MailSmimeSignedReplied</span><span class="sxs-lookup"><span data-stu-id="54ce8-136">MailSmimeSignedReplied</span></span>  <br/> |<span data-ttu-id="54ce8-137">Gibt an, der S/MIME beantwortete Symbol "Voicemail" angemeldet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-137">Specifies the S/MIME signed replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-138">MailEncryptedForwarded</span><span class="sxs-lookup"><span data-stu-id="54ce8-138">MailEncryptedForwarded</span></span>  <br/> |<span data-ttu-id="54ce8-139">Gibt das Symbol für verschlüsselte weitergeleitete e-Mails an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-139">Specifies the encrypted forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-140">MailSmimeSignedForwarded</span><span class="sxs-lookup"><span data-stu-id="54ce8-140">MailSmimeSignedForwarded</span></span>  <br/> |<span data-ttu-id="54ce8-141">Gibt an, der S/MIME signiert Symbol "Voicemail" weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-141">Specifies the S/MIME signed forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-142">MailEncryptedRead</span><span class="sxs-lookup"><span data-stu-id="54ce8-142">MailEncryptedRead</span></span>  <br/> |<span data-ttu-id="54ce8-143">Gibt das Symbol für verschlüsselte Nachrichten lesen.</span><span class="sxs-lookup"><span data-stu-id="54ce8-143">Specifies the encrypted read mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-144">MailSmimeSignedRead</span><span class="sxs-lookup"><span data-stu-id="54ce8-144">MailSmimeSignedRead</span></span>  <br/> |<span data-ttu-id="54ce8-145">Gibt an, der S/MIME signierten e-Mail-Symbol lesen.</span><span class="sxs-lookup"><span data-stu-id="54ce8-145">Specifies the S/MIME signed read mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-146">MailIrm</span><span class="sxs-lookup"><span data-stu-id="54ce8-146">MailIrm</span></span>  <br/> |<span data-ttu-id="54ce8-147">Gibt das Information Rights Management, IRM-geschützten e-Mail-Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-147">Specifies the Information Rights Management (IRM)-protected mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-148">MailIrmForwarded</span><span class="sxs-lookup"><span data-stu-id="54ce8-148">MailIrmForwarded</span></span>  <br/> |<span data-ttu-id="54ce8-149">Gibt die IRM-geschützten Symbol "Voicemail" weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-149">Specifies the IRM-protected forwarded mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-150">MailIrmReplied</span><span class="sxs-lookup"><span data-stu-id="54ce8-150">MailIrmReplied</span></span>  <br/> |<span data-ttu-id="54ce8-151">Gibt an, dass die IRM-geschützten e-Mail-Symbol geantwortet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-151">Specifies the IRM-protected replied to mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-152">SmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="54ce8-152">SmsSubmitted</span></span>  <br/> |<span data-ttu-id="54ce8-153">Gibt die Symbol e-Mail für das routing Short Message Service (SMS) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="54ce8-153">Specifies the icon mail submitted for Short Message Service (SMS) routing.</span></span>  <br/> |
|<span data-ttu-id="54ce8-154">SmsRoutedToDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="54ce8-154">SmsRoutedToDeliveryPoint</span></span>  <br/> |<span data-ttu-id="54ce8-155">Gibt das Symbol für die SMS-Weiterleitung an einen Punkt, externe Zustellung an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-155">Specifies the icon for SMS routing to an external delivery point.</span></span>  <br/> |
|<span data-ttu-id="54ce8-156">SmsRoutedToExternalMessagingSystem</span><span class="sxs-lookup"><span data-stu-id="54ce8-156">SmsRoutedToExternalMessagingSystem</span></span>  <br/> |<span data-ttu-id="54ce8-157">Gibt das Symbol für SMS-routing mit einem externen Messagingsystem an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-157">Specifies the icon for SMS routing to an external messaging system.</span></span>  <br/> |
|<span data-ttu-id="54ce8-158">SmsDelivered</span><span class="sxs-lookup"><span data-stu-id="54ce8-158">SmsDelivered</span></span>  <br/> |<span data-ttu-id="54ce8-159">Gibt das SMS zugestellte e-Mail-Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-159">Specifies the SMS delivered mail icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-160">OutlookDefaultForContacts</span><span class="sxs-lookup"><span data-stu-id="54ce8-160">OutlookDefaultForContacts</span></span>  <br/> |<span data-ttu-id="54ce8-161">Gibt das Standardsymbol für Kontakte.</span><span class="sxs-lookup"><span data-stu-id="54ce8-161">Specifies the default icon for contacts.</span></span>  <br/> |
|<span data-ttu-id="54ce8-162">AppointmentItem-Objekts</span><span class="sxs-lookup"><span data-stu-id="54ce8-162">AppointmentItem</span></span>  <br/> |<span data-ttu-id="54ce8-163">Gibt das Symbol Termin Element an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-163">Specifies the appointment item icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-164">AppointmentRecur</span><span class="sxs-lookup"><span data-stu-id="54ce8-164">AppointmentRecur</span></span>  <br/> |<span data-ttu-id="54ce8-165">Gibt die wiederkehrenden Termin Symbol an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-165">Specifies the recurring appointment icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-166">AppointmentMeet</span><span class="sxs-lookup"><span data-stu-id="54ce8-166">AppointmentMeet</span></span>  <br/> |<span data-ttu-id="54ce8-167">Gibt das Besprechungssymbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-167">Specifies the meeting icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-168">AppointmentMeetRecur</span><span class="sxs-lookup"><span data-stu-id="54ce8-168">AppointmentMeetRecur</span></span>  <br/> |<span data-ttu-id="54ce8-169">Gibt das Symbol für wiederkehrende Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-169">Specifies the recurring meeting icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-170">AppointmentMeetNY</span><span class="sxs-lookup"><span data-stu-id="54ce8-170">AppointmentMeetNY</span></span>  <br/> |<span data-ttu-id="54ce8-171">Gibt das Symbol für eine mit Vorbehalt Antwort auf die Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-171">Specifies the icon for a tentative response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="54ce8-172">AppointmentMeetYes</span><span class="sxs-lookup"><span data-stu-id="54ce8-172">AppointmentMeetYes</span></span>  <br/> |<span data-ttu-id="54ce8-173">Gibt an, die Besprechung Annahme-Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-173">Specifies the meeting acceptance icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-174">AppointmentMeetNo</span><span class="sxs-lookup"><span data-stu-id="54ce8-174">AppointmentMeetNo</span></span>  <br/> |<span data-ttu-id="54ce8-175">Gibt das Besprechungssymbol abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="54ce8-175">Specifies the meeting declined icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-176">AppointmentMeetMaybe</span><span class="sxs-lookup"><span data-stu-id="54ce8-176">AppointmentMeetMaybe</span></span>  <br/> |<span data-ttu-id="54ce8-177">Gibt das Symbol für eine Antwort möglicherweise zur Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-177">Specifies the icon for a maybe response to the meeting.</span></span>  <br/> |
|<span data-ttu-id="54ce8-178">AppointmentMeetCancel</span><span class="sxs-lookup"><span data-stu-id="54ce8-178">AppointmentMeetCancel</span></span>  <br/> |<span data-ttu-id="54ce8-179">Gibt an, die Besprechung absagen Symbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-179">Specifies the meeting cancel icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-180">AppointmentMeetInfo</span><span class="sxs-lookup"><span data-stu-id="54ce8-180">AppointmentMeetInfo</span></span>  <br/> |<span data-ttu-id="54ce8-181">Gibt an, die Besprechung Informationssymbol.</span><span class="sxs-lookup"><span data-stu-id="54ce8-181">Specifies the meeting information icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-182">TaskItem</span><span class="sxs-lookup"><span data-stu-id="54ce8-182">TaskItem</span></span>  <br/> |<span data-ttu-id="54ce8-183">Gibt das Symbol für Element an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-183">Specifies the task item icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-184">TaskRecur</span><span class="sxs-lookup"><span data-stu-id="54ce8-184">TaskRecur</span></span>  <br/> |<span data-ttu-id="54ce8-185">Gibt das Symbol für wiederkehrende Aufgaben an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-185">Specifies the recurring task icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-186">TaskOwned</span><span class="sxs-lookup"><span data-stu-id="54ce8-186">TaskOwned</span></span>  <br/> |<span data-ttu-id="54ce8-187">Gibt die Aufgabe Symbol gehören.</span><span class="sxs-lookup"><span data-stu-id="54ce8-187">Specifies the task owned icon.</span></span>  <br/> |
|<span data-ttu-id="54ce8-188">TaskDelegated</span><span class="sxs-lookup"><span data-stu-id="54ce8-188">TaskDelegated</span></span>  <br/> |<span data-ttu-id="54ce8-189">Gibt das Symbol für delegierte an.</span><span class="sxs-lookup"><span data-stu-id="54ce8-189">Specifies the task delegated icon.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54ce8-190">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54ce8-190">Remarks</span></span>

<span data-ttu-id="54ce8-191">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="54ce8-191">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="54ce8-192">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="54ce8-192">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54ce8-193">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="54ce8-193">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54ce8-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="54ce8-194">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54ce8-195">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="54ce8-195">Schema name</span></span>  <br/> |<span data-ttu-id="54ce8-196">Schematypen</span><span class="sxs-lookup"><span data-stu-id="54ce8-196">Types schema</span></span>  <br/> |
|<span data-ttu-id="54ce8-197">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="54ce8-197">Validation file</span></span>  <br/> |<span data-ttu-id="54ce8-198">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54ce8-198">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54ce8-199">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="54ce8-199">Can be empty</span></span>  <br/> |<span data-ttu-id="54ce8-200">false</span><span class="sxs-lookup"><span data-stu-id="54ce8-200">false</span></span>  <br/> |
   

