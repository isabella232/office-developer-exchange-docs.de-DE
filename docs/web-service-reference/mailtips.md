---
title: MailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTips
api_type:
- schema
ms.assetid: c1cba493-bccc-4b8e-be8e-bfa8a8b10882
description: Das MailTips-Element stellt Werte für verschiedene Arten von e-Mail-Tipps dar.
ms.openlocfilehash: 9bacdea7b4f3108f700ed102025445e01a73e69d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44447596"
---
# <a name="mailtips"></a><span data-ttu-id="d0c3f-103">MailTips</span><span class="sxs-lookup"><span data-stu-id="d0c3f-103">MailTips</span></span>

<span data-ttu-id="d0c3f-104">Das **MailTips** -Element stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
```XML
<MailTips>
   <RecipientAddress/>
   <PendingMailTips/>
   <OutOfOffice/>
   <MailboxFull/>
   <CustomMailTip/>
   <TotalMemberCount/>
   <ExternalMemberCount/>
   <MaxMessageSize/>
   <DeliveryRestricted/>
   <IsModerated/>
   <InvalidRecipient/>
</MailTips>
```

 <span data-ttu-id="d0c3f-105">**E-Mail-Info**</span><span class="sxs-lookup"><span data-stu-id="d0c3f-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0c3f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c3f-106">Attributes and elements</span></span>

<span data-ttu-id="d0c3f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0c3f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0c3f-108">Attributes</span></span>

<span data-ttu-id="d0c3f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0c3f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c3f-110">Child elements</span></span>

|<span data-ttu-id="d0c3f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0c3f-111">**Element**</span></span>|<span data-ttu-id="d0c3f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0c3f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0c3f-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="d0c3f-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="d0c3f-114">Stellt das Postfach des Empfängers dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="d0c3f-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="d0c3f-116">Gibt an, dass die e-Mail-Tipps in diesem Element nicht ausgewertet werden konnten, bevor das Verarbeitungstimeout des Servers abgelaufen war.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-117">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="d0c3f-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="d0c3f-118">Stellt die Antwortnachricht und einen Zeitraum für das Senden der Antwortnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="d0c3f-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="d0c3f-120">Gibt an, ob das Postfach für den Empfänger voll ist.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="d0c3f-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="d0c3f-122">Stellt eine angepasste e-Mail-Tipp Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="d0c3f-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="d0c3f-124">Stellt die Anzahl aller Elemente in einer Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="d0c3f-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="d0c3f-126">Stellt die Anzahl externer Mitglieder in einer Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="d0c3f-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="d0c3f-128">Stellt die maximale Nachrichtengröße dar, die der Empfänger annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="d0c3f-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="d0c3f-130">Gibt an, ob durch Übermittlungseinschränkungen verhindert wird, dass die Nachricht des Absenders den Empfänger erreicht.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-131">Ismoderiert</span><span class="sxs-lookup"><span data-stu-id="d0c3f-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="d0c3f-132">Gibt an, ob das Postfach des Empfängers moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="d0c3f-133">InvalidRecipient (e-Mail-Infos)</span><span class="sxs-lookup"><span data-stu-id="d0c3f-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="d0c3f-134">Gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0c3f-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0c3f-135">Parent elements</span></span>

|<span data-ttu-id="d0c3f-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0c3f-136">**Element**</span></span>|<span data-ttu-id="d0c3f-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0c3f-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0c3f-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="d0c3f-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="d0c3f-139">Stellt Einstellungen für e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0c3f-140">Textwert</span><span class="sxs-lookup"><span data-stu-id="d0c3f-140">Text value</span></span>

<span data-ttu-id="d0c3f-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0c3f-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0c3f-142">Remarks</span></span>

<span data-ttu-id="d0c3f-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d0c3f-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0c3f-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d0c3f-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0c3f-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c3f-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0c3f-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0c3f-146">Schema Name</span></span>  <br/> |<span data-ttu-id="d0c3f-147">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d0c3f-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0c3f-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0c3f-148">Validation File</span></span>  <br/> |<span data-ttu-id="d0c3f-149">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d0c3f-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0c3f-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0c3f-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0c3f-151">False</span><span class="sxs-lookup"><span data-stu-id="d0c3f-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0c3f-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0c3f-152">See also</span></span>



- [<span data-ttu-id="d0c3f-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0c3f-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

