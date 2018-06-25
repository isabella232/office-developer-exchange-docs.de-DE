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
description: Das SubscribeResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung Subscribe-Vorgang.
ms.openlocfilehash: 97c7bd9f12511ff226e75f53278c13481679c8a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831621"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="d82f3-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d82f3-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="d82f3-104">Das **SubscribeResponseMessage** -Element enthält, der Status und das Ergebnis eines einzigen [Vorgang Subscribe](subscribe-operation.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d82f3-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="d82f3-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="d82f3-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="d82f3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d82f3-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="d82f3-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d82f3-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
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

 <span data-ttu-id="d82f3-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d82f3-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d82f3-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d82f3-109">Attributes and elements</span></span>

<span data-ttu-id="d82f3-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d82f3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d82f3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d82f3-111">Attributes</span></span>

|<span data-ttu-id="d82f3-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d82f3-112">**Attribute**</span></span>|<span data-ttu-id="d82f3-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d82f3-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d82f3-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d82f3-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d82f3-115">Beschreibt den Status einer Antwort [Subscribe-Vorgang](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="d82f3-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="d82f3-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d82f3-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d82f3-117">-Success</span><span class="sxs-lookup"><span data-stu-id="d82f3-117">-  Success</span></span>  <br/><span data-ttu-id="d82f3-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d82f3-118">-  Warning</span></span>  <br/><span data-ttu-id="d82f3-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="d82f3-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d82f3-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="d82f3-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="d82f3-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d82f3-121">**Value**</span></span>|<span data-ttu-id="d82f3-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d82f3-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d82f3-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="d82f3-123">**Success**</span></span> <br/> |<span data-ttu-id="d82f3-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d82f3-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d82f3-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d82f3-125">**Warning**</span></span> <br/> | <span data-ttu-id="d82f3-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d82f3-126">Describes a request that was not processed.</span></span> <span data-ttu-id="d82f3-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d82f3-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d82f3-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="d82f3-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="d82f3-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="d82f3-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d82f3-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d82f3-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d82f3-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="d82f3-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="d82f3-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d82f3-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d82f3-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d82f3-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="d82f3-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d82f3-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="d82f3-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="d82f3-135">**Error**</span></span> <br/> | <span data-ttu-id="d82f3-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d82f3-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d82f3-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="d82f3-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d82f3-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="d82f3-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d82f3-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="d82f3-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="d82f3-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="d82f3-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="d82f3-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d82f3-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="d82f3-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="d82f3-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d82f3-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="d82f3-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d82f3-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="d82f3-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d82f3-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d82f3-145">Child elements</span></span>

|<span data-ttu-id="d82f3-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="d82f3-146">**Element**</span></span>|<span data-ttu-id="d82f3-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d82f3-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d82f3-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="d82f3-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d82f3-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d82f3-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d82f3-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d82f3-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d82f3-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="d82f3-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d82f3-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d82f3-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d82f3-153">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d82f3-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="d82f3-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="d82f3-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d82f3-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="d82f3-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d82f3-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d82f3-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d82f3-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="d82f3-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="d82f3-158">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d82f3-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="d82f3-159">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="d82f3-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="d82f3-160">Stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach an.</span><span class="sxs-lookup"><span data-stu-id="d82f3-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d82f3-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d82f3-161">Parent elements</span></span>

|<span data-ttu-id="d82f3-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="d82f3-162">**Element**</span></span>|<span data-ttu-id="d82f3-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d82f3-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d82f3-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d82f3-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d82f3-165">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d82f3-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d82f3-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d82f3-166">Remarks</span></span>

<span data-ttu-id="d82f3-167">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d82f3-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d82f3-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d82f3-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d82f3-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="d82f3-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d82f3-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d82f3-170">Schema Name</span></span>  <br/> |<span data-ttu-id="d82f3-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d82f3-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d82f3-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d82f3-172">Validation File</span></span>  <br/> |<span data-ttu-id="d82f3-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d82f3-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d82f3-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d82f3-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="d82f3-175">False</span><span class="sxs-lookup"><span data-stu-id="d82f3-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d82f3-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d82f3-176">See also</span></span>

- [<span data-ttu-id="d82f3-177">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="d82f3-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="d82f3-178">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d82f3-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="d82f3-179">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="d82f3-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

