---
title: CopyItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItemResponseMessage
api_type:
- schema
ms.assetid: a43fe442-12c8-44ab-912c-8a226c9bb3e7
description: Das CopyItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CopyItem-Vorgang.
ms.openlocfilehash: 6c1acaff422fd731ca81a3ab244d76a73f3b5c15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757729"
---
# <a name="copyitemresponsemessage"></a><span data-ttu-id="5c6c4-103">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5c6c4-103">CopyItemResponseMessage</span></span>

<span data-ttu-id="5c6c4-104">Das **CopyItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CopyItem-Vorgang](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6c4-104">The **CopyItemResponseMessage** element contains the status and result of a single [CopyItem operation](copyitem-operation.md) request.</span></span> 
  
```xml
<CopyItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CopyItemResponseMessage>
```

 <span data-ttu-id="5c6c4-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c6c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-106">Attributes and elements</span></span>

<span data-ttu-id="5c6c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c6c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c6c4-108">Attributes</span></span>

|<span data-ttu-id="5c6c4-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-109">**Attribute**</span></span>|<span data-ttu-id="5c6c4-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c6c4-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5c6c4-112">Beschreibt den Status einer Antwort [CopyItem-Vorgang](copyitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6c4-112">Describes the status of a [CopyItem operation](copyitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="5c6c4-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="5c6c4-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="5c6c4-114">-Success</span><span class="sxs-lookup"><span data-stu-id="5c6c4-114">- Success</span></span>  <br/><span data-ttu-id="5c6c4-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="5c6c4-115">-  Warning</span></span>  <br/><span data-ttu-id="5c6c4-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="5c6c4-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="5c6c4-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5c6c4-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="5c6c4-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-118">**Value**</span></span>|<span data-ttu-id="5c6c4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c6c4-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-120">**Success**</span></span> <br/> |<span data-ttu-id="5c6c4-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5c6c4-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-122">**Warning**</span></span> <br/> | <span data-ttu-id="5c6c4-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-123">Describes a request that was not processed.</span></span> <span data-ttu-id="5c6c4-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="5c6c4-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="5c6c4-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="5c6c4-126">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-126">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="5c6c4-127">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="5c6c4-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="5c6c4-129">-Die Postfachdatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-129">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="5c6c4-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="5c6c4-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="5c6c4-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-132">**Error**</span></span> <br/> | <span data-ttu-id="5c6c4-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="5c6c4-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="5c6c4-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="5c6c4-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-135">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="5c6c4-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="5c6c4-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="5c6c4-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="5c6c4-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="5c6c4-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="5c6c4-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="5c6c4-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5c6c4-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="5c6c4-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="5c6c4-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c6c4-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-142">Child elements</span></span>

|<span data-ttu-id="5c6c4-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-143">**Element**</span></span>|<span data-ttu-id="5c6c4-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c6c4-145">- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="5c6c4-145">- [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)</span></span> <br/> [<span data-ttu-id="5c6c4-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="5c6c4-146">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5c6c4-147">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-147">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5c6c4-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5c6c4-148">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5c6c4-149">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-149">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5c6c4-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5c6c4-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5c6c4-151">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-151">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="5c6c4-152">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-152">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5c6c4-153">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5c6c4-153">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5c6c4-154">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-154">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5c6c4-155">Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-155">Items</span></span>](items.md) <br/> |<span data-ttu-id="5c6c4-156">Enthält ein Array der kopierten Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-156">Contains an array of copied items</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c6c4-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c6c4-157">Parent elements</span></span>

|<span data-ttu-id="5c6c4-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-158">**Element**</span></span>|<span data-ttu-id="5c6c4-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c6c4-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c6c4-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5c6c4-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5c6c4-161">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c6c4-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c6c4-162">Remarks</span></span>

<span data-ttu-id="5c6c4-163">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c6c4-164">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5c6c4-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c6c4-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c6c4-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5c6c4-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5c6c4-166">Schema name</span></span>  <br/> |<span data-ttu-id="5c6c4-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5c6c4-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5c6c4-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5c6c4-168">Validation file</span></span>  <br/> |<span data-ttu-id="5c6c4-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5c6c4-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c6c4-170">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5c6c4-170">Can be empty</span></span>  <br/> |<span data-ttu-id="5c6c4-171">False</span><span class="sxs-lookup"><span data-stu-id="5c6c4-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c6c4-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c6c4-172">See also</span></span>

- [<span data-ttu-id="5c6c4-173">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="5c6c4-173">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="5c6c4-174">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="5c6c4-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

