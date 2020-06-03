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
description: Das MoveItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen MoveItem-Vorgangsanforderung.
ms.openlocfilehash: fd96c34840acd5b6137a2a5d50980dc86202629f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530394"
---
# <a name="moveitemresponsemessage"></a><span data-ttu-id="64b73-103">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="64b73-103">MoveItemResponseMessage</span></span>

<span data-ttu-id="64b73-104">Das **MoveItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [MoveItem-Vorgangs](moveitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64b73-104">The **MoveItemResponseMessage** element contains the status and result of a single [MoveItem operation](moveitem-operation.md) request.</span></span> 
  
```xml
<MoveItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</MoveItemResponseMessage>
```

 <span data-ttu-id="64b73-105">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="64b73-105">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64b73-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="64b73-106">Attributes and elements</span></span>

<span data-ttu-id="64b73-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="64b73-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64b73-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="64b73-108">Attributes</span></span>

|<span data-ttu-id="64b73-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="64b73-109">**Attribute**</span></span>|<span data-ttu-id="64b73-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64b73-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64b73-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="64b73-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="64b73-112">Beschreibt den Status einer [MoveItem-Vorgangs](moveitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="64b73-112">Describes the status of a [MoveItem operation](moveitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="64b73-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="64b73-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="64b73-114">-Success</span><span class="sxs-lookup"><span data-stu-id="64b73-114">-  Success</span></span>  <br/><span data-ttu-id="64b73-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="64b73-115">-  Warning</span></span>  <br/><span data-ttu-id="64b73-116">-Error</span><span class="sxs-lookup"><span data-stu-id="64b73-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="64b73-117">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="64b73-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="64b73-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="64b73-118">**Value**</span></span>|<span data-ttu-id="64b73-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64b73-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64b73-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="64b73-120">**Success**</span></span> <br/> |<span data-ttu-id="64b73-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="64b73-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="64b73-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="64b73-122">**Warning**</span></span> <br/> | <span data-ttu-id="64b73-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="64b73-123">Describes a request that was not processed.</span></span> <span data-ttu-id="64b73-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="64b73-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="64b73-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="64b73-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="64b73-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="64b73-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="64b73-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="64b73-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="64b73-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="64b73-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="64b73-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="64b73-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="64b73-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="64b73-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="64b73-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="64b73-131">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="64b73-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="64b73-132">**Error**</span></span> <br/> | <span data-ttu-id="64b73-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="64b73-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="64b73-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="64b73-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="64b73-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="64b73-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="64b73-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="64b73-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="64b73-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="64b73-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="64b73-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="64b73-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="64b73-139">-Jeder nicht autorisierte Zugriff, der von einem Client versucht wird</span><span class="sxs-lookup"><span data-stu-id="64b73-139">-  Any unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="64b73-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="64b73-140">-  Any server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="64b73-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="64b73-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="64b73-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64b73-142">Child elements</span></span>

|<span data-ttu-id="64b73-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="64b73-143">**Element**</span></span>|<span data-ttu-id="64b73-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64b73-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64b73-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="64b73-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="64b73-146">Eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="64b73-146">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="64b73-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="64b73-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="64b73-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="64b73-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="64b73-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="64b73-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="64b73-150">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="64b73-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="64b73-151">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="64b73-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="64b73-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="64b73-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="64b73-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="64b73-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="64b73-154">Elemente</span><span class="sxs-lookup"><span data-stu-id="64b73-154">Items</span></span>](items.md) <br/> |<span data-ttu-id="64b73-155">Enthält ein Array von verschobenen Elementen.</span><span class="sxs-lookup"><span data-stu-id="64b73-155">Contains an array of moved items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64b73-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64b73-156">Parent elements</span></span>

|<span data-ttu-id="64b73-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="64b73-157">**Element**</span></span>|<span data-ttu-id="64b73-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64b73-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64b73-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="64b73-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="64b73-160">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="64b73-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64b73-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64b73-161">Remarks</span></span>

<span data-ttu-id="64b73-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="64b73-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64b73-163">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="64b73-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64b73-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="64b73-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="64b73-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="64b73-165">Schema Name</span></span>  <br/> |<span data-ttu-id="64b73-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="64b73-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="64b73-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="64b73-167">Validation File</span></span>  <br/> |<span data-ttu-id="64b73-168">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="64b73-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="64b73-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="64b73-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="64b73-170">False</span><span class="sxs-lookup"><span data-stu-id="64b73-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64b73-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64b73-171">See also</span></span>

- [<span data-ttu-id="64b73-172">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="64b73-172">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="64b73-173">MoveItem</span><span class="sxs-lookup"><span data-stu-id="64b73-173">MoveItem</span></span>](moveitem.md)

