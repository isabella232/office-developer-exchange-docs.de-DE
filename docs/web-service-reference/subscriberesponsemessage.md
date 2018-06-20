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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831621"
---
# <a name="subscriberesponsemessage"></a><span data-ttu-id="11ca1-103">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="11ca1-103">SubscribeResponseMessage</span></span>

<span data-ttu-id="11ca1-104">Das **SubscribeResponseMessage** -Element enthält, der Status und das Ergebnis eines einzigen [Vorgang Subscribe](subscribe-operation.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="11ca1-104">The **SubscribeResponseMessage** element contains the status and result of a single [Subscribe operation](subscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="11ca1-105">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="11ca1-105">SubscribeResponse</span></span>](subscriberesponse.md)
- [<span data-ttu-id="11ca1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="11ca1-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="11ca1-107">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="11ca1-107">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
  
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

 <span data-ttu-id="11ca1-108">**SubscribeResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="11ca1-108">**SubscribeResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11ca1-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="11ca1-109">Attributes and elements</span></span>

<span data-ttu-id="11ca1-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="11ca1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11ca1-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="11ca1-111">Attributes</span></span>

|<span data-ttu-id="11ca1-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="11ca1-112">**Attribute**</span></span>|<span data-ttu-id="11ca1-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11ca1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11ca1-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="11ca1-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="11ca1-115">Beschreibt den Status einer Antwort [Subscribe-Vorgang](subscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="11ca1-115">Describes the status of a [Subscribe operation](subscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="11ca1-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="11ca1-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="11ca1-117">-Success</span><span class="sxs-lookup"><span data-stu-id="11ca1-117">-  Success</span></span>  <br/><span data-ttu-id="11ca1-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="11ca1-118">-  Warning</span></span>  <br/><span data-ttu-id="11ca1-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="11ca1-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="11ca1-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="11ca1-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="11ca1-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="11ca1-121">**Value**</span></span>|<span data-ttu-id="11ca1-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11ca1-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11ca1-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="11ca1-123">**Success**</span></span> <br/> |<span data-ttu-id="11ca1-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="11ca1-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="11ca1-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="11ca1-125">**Warning**</span></span> <br/> | <span data-ttu-id="11ca1-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="11ca1-126">Describes a request that was not processed.</span></span> <span data-ttu-id="11ca1-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="11ca1-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="11ca1-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="11ca1-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="11ca1-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="11ca1-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="11ca1-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="11ca1-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="11ca1-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="11ca1-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="11ca1-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="11ca1-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="11ca1-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="11ca1-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="11ca1-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="11ca1-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="11ca1-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="11ca1-135">**Error**</span></span> <br/> | <span data-ttu-id="11ca1-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="11ca1-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="11ca1-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="11ca1-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="11ca1-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="11ca1-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="11ca1-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="11ca1-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="11ca1-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="11ca1-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="11ca1-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="11ca1-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="11ca1-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="11ca1-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="11ca1-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="11ca1-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="11ca1-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="11ca1-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11ca1-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11ca1-145">Child elements</span></span>

|<span data-ttu-id="11ca1-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="11ca1-146">**Element**</span></span>|<span data-ttu-id="11ca1-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11ca1-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11ca1-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="11ca1-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="11ca1-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="11ca1-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="11ca1-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="11ca1-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="11ca1-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="11ca1-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="11ca1-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="11ca1-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="11ca1-153">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="11ca1-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="11ca1-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="11ca1-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="11ca1-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="11ca1-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="11ca1-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="11ca1-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="11ca1-157">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="11ca1-157">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="11ca1-158">Stellt den Bezeichner für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11ca1-158">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="11ca1-159">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="11ca1-159">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="11ca1-160">Stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach an.</span><span class="sxs-lookup"><span data-stu-id="11ca1-160">Represents an event bookmark in the mailbox event queue.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11ca1-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11ca1-161">Parent elements</span></span>

|<span data-ttu-id="11ca1-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="11ca1-162">**Element**</span></span>|<span data-ttu-id="11ca1-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11ca1-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11ca1-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="11ca1-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="11ca1-165">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="11ca1-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11ca1-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11ca1-166">Remarks</span></span>

<span data-ttu-id="11ca1-167">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="11ca1-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11ca1-168">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="11ca1-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11ca1-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="11ca1-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="11ca1-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="11ca1-170">Schema Name</span></span>  <br/> |<span data-ttu-id="11ca1-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="11ca1-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="11ca1-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="11ca1-172">Validation File</span></span>  <br/> |<span data-ttu-id="11ca1-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="11ca1-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="11ca1-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="11ca1-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="11ca1-175">False</span><span class="sxs-lookup"><span data-stu-id="11ca1-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11ca1-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11ca1-176">See also</span></span>

- [<span data-ttu-id="11ca1-177">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="11ca1-177">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="11ca1-178">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="11ca1-178">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="11ca1-179">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="11ca1-179">Unsubscribe operation</span></span>](unsubscribe-operation.md)

