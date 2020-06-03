---
title: GetStreamingEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEventsResponseMessage
api_type:
- schema
ms.assetid: 655e4e78-af74-48b0-a988-7d86ab368feb
description: Das GetStreamingEventsResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetStreamingEvents-Vorgangsanforderung.
ms.openlocfilehash: 055fb7eeb12e241739eb860cecbe398b8a322bd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459146"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="d5e49-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5e49-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="d5e49-104">Das **GetStreamingEventsResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5e49-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
```xml
<GetStreamingEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notifications/>
   <ErrorSubscriptionIds/>
   <ConnectionStatus/>
</GetStreamingEventsResponseMessage>
```

 <span data-ttu-id="d5e49-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d5e49-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5e49-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5e49-106">Attributes and elements</span></span>

<span data-ttu-id="d5e49-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5e49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5e49-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5e49-108">Attributes</span></span>

|<span data-ttu-id="d5e49-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d5e49-109">**Attribute**</span></span>|<span data-ttu-id="d5e49-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5e49-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5e49-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d5e49-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d5e49-112">Beschreibt den Status einer [GetStreamingEvents-Vorgangs](getstreamingevents-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="d5e49-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="d5e49-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d5e49-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d5e49-114">-Success</span><span class="sxs-lookup"><span data-stu-id="d5e49-114">-  Success</span></span>  <br/><span data-ttu-id="d5e49-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d5e49-115">-  Warning</span></span>  <br/><span data-ttu-id="d5e49-116">-Error</span><span class="sxs-lookup"><span data-stu-id="d5e49-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="d5e49-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="d5e49-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="d5e49-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d5e49-118">**Value**</span></span>|<span data-ttu-id="d5e49-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5e49-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5e49-120">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="d5e49-120">Success</span></span>  <br/> |<span data-ttu-id="d5e49-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d5e49-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d5e49-122">Warnung</span><span class="sxs-lookup"><span data-stu-id="d5e49-122">Warning</span></span>  <br/> | <span data-ttu-id="d5e49-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5e49-123">Describes a request that was not processed.</span></span> <span data-ttu-id="d5e49-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d5e49-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d5e49-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d5e49-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="d5e49-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="d5e49-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d5e49-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d5e49-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d5e49-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="d5e49-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="d5e49-129">-Die Postfachdatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d5e49-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d5e49-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d5e49-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="d5e49-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d5e49-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="d5e49-132">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="d5e49-132">Error</span></span>  <br/> | <span data-ttu-id="d5e49-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5e49-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d5e49-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="d5e49-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d5e49-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="d5e49-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d5e49-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="d5e49-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d5e49-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="d5e49-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="d5e49-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="d5e49-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d5e49-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="d5e49-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d5e49-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="d5e49-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d5e49-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e49-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d5e49-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5e49-142">Child elements</span></span>

|<span data-ttu-id="d5e49-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5e49-143">**Element**</span></span>|<span data-ttu-id="d5e49-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5e49-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5e49-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="d5e49-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d5e49-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d5e49-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d5e49-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d5e49-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d5e49-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d5e49-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d5e49-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d5e49-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d5e49-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="d5e49-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="d5e49-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d5e49-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d5e49-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-154">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d5e49-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="d5e49-155">Enthält eine Liste mit Informationen zum Abonnement und zu den Ereignissen, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d5e49-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="d5e49-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="d5e49-157">Enthält eine Liste von Abonnement-IDs, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="d5e49-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="d5e49-158">Den ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="d5e49-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="d5e49-159">Enthält eine Textbeschreibung des Status eines Streaming-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d5e49-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5e49-160">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5e49-160">Parent elements</span></span>

|<span data-ttu-id="d5e49-161">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5e49-161">**Element**</span></span>|<span data-ttu-id="d5e49-162">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5e49-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5e49-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d5e49-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d5e49-164">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d5e49-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d5e49-165">Textwert</span><span class="sxs-lookup"><span data-stu-id="d5e49-165">Text value</span></span>

<span data-ttu-id="d5e49-166">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5e49-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5e49-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5e49-167">Remarks</span></span>

<span data-ttu-id="d5e49-168">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d5e49-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5e49-169">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d5e49-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5e49-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5e49-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5e49-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5e49-171">Schema Name</span></span>  <br/> |<span data-ttu-id="d5e49-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d5e49-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5e49-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5e49-173">Validation File</span></span>  <br/> |<span data-ttu-id="d5e49-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d5e49-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5e49-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5e49-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5e49-176">False</span><span class="sxs-lookup"><span data-stu-id="d5e49-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5e49-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5e49-177">See also</span></span>

- [<span data-ttu-id="d5e49-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="d5e49-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="d5e49-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="d5e49-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="d5e49-180">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5e49-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

