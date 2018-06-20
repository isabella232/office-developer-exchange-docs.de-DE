---
title: UnsubscribeResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponseMessage
api_type:
- schema
ms.assetid: 92c53b13-0ca1-4b44-b925-b23682e9417c
description: Das UnsubscribeResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung zum Abmelden Vorgang.
ms.openlocfilehash: 09475b8c858ddcd0e404819b6b9a281cbf7cfcbb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839338"
---
# <a name="unsubscriberesponsemessage"></a><span data-ttu-id="87355-103">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="87355-103">UnsubscribeResponseMessage</span></span>

<span data-ttu-id="87355-104">Das **UnsubscribeResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [zum Abmelden Vorgang](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="87355-104">The **UnsubscribeResponseMessage** element contains the status and result of a single [Unsubscribe operation](unsubscribe-operation.md) request.</span></span> 
  
- [<span data-ttu-id="87355-105">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="87355-105">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
- [<span data-ttu-id="87355-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="87355-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="87355-107">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="87355-107">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
  
```xml
<UnsubscribeResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</UnsubscribeResponseMessage>
```

 <span data-ttu-id="87355-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="87355-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87355-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="87355-109">Attributes and elements</span></span>

<span data-ttu-id="87355-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="87355-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87355-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="87355-111">Attributes</span></span>

|<span data-ttu-id="87355-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="87355-112">**Attribute**</span></span>|<span data-ttu-id="87355-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87355-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87355-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="87355-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="87355-115">Beschreibt den Status einer Antwort auf einen [Vorgang zum Abmelden](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="87355-115">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span> <br/><br/><span data-ttu-id="87355-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="87355-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="87355-117">-Success</span><span class="sxs-lookup"><span data-stu-id="87355-117">-  Success</span></span>  <br/><span data-ttu-id="87355-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="87355-118">-  Warning</span></span>  <br/><span data-ttu-id="87355-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="87355-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="87355-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="87355-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="87355-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="87355-121">**Value**</span></span>|<span data-ttu-id="87355-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87355-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87355-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="87355-123">**Success**</span></span> <br/> |<span data-ttu-id="87355-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="87355-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="87355-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="87355-125">**Warning**</span></span> <br/> | <span data-ttu-id="87355-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="87355-126">Describes a request that was not processed.</span></span> <span data-ttu-id="87355-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="87355-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="87355-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="87355-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="87355-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="87355-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="87355-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="87355-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="87355-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="87355-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="87355-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="87355-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="87355-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="87355-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="87355-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="87355-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="87355-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="87355-135">**Error**</span></span> <br/> | <span data-ttu-id="87355-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="87355-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="87355-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="87355-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="87355-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="87355-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="87355-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="87355-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="87355-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="87355-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="87355-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="87355-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="87355-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="87355-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="87355-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="87355-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="87355-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="87355-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87355-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87355-145">Child elements</span></span>

|<span data-ttu-id="87355-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="87355-146">**Element**</span></span>|<span data-ttu-id="87355-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87355-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87355-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="87355-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="87355-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="87355-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="87355-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="87355-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="87355-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="87355-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="87355-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="87355-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="87355-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="87355-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="87355-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="87355-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="87355-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="87355-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="87355-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="87355-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="87355-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87355-157">Parent elements</span></span>

|<span data-ttu-id="87355-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="87355-158">**Element**</span></span>|<span data-ttu-id="87355-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87355-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87355-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="87355-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="87355-161">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="87355-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87355-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87355-162">Remarks</span></span>

<span data-ttu-id="87355-163">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="87355-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87355-164">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="87355-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87355-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="87355-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="87355-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="87355-166">Schema Name</span></span>  <br/> |<span data-ttu-id="87355-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="87355-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="87355-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="87355-168">Validation File</span></span>  <br/> |<span data-ttu-id="87355-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="87355-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="87355-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="87355-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="87355-171">False</span><span class="sxs-lookup"><span data-stu-id="87355-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87355-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87355-172">See also</span></span>

- [<span data-ttu-id="87355-173">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="87355-173">Unsubscribe operation</span></span>](unsubscribe-operation.md)
- [<span data-ttu-id="87355-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="87355-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

