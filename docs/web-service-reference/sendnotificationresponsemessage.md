---
title: SendNotificationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotificationResponseMessage
api_type:
- schema
ms.assetid: 2c6d681b-67ac-4331-bc6b-a2e709b638e3
description: Das SendNotificationResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung SendNotification-Vorgang.
ms.openlocfilehash: 49677b6d61f525b469679ec3fdcb8aadcca7239d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19831348"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="884bb-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="884bb-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="884bb-104">Das **SendNotificationResponseMessage** -Element enthält den Status und das Ergebnis einer Anforderung **SendNotification** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="884bb-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="884bb-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="884bb-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="884bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="884bb-106">Attributes and elements</span></span>

<span data-ttu-id="884bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="884bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="884bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="884bb-108">Attributes</span></span>

|<span data-ttu-id="884bb-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="884bb-109">**Attribute**</span></span>|<span data-ttu-id="884bb-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884bb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="884bb-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="884bb-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="884bb-112">Beschreibt den Status der Antwort eine **SendNotification** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="884bb-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="884bb-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="884bb-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="884bb-114">-Success</span><span class="sxs-lookup"><span data-stu-id="884bb-114">-  Success</span></span>  <br/><span data-ttu-id="884bb-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="884bb-115">-  Warning</span></span>  <br/><span data-ttu-id="884bb-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="884bb-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="884bb-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="884bb-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="884bb-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="884bb-118">**Value**</span></span>|<span data-ttu-id="884bb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884bb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="884bb-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="884bb-120">**Success**</span></span> <br/> |<span data-ttu-id="884bb-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="884bb-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="884bb-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="884bb-122">**Warning**</span></span> <br/> | <span data-ttu-id="884bb-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="884bb-123">Describes a request that was not processed.</span></span> <span data-ttu-id="884bb-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="884bb-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="884bb-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="884bb-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="884bb-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="884bb-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="884bb-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="884bb-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="884bb-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="884bb-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="884bb-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="884bb-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="884bb-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="884bb-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="884bb-131">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="884bb-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="884bb-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="884bb-132">**Error**</span></span> <br/> | <span data-ttu-id="884bb-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="884bb-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="884bb-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="884bb-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="884bb-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="884bb-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="884bb-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="884bb-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="884bb-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="884bb-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="884bb-138">-Attribut oder ein Element, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="884bb-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="884bb-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="884bb-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="884bb-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="884bb-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="884bb-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="884bb-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="884bb-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="884bb-142">Child elements</span></span>

|<span data-ttu-id="884bb-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="884bb-143">**Element**</span></span>|<span data-ttu-id="884bb-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884bb-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="884bb-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="884bb-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="884bb-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="884bb-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="884bb-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="884bb-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="884bb-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="884bb-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="884bb-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="884bb-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="884bb-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="884bb-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="884bb-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="884bb-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="884bb-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="884bb-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="884bb-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="884bb-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="884bb-154">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="884bb-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="884bb-155">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="884bb-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="884bb-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="884bb-156">Parent elements</span></span>

|<span data-ttu-id="884bb-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="884bb-157">**Element**</span></span>|<span data-ttu-id="884bb-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="884bb-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="884bb-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="884bb-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="884bb-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="884bb-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="884bb-161">Textwert</span><span class="sxs-lookup"><span data-stu-id="884bb-161">Text value</span></span>

<span data-ttu-id="884bb-162">Keine.</span><span class="sxs-lookup"><span data-stu-id="884bb-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="884bb-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="884bb-163">Remarks</span></span>

<span data-ttu-id="884bb-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="884bb-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="884bb-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="884bb-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="884bb-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="884bb-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="884bb-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="884bb-167">Schema Name</span></span>  <br/> |<span data-ttu-id="884bb-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="884bb-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="884bb-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="884bb-169">Validation File</span></span>  <br/> |<span data-ttu-id="884bb-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="884bb-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="884bb-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="884bb-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="884bb-172">False</span><span class="sxs-lookup"><span data-stu-id="884bb-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="884bb-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="884bb-173">See also</span></span>

- [<span data-ttu-id="884bb-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="884bb-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="884bb-175">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="884bb-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="884bb-176">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="884bb-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

