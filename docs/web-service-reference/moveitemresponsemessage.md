---
title: MoveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItemResponseMessage
api_type:
- schema
ms.assetid: 1efacb2c-cb76-44ad-b0be-bb47bf2553be
description: Das MoveItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung MoveItem-Vorgang.
ms.openlocfilehash: af1c10391d9b5b761ab87983eea6321d61231152
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830493"
---
# <a name="moveitemresponsemessage"></a><span data-ttu-id="4938b-103">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4938b-103">MoveItemResponseMessage</span></span>

<span data-ttu-id="4938b-104">Das **MoveItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [MoveItem-Vorgang](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4938b-104">The **MoveItemResponseMessage** element contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.</span></span> 
  
```xml
<MoveItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</MoveItemResponseMessage>
```

 <span data-ttu-id="4938b-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4938b-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4938b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4938b-106">Attributes and elements</span></span>

<span data-ttu-id="4938b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4938b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4938b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4938b-108">Attributes</span></span>

|<span data-ttu-id="4938b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4938b-109">**Attribute**</span></span>|<span data-ttu-id="4938b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4938b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4938b-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4938b-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4938b-112">Beschreibt den Status einer Antwort [MoveItem-Vorgang](moveitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4938b-112">Describes the status of a [MoveItem operation](moveitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="4938b-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="4938b-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="4938b-114">-Success</span><span class="sxs-lookup"><span data-stu-id="4938b-114">-  Success</span></span>  <br/><span data-ttu-id="4938b-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="4938b-115">-  Warning</span></span>  <br/><span data-ttu-id="4938b-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="4938b-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="4938b-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="4938b-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="4938b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4938b-118">**Value**</span></span>|<span data-ttu-id="4938b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4938b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4938b-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="4938b-120">**Success**</span></span> <br/> |<span data-ttu-id="4938b-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="4938b-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4938b-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4938b-122">**Warning**</span></span> <br/> | <span data-ttu-id="4938b-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4938b-123">Describes a request that was not processed.</span></span> <span data-ttu-id="4938b-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="4938b-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="4938b-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="4938b-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="4938b-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="4938b-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4938b-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4938b-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4938b-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="4938b-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="4938b-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4938b-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4938b-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="4938b-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="4938b-131">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="4938b-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="4938b-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="4938b-132">**Error**</span></span> <br/> | <span data-ttu-id="4938b-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4938b-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4938b-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="4938b-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="4938b-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="4938b-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="4938b-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="4938b-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="4938b-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="4938b-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="4938b-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4938b-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="4938b-139">-Alle nicht autorisierten Zugriff von jedem Client versucht</span><span class="sxs-lookup"><span data-stu-id="4938b-139">-  Any unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="4938b-140">-Alle serverseitigen Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="4938b-140">-  Any server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="4938b-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4938b-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4938b-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4938b-142">Child elements</span></span>

|<span data-ttu-id="4938b-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="4938b-143">**Element**</span></span>|<span data-ttu-id="4938b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4938b-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4938b-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="4938b-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4938b-146">Beschreibender Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4938b-146">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4938b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4938b-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4938b-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="4938b-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4938b-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4938b-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4938b-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4938b-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="4938b-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="4938b-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4938b-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4938b-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4938b-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="4938b-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4938b-154">Elemente</span><span class="sxs-lookup"><span data-stu-id="4938b-154">Items</span></span>](items.md) <br/> |<span data-ttu-id="4938b-155">Ein Array von verschobene Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="4938b-155">Contains an array of moved items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4938b-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4938b-156">Parent elements</span></span>

|<span data-ttu-id="4938b-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="4938b-157">**Element**</span></span>|<span data-ttu-id="4938b-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4938b-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4938b-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4938b-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4938b-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4938b-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4938b-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4938b-161">Remarks</span></span>

<span data-ttu-id="4938b-162">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4938b-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4938b-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4938b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4938b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="4938b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4938b-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4938b-165">Schema Name</span></span>  <br/> |<span data-ttu-id="4938b-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4938b-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4938b-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4938b-167">Validation File</span></span>  <br/> |<span data-ttu-id="4938b-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4938b-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4938b-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4938b-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="4938b-170">False</span><span class="sxs-lookup"><span data-stu-id="4938b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4938b-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4938b-171">See also</span></span>

- [<span data-ttu-id="4938b-172">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="4938b-172">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="4938b-173">MoveItem</span><span class="sxs-lookup"><span data-stu-id="4938b-173">MoveItem</span></span>](moveitem.md)

