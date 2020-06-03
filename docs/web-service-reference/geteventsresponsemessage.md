---
title: GetEventsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEventsResponseMessage
api_type:
- schema
ms.assetid: d433977f-b86a-499e-b9c3-f405ac229358
description: Das GetEventsResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetEvents-Vorgangsanforderung.
ms.openlocfilehash: d307aa1f5234ab5a7a2527c55f5e48814ea2687b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462857"
---
# <a name="geteventsresponsemessage"></a><span data-ttu-id="2f6fb-103">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2f6fb-103">GetEventsResponseMessage</span></span>

<span data-ttu-id="2f6fb-104">Das **GetEventsResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetEvents-Vorgangs](getevents-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-104">The **GetEventsResponseMessage** element contains the status and result of a single [GetEvents operation](getevents-operation.md) request.</span></span> 
  
```xml
<GetEventsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</GetEventsResponseMessage>
```

 <span data-ttu-id="2f6fb-105">**GetEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-105">**GetEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f6fb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2f6fb-106">Attributes and elements</span></span>

<span data-ttu-id="2f6fb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f6fb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2f6fb-108">Attributes</span></span>

|<span data-ttu-id="2f6fb-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-109">**Attribute**</span></span>|<span data-ttu-id="2f6fb-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f6fb-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2f6fb-112">Beschreibt den Status einer [GetEvents-Vorgangs](getevents-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-112">Describes the status of a [GetEvents operation](getevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="2f6fb-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="2f6fb-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="2f6fb-114">-Success</span><span class="sxs-lookup"><span data-stu-id="2f6fb-114">-  Success</span></span>  <br/><span data-ttu-id="2f6fb-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="2f6fb-115">-  Warning</span></span>  <br/><span data-ttu-id="2f6fb-116">-Error</span><span class="sxs-lookup"><span data-stu-id="2f6fb-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="2f6fb-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="2f6fb-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="2f6fb-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-118">**Value**</span></span>|<span data-ttu-id="2f6fb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f6fb-120">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="2f6fb-120">Success</span></span>  <br/> |<span data-ttu-id="2f6fb-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2f6fb-122">Warnung</span><span class="sxs-lookup"><span data-stu-id="2f6fb-122">Warning</span></span>  <br/> | <span data-ttu-id="2f6fb-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-123">Describes a request that was not processed.</span></span> <span data-ttu-id="2f6fb-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2f6fb-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="2f6fb-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="2f6fb-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2f6fb-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2f6fb-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="2f6fb-129">-Die Postfachdatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2f6fb-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="2f6fb-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="2f6fb-132">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="2f6fb-132">Error</span></span>  <br/> | <span data-ttu-id="2f6fb-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2f6fb-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="2f6fb-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2f6fb-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="2f6fb-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2f6fb-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="2f6fb-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="2f6fb-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="2f6fb-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="2f6fb-138">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="2f6fb-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="2f6fb-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="2f6fb-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2f6fb-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="2f6fb-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2f6fb-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="2f6fb-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2f6fb-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f6fb-142">Child elements</span></span>

|<span data-ttu-id="2f6fb-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-143">**Element**</span></span>|<span data-ttu-id="2f6fb-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6fb-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="2f6fb-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2f6fb-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2f6fb-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2f6fb-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2f6fb-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2f6fb-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2f6fb-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2f6fb-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2f6fb-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2f6fb-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="2f6fb-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2f6fb-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2f6fb-154">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2f6fb-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2f6fb-155">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f6fb-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2f6fb-156">Parent elements</span></span>

|<span data-ttu-id="2f6fb-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-157">**Element**</span></span>|<span data-ttu-id="2f6fb-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f6fb-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f6fb-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2f6fb-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2f6fb-160">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f6fb-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f6fb-161">Remarks</span></span>

<span data-ttu-id="2f6fb-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2f6fb-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f6fb-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2f6fb-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f6fb-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f6fb-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f6fb-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2f6fb-165">Schema Name</span></span>  <br/> |<span data-ttu-id="2f6fb-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2f6fb-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f6fb-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2f6fb-167">Validation File</span></span>  <br/> |<span data-ttu-id="2f6fb-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f6fb-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f6fb-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2f6fb-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f6fb-170">False</span><span class="sxs-lookup"><span data-stu-id="2f6fb-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f6fb-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f6fb-171">See also</span></span>

- [<span data-ttu-id="2f6fb-172">GetEvents</span><span class="sxs-lookup"><span data-stu-id="2f6fb-172">GetEvents</span></span>](getevents.md) 
- [<span data-ttu-id="2f6fb-173">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="2f6fb-173">GetEventsResponse</span></span>](geteventsresponse.md)
- [<span data-ttu-id="2f6fb-174">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f6fb-174">GetEvents operation</span></span>](getevents-operation.md)

