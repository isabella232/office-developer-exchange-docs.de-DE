---
title: GetItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItemResponseMessage
api_type:
- schema
ms.assetid: cc583723-54d1-4a17-8c1f-6586f70fdefd
description: Das GetItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetItem Operation.
ms.openlocfilehash: 0c8527258d4637ede053e189dfb918b910c859d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758726"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="458b1-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="458b1-103">GetItemResponseMessage</span></span>

<span data-ttu-id="458b1-104">Das **GetItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetItem Operation](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="458b1-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="458b1-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="458b1-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="458b1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="458b1-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="458b1-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="458b1-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="458b1-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="458b1-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="458b1-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="458b1-109">Attributes and elements</span></span>

<span data-ttu-id="458b1-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="458b1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="458b1-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="458b1-111">Attributes</span></span>

|<span data-ttu-id="458b1-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="458b1-112">**Attribute**</span></span>|<span data-ttu-id="458b1-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458b1-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="458b1-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="458b1-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="458b1-115">Beschreibt den Status einer Antwort [GetItem Operation](getitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="458b1-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="458b1-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="458b1-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="458b1-117">-Success</span><span class="sxs-lookup"><span data-stu-id="458b1-117">- Success</span></span><br/><span data-ttu-id="458b1-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="458b1-118">- Warning</span></span><br/><span data-ttu-id="458b1-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="458b1-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="458b1-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="458b1-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="458b1-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="458b1-121">**Value**</span></span>|<span data-ttu-id="458b1-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458b1-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="458b1-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="458b1-123">**Success**</span></span> <br/> |<span data-ttu-id="458b1-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="458b1-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="458b1-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="458b1-125">**Warning**</span></span> <br/> | <span data-ttu-id="458b1-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="458b1-126">Describes a request that was not processed.</span></span> <span data-ttu-id="458b1-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="458b1-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="458b1-128">Es folgen Beispiele für Datenquellen für Warnungen:</span><span class="sxs-lookup"><span data-stu-id="458b1-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="458b1-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="458b1-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="458b1-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="458b1-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="458b1-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="458b1-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="458b1-132">-MDB ist offline.</span><span class="sxs-lookup"><span data-stu-id="458b1-132">- MDB is offline.</span></span><br/><span data-ttu-id="458b1-133">-Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="458b1-133">- Password is expired.</span></span>  <br/><span data-ttu-id="458b1-134">-Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="458b1-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="458b1-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="458b1-135">**Error**</span></span> <br/> | <span data-ttu-id="458b1-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="458b1-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="458b1-137">Es folgen Beispiele für Datenquellen für Fehler:</span><span class="sxs-lookup"><span data-stu-id="458b1-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="458b1-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="458b1-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="458b1-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="458b1-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="458b1-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="458b1-140">- Unknown tag</span></span><br/><span data-ttu-id="458b1-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="458b1-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="458b1-142">-Nicht autorisierten Zugriff von jedem Client versucht</span><span class="sxs-lookup"><span data-stu-id="458b1-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="458b1-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="458b1-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="458b1-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="458b1-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="458b1-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="458b1-145">Child elements</span></span>

|<span data-ttu-id="458b1-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="458b1-146">**Element**</span></span>|<span data-ttu-id="458b1-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458b1-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458b1-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="458b1-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="458b1-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="458b1-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="458b1-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="458b1-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="458b1-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="458b1-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="458b1-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="458b1-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="458b1-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="458b1-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="458b1-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="458b1-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="458b1-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="458b1-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="458b1-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="458b1-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="458b1-157">Elemente</span><span class="sxs-lookup"><span data-stu-id="458b1-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="458b1-158">Enthält ein Array der zurückgegebenen Elemente an.</span><span class="sxs-lookup"><span data-stu-id="458b1-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="458b1-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="458b1-159">Parent elements</span></span>

|<span data-ttu-id="458b1-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="458b1-160">**Element**</span></span>|<span data-ttu-id="458b1-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458b1-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458b1-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="458b1-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="458b1-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="458b1-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="458b1-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="458b1-164">Remarks</span></span>

<span data-ttu-id="458b1-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="458b1-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="458b1-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="458b1-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="458b1-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="458b1-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="458b1-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="458b1-168">Schema Name</span></span>  <br/> |<span data-ttu-id="458b1-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="458b1-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="458b1-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="458b1-170">Validation File</span></span>  <br/> |<span data-ttu-id="458b1-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="458b1-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="458b1-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="458b1-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="458b1-173">False</span><span class="sxs-lookup"><span data-stu-id="458b1-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="458b1-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="458b1-174">See also</span></span>

- [<span data-ttu-id="458b1-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="458b1-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="458b1-176">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="458b1-176">GetItem operation</span></span>](getitem-operation.md)

