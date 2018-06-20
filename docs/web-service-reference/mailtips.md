---
title: E-Mail-Infos
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
description: Das e-Mail-Infos Element stellt Werte für verschiedene Arten von e-Mail-Infos.
ms.openlocfilehash: 3a2e95225b09fd2d81db32f821ea3069ab7e7852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830311"
---
# <a name="mailtips"></a><span data-ttu-id="208de-103">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="208de-103">MailTips</span></span>

<span data-ttu-id="208de-104">Das **e-Mail-Infos** Element stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="208de-104">The **MailTips** element represents values for various types of mail tips.</span></span> 
  
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

 <span data-ttu-id="208de-105">**E-Mail-Infos**</span><span class="sxs-lookup"><span data-stu-id="208de-105">**MailTips**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="208de-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="208de-106">Attributes and elements</span></span>

<span data-ttu-id="208de-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="208de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="208de-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="208de-108">Attributes</span></span>

<span data-ttu-id="208de-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="208de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="208de-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="208de-110">Child elements</span></span>

|<span data-ttu-id="208de-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="208de-111">**Element**</span></span>|<span data-ttu-id="208de-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="208de-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="208de-113">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="208de-113">RecipientAddress</span></span>](recipientaddress.md) <br/> |<span data-ttu-id="208de-114">Das Postfach des Empfängers darstellt.</span><span class="sxs-lookup"><span data-stu-id="208de-114">Represents the mailbox of the recipient.</span></span>  <br/> |
|[<span data-ttu-id="208de-115">PendingMailTips</span><span class="sxs-lookup"><span data-stu-id="208de-115">PendingMailTips</span></span>](pendingmailtips.md) <br/> |<span data-ttu-id="208de-116">Gibt an, dass die e-Mail-Infos in diesem Element nicht ausgewertet werden konnte, bevor die Verarbeitung der Servertimeout abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="208de-116">Indicates that the mail tips in this element could not be evaluated before the server's processing timeout expired.</span></span>  <br/> |
|[<span data-ttu-id="208de-117">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="208de-117">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="208de-118">Stellt die Antwortnachricht und einer Zeitdauer für die Response-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="208de-118">Represents the response message and a duration time for sending the response message.</span></span>  <br/> |
|[<span data-ttu-id="208de-119">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="208de-119">MailboxFull</span></span>](mailboxfull.md) <br/> |<span data-ttu-id="208de-120">Gibt an, ob das Postfach des Empfängers voll ist.</span><span class="sxs-lookup"><span data-stu-id="208de-120">Indicates whether the mailbox for the recipient is full.</span></span>  <br/> |
|[<span data-ttu-id="208de-121">CustomMailTip</span><span class="sxs-lookup"><span data-stu-id="208de-121">CustomMailTip</span></span>](custommailtip.md) <br/> |<span data-ttu-id="208de-122">Stellt eine benutzerdefinierte e-Mail-Info.</span><span class="sxs-lookup"><span data-stu-id="208de-122">Represents a customized mail tip message.</span></span>  <br/> |
|[<span data-ttu-id="208de-123">TotalMemberCount</span><span class="sxs-lookup"><span data-stu-id="208de-123">TotalMemberCount</span></span>](totalmembercount.md) <br/> |<span data-ttu-id="208de-124">Stellt die Anzahl aller Elemente in einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="208de-124">Represents the count of all members in a group.</span></span>  <br/> |
|[<span data-ttu-id="208de-125">ExternalMemberCount</span><span class="sxs-lookup"><span data-stu-id="208de-125">ExternalMemberCount</span></span>](externalmembercount.md) <br/> |<span data-ttu-id="208de-126">Stellt die Anzahl der externen Elemente in einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="208de-126">Represents the count of external members in a group.</span></span>  <br/> |
|[<span data-ttu-id="208de-127">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="208de-127">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="208de-128">Stellt die maximale Größe von Nachrichten, die der Empfänger akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="208de-128">Represents the maximum message size the recipient can accept.</span></span>  <br/> |
|[<span data-ttu-id="208de-129">DeliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="208de-129">DeliveryRestricted</span></span>](deliveryrestricted.md) <br/> |<span data-ttu-id="208de-130">Gibt an, ob Einschränkungen Übermittlung des Absenders der Nachricht verhindern Erreichen des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="208de-130">Indicates whether delivery restrictions will prevent the sender's message from reaching the recipient.</span></span>  <br/> |
|[<span data-ttu-id="208de-131">IsModerated</span><span class="sxs-lookup"><span data-stu-id="208de-131">IsModerated</span></span>](ismoderated.md) <br/> |<span data-ttu-id="208de-132">Gibt an, ob das Postfach des Empfängers ist moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="208de-132">Indicates whether the recipient's mailbox is being moderated.</span></span>  <br/> |
|[<span data-ttu-id="208de-133">InvalidRecipient (e-Mail-Infos)</span><span class="sxs-lookup"><span data-stu-id="208de-133">InvalidRecipient (MailTips)</span></span>](invalidrecipient-mailtips.md) <br/> |<span data-ttu-id="208de-134">Gibt an, ob der Empfänger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="208de-134">Indicates whether the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="208de-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="208de-135">Parent elements</span></span>

|<span data-ttu-id="208de-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="208de-136">**Element**</span></span>|<span data-ttu-id="208de-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="208de-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="208de-138">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="208de-138">MailTipsResponseMessageType</span></span>](mailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="208de-139">Stellt e-Mail-Tipps Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="208de-139">Represents mail tips settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="208de-140">Textwert</span><span class="sxs-lookup"><span data-stu-id="208de-140">Text value</span></span>

<span data-ttu-id="208de-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="208de-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="208de-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="208de-142">Remarks</span></span>

<span data-ttu-id="208de-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="208de-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="208de-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="208de-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="208de-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="208de-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="208de-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="208de-146">Schema Name</span></span>  <br/> |<span data-ttu-id="208de-147">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="208de-147">Messages schema</span></span>  <br/> |
|<span data-ttu-id="208de-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="208de-148">Validation File</span></span>  <br/> |<span data-ttu-id="208de-149">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="208de-149">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="208de-150">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="208de-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="208de-151">False</span><span class="sxs-lookup"><span data-stu-id="208de-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="208de-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="208de-152">See also</span></span>



- [<span data-ttu-id="208de-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="208de-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

