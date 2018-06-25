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
description: Das GetStreamingEventsResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetStreamingEvents Vorgang.
ms.openlocfilehash: 5fcc7ddde41b49a5d8b304da0732f4472c61a76a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829682"
---
# <a name="getstreamingeventsresponsemessage"></a><span data-ttu-id="409a4-103">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="409a4-103">GetStreamingEventsResponseMessage</span></span>

<span data-ttu-id="409a4-104">Das **GetStreamingEventsResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetStreamingEvents Vorgang](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="409a4-104">The **GetStreamingEventsResponseMessage** element contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="409a4-105">**GetStreamingEventsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="409a4-105">**GetStreamingEventsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="409a4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="409a4-106">Attributes and elements</span></span>

<span data-ttu-id="409a4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="409a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="409a4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="409a4-108">Attributes</span></span>

|<span data-ttu-id="409a4-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="409a4-109">**Attribute**</span></span>|<span data-ttu-id="409a4-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="409a4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="409a4-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="409a4-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="409a4-112">Beschreibt den Status einer Antwort [GetStreamingEvents Vorgang](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="409a4-112">Describes the status of a [GetStreamingEvents operation](getstreamingevents-operation.md) response.</span></span> <br/><br/><span data-ttu-id="409a4-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="409a4-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="409a4-114">-Success</span><span class="sxs-lookup"><span data-stu-id="409a4-114">-  Success</span></span>  <br/><span data-ttu-id="409a4-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="409a4-115">-  Warning</span></span>  <br/><span data-ttu-id="409a4-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="409a4-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="409a4-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="409a4-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="409a4-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="409a4-118">**Value**</span></span>|<span data-ttu-id="409a4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="409a4-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="409a4-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="409a4-120">Success</span></span>  <br/> |<span data-ttu-id="409a4-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="409a4-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="409a4-122">Warning</span><span class="sxs-lookup"><span data-stu-id="409a4-122">Warning</span></span>  <br/> | <span data-ttu-id="409a4-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="409a4-123">Describes a request that was not processed.</span></span> <span data-ttu-id="409a4-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="409a4-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="409a4-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="409a4-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="409a4-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="409a4-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="409a4-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="409a4-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="409a4-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="409a4-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="409a4-129">-Die Postfachdatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="409a4-129">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="409a4-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="409a4-130">-  A password has expired.</span></span>  <br/><span data-ttu-id="409a4-131">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="409a4-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="409a4-132">Fehler</span><span class="sxs-lookup"><span data-stu-id="409a4-132">Error</span></span>  <br/> | <span data-ttu-id="409a4-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="409a4-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="409a4-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="409a4-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="409a4-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="409a4-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="409a4-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="409a4-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="409a4-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="409a4-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="409a4-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="409a4-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="409a4-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="409a4-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="409a4-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="409a4-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="409a4-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="409a4-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="409a4-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="409a4-142">Child elements</span></span>

|<span data-ttu-id="409a4-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="409a4-143">**Element**</span></span>|<span data-ttu-id="409a4-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="409a4-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="409a4-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="409a4-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="409a4-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="409a4-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="409a4-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="409a4-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="409a4-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="409a4-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="409a4-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="409a4-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="409a4-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="409a4-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="409a4-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="409a4-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="409a4-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="409a4-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="409a4-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="409a4-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="409a4-154">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="409a4-154">Notifications</span></span>](notifications.md) <br/> |<span data-ttu-id="409a4-155">Enthält eine Liste von Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="409a4-155">Contains a list of information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
|[<span data-ttu-id="409a4-156">ErrorSubscriptionIds</span><span class="sxs-lookup"><span data-stu-id="409a4-156">ErrorSubscriptionIds</span></span>](errorsubscriptionids.md) <br/> |<span data-ttu-id="409a4-157">Enthält eine Liste der Abonnement-IDs, ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="409a4-157">Contains a list of subscription IDs that are invalid.</span></span>  <br/> |
|[<span data-ttu-id="409a4-158">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="409a4-158">ConnectionStatus</span></span>](connectionstatus.md) <br/> |<span data-ttu-id="409a4-159">Enthält eine Beschreibung des Status eines streaming Abonnements.</span><span class="sxs-lookup"><span data-stu-id="409a4-159">Provides a text description of the status of a streaming subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="409a4-160">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="409a4-160">Parent elements</span></span>

|<span data-ttu-id="409a4-161">**Element**</span><span class="sxs-lookup"><span data-stu-id="409a4-161">**Element**</span></span>|<span data-ttu-id="409a4-162">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="409a4-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="409a4-163">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="409a4-163">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="409a4-164">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="409a4-164">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="409a4-165">Textwert</span><span class="sxs-lookup"><span data-stu-id="409a4-165">Text value</span></span>

<span data-ttu-id="409a4-166">Keine.</span><span class="sxs-lookup"><span data-stu-id="409a4-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="409a4-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="409a4-167">Remarks</span></span>

<span data-ttu-id="409a4-168">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="409a4-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="409a4-169">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="409a4-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="409a4-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="409a4-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="409a4-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="409a4-171">Schema Name</span></span>  <br/> |<span data-ttu-id="409a4-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="409a4-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="409a4-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="409a4-173">Validation File</span></span>  <br/> |<span data-ttu-id="409a4-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="409a4-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="409a4-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="409a4-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="409a4-176">False</span><span class="sxs-lookup"><span data-stu-id="409a4-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="409a4-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="409a4-177">See also</span></span>

- [<span data-ttu-id="409a4-178">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="409a4-178">GetStreamingEvents</span></span>](getstreamingevents.md) 
- [<span data-ttu-id="409a4-179">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="409a4-179">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
- [<span data-ttu-id="409a4-180">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="409a4-180">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)

