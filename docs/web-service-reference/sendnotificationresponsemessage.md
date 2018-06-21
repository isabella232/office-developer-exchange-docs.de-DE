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
ms.lasthandoff: 06/21/2018
ms.locfileid: "19831348"
---
# <a name="sendnotificationresponsemessage"></a><span data-ttu-id="7f86b-103">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7f86b-103">SendNotificationResponseMessage</span></span>

<span data-ttu-id="7f86b-104">Das **SendNotificationResponseMessage** -Element enthält den Status und das Ergebnis einer Anforderung **SendNotification** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7f86b-104">The **SendNotificationResponseMessage** element contains the status and result of a single **SendNotification** operation request.</span></span> 
  
```xml
<SendNotificationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Notification/>
</SendNotificationResponseMessage>
```

 <span data-ttu-id="7f86b-105">**SendNotificationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7f86b-105">**SendNotificationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f86b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7f86b-106">Attributes and elements</span></span>

<span data-ttu-id="7f86b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7f86b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f86b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7f86b-108">Attributes</span></span>

|<span data-ttu-id="7f86b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7f86b-109">**Attribute**</span></span>|<span data-ttu-id="7f86b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f86b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f86b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7f86b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7f86b-112">Beschreibt den Status der Antwort eine **SendNotification** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7f86b-112">Describes the status of a **SendNotification** operation response.</span></span> <br/><br/><span data-ttu-id="7f86b-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="7f86b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="7f86b-114">-Success</span><span class="sxs-lookup"><span data-stu-id="7f86b-114">-  Success</span></span>  <br/><span data-ttu-id="7f86b-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="7f86b-115">-  Warning</span></span>  <br/><span data-ttu-id="7f86b-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="7f86b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="7f86b-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="7f86b-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="7f86b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7f86b-118">**Value**</span></span>|<span data-ttu-id="7f86b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f86b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f86b-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="7f86b-120">**Success**</span></span> <br/> |<span data-ttu-id="7f86b-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="7f86b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7f86b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7f86b-122">**Warning**</span></span> <br/> | <span data-ttu-id="7f86b-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7f86b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="7f86b-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="7f86b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="7f86b-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="7f86b-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7f86b-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="7f86b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7f86b-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7f86b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7f86b-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="7f86b-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="7f86b-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7f86b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7f86b-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="7f86b-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="7f86b-131">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="7f86b-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="7f86b-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="7f86b-132">**Error**</span></span> <br/> | <span data-ttu-id="7f86b-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f86b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7f86b-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="7f86b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7f86b-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="7f86b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7f86b-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="7f86b-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="7f86b-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="7f86b-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="7f86b-138">-Attribut oder ein Element, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7f86b-138">-  Attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="7f86b-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="7f86b-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7f86b-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="7f86b-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="7f86b-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7f86b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7f86b-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f86b-142">Child elements</span></span>

|<span data-ttu-id="7f86b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f86b-143">**Element**</span></span>|<span data-ttu-id="7f86b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f86b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f86b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="7f86b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7f86b-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="7f86b-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7f86b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7f86b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7f86b-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="7f86b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7f86b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7f86b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7f86b-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7f86b-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="7f86b-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="7f86b-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7f86b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7f86b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7f86b-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="7f86b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7f86b-154">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7f86b-154">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7f86b-155">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="7f86b-155">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7f86b-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7f86b-156">Parent elements</span></span>

|<span data-ttu-id="7f86b-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="7f86b-157">**Element**</span></span>|<span data-ttu-id="7f86b-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f86b-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f86b-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7f86b-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7f86b-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7f86b-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7f86b-161">Textwert</span><span class="sxs-lookup"><span data-stu-id="7f86b-161">Text value</span></span>

<span data-ttu-id="7f86b-162">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f86b-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f86b-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f86b-163">Remarks</span></span>

<span data-ttu-id="7f86b-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7f86b-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f86b-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7f86b-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f86b-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f86b-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7f86b-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7f86b-167">Schema Name</span></span>  <br/> |<span data-ttu-id="7f86b-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7f86b-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7f86b-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7f86b-169">Validation File</span></span>  <br/> |<span data-ttu-id="7f86b-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7f86b-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7f86b-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7f86b-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="7f86b-172">False</span><span class="sxs-lookup"><span data-stu-id="7f86b-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f86b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f86b-173">See also</span></span>

- [<span data-ttu-id="7f86b-174">SendNotification</span><span class="sxs-lookup"><span data-stu-id="7f86b-174">SendNotification</span></span>](sendnotification.md)
- [<span data-ttu-id="7f86b-175">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="7f86b-175">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="7f86b-176">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="7f86b-176">Unsubscribe operation</span></span>](unsubscribe-operation.md)

