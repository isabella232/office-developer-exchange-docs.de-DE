---
title: SubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscribeResponseMessage
api_type:
- schema
ms.assetid: d121d38a-a61a-4f9c-a477-fc6d7f9af77e
description: Das SubscribeResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen subscribe-Vorgangsanforderung.
ms.openlocfilehash: eea7356dbcf1887383d56e40a4f6dcd091535fa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465373"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="ad5b0-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ad5b0-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="ad5b0-104">Das **SubscribeResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [subscribe-Vorgangs](subscribe-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="ad5b0-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="ad5b0-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="ad5b0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ad5b0-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="ad5b0-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ad5b0-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
```xml
<SubscribeResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SubscriptionId/>
   <Watermark/>
</SubscribeResponseMessage>
```

 <span data-ttu-id="ad5b0-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad5b0-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad5b0-109">Attributes and elements</span></span>

<span data-ttu-id="ad5b0-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad5b0-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad5b0-111">Attributes</span></span>

|<span data-ttu-id="ad5b0-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-112">**Attribute**</span></span>|<span data-ttu-id="ad5b0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad5b0-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ad5b0-115">Beschreibt den Status einer Antwort des [subscribe-Vorgangs](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5b0-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="ad5b0-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ad5b0-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ad5b0-117">-Success</span><span class="sxs-lookup"><span data-stu-id="ad5b0-117">-  Success</span></span>  <br/><span data-ttu-id="ad5b0-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ad5b0-118">-  Warning</span></span>  <br/><span data-ttu-id="ad5b0-119">-Error</span><span class="sxs-lookup"><span data-stu-id="ad5b0-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ad5b0-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="ad5b0-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="ad5b0-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-121">**Value**</span></span>|<span data-ttu-id="ad5b0-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad5b0-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-123">**Success**</span></span> <br/> |<span data-ttu-id="ad5b0-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ad5b0-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-125">**Warning**</span></span> <br/> | <span data-ttu-id="ad5b0-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-126">Describes a request that was not processed.</span></span> <span data-ttu-id="ad5b0-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ad5b0-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ad5b0-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ad5b0-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ad5b0-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ad5b0-131">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ad5b0-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ad5b0-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="ad5b0-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ad5b0-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-135">**Error**</span></span> <br/> | <span data-ttu-id="ad5b0-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ad5b0-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="ad5b0-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ad5b0-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ad5b0-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ad5b0-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="ad5b0-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ad5b0-140">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="ad5b0-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="ad5b0-141">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="ad5b0-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ad5b0-142">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="ad5b0-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ad5b0-143">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ad5b0-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ad5b0-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5b0-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad5b0-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad5b0-145">Child elements</span></span>

|<span data-ttu-id="ad5b0-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-146">**Element**</span></span>|<span data-ttu-id="ad5b0-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad5b0-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="ad5b0-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ad5b0-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ad5b0-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ad5b0-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ad5b0-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ad5b0-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ad5b0-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ad5b0-153">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ad5b0-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ad5b0-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="ad5b0-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ad5b0-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ad5b0-157">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="ad5b0-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="ad5b0-158">Stellt den Bezeichner für ein Abonnement dar.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="ad5b0-159">Watermark</span><span class="sxs-lookup"><span data-stu-id="ad5b0-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ad5b0-160">Stellt eine Ereignis Textmarke in der Post Fach Ereigniswarteschlange dar.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad5b0-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad5b0-161">Parent elements</span></span>

|<span data-ttu-id="ad5b0-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-162">**Element**</span></span>|<span data-ttu-id="ad5b0-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad5b0-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad5b0-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ad5b0-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ad5b0-165">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad5b0-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad5b0-166">Remarks</span></span>

<span data-ttu-id="ad5b0-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad5b0-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad5b0-168">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ad5b0-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad5b0-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad5b0-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ad5b0-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad5b0-170">Schema Name</span></span>  <br/> |<span data-ttu-id="ad5b0-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ad5b0-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ad5b0-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad5b0-172">Validation File</span></span>  <br/> |<span data-ttu-id="ad5b0-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ad5b0-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad5b0-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ad5b0-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad5b0-175">False</span><span class="sxs-lookup"><span data-stu-id="ad5b0-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad5b0-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad5b0-176">See also</span></span>

- [<span data-ttu-id="ad5b0-177">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="ad5b0-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="ad5b0-178">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ad5b0-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="ad5b0-179">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="ad5b0-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

