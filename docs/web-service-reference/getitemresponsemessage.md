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
description: Das GetItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetItem-Vorgangsanforderung.
ms.openlocfilehash: bd25a82641259e1546bad6eef5c2f6f8f03e98cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458670"
---
# <a name="getitemresponsemessage"></a><span data-ttu-id="48b5e-103">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="48b5e-103">GetItemResponseMessage</span></span>

<span data-ttu-id="48b5e-104">Das **GetItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetItem-Vorgangs](getitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48b5e-104">The **GetItemResponseMessage** element contains the status and result of a single [GetItem operation](getitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="48b5e-105">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="48b5e-105">GetItemResponse</span></span>](getitemresponse.md) 
- [<span data-ttu-id="48b5e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="48b5e-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="48b5e-107">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="48b5e-107">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
  
```xml
<GetItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</GetItemResponseMessage>
```

<span data-ttu-id="48b5e-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="48b5e-108">**ItemInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="48b5e-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="48b5e-109">Attributes and elements</span></span>

<span data-ttu-id="48b5e-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="48b5e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48b5e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="48b5e-111">Attributes</span></span>

|<span data-ttu-id="48b5e-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48b5e-112">**Attribute**</span></span>|<span data-ttu-id="48b5e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48b5e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48b5e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="48b5e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="48b5e-115">Beschreibt den Status einer [GetItem-Vorgangs](getitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="48b5e-115">Describes the status of a [GetItem operation](getitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="48b5e-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="48b5e-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="48b5e-117">-Success</span><span class="sxs-lookup"><span data-stu-id="48b5e-117">- Success</span></span><br/><span data-ttu-id="48b5e-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="48b5e-118">- Warning</span></span><br/><span data-ttu-id="48b5e-119">-Error</span><span class="sxs-lookup"><span data-stu-id="48b5e-119">- Error</span></span> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="48b5e-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="48b5e-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="48b5e-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="48b5e-121">**Value**</span></span>|<span data-ttu-id="48b5e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48b5e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48b5e-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="48b5e-123">**Success**</span></span> <br/> |<span data-ttu-id="48b5e-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="48b5e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="48b5e-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="48b5e-125">**Warning**</span></span> <br/> | <span data-ttu-id="48b5e-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="48b5e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="48b5e-127">Eine Warnung wird möglicherweise zurückgegeben, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="48b5e-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="48b5e-128">Im folgenden sind Beispiele für Quellen für Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="48b5e-128">The following are examples of sources for warnings:</span></span><br/><br/><span data-ttu-id="48b5e-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="48b5e-129">- The Exchange store is offline during the batch.</span></span><br/><span data-ttu-id="48b5e-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="48b5e-130">- Active Directory Domain Services (AD DS) is offline.</span></span><br/><span data-ttu-id="48b5e-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="48b5e-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="48b5e-132">-MDB ist offline.</span><span class="sxs-lookup"><span data-stu-id="48b5e-132">- MDB is offline.</span></span><br/><span data-ttu-id="48b5e-133">-Password ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="48b5e-133">- Password is expired.</span></span>  <br/><span data-ttu-id="48b5e-134">-Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="48b5e-134">- Quota is exceeded.</span></span> |
|<span data-ttu-id="48b5e-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="48b5e-135">**Error**</span></span> <br/> | <span data-ttu-id="48b5e-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="48b5e-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="48b5e-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="48b5e-137">The following are examples of sources for errors:</span></span><br/><br/><span data-ttu-id="48b5e-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="48b5e-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="48b5e-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="48b5e-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="48b5e-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="48b5e-140">- Unknown tag</span></span><br/><span data-ttu-id="48b5e-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="48b5e-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="48b5e-142">-Nicht autorisierter Zugriff durch einen Client versucht</span><span class="sxs-lookup"><span data-stu-id="48b5e-142">- Unauthorized access attempted by any client</span></span><br/><span data-ttu-id="48b5e-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="48b5e-143">- Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="48b5e-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="48b5e-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="48b5e-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48b5e-145">Child elements</span></span>

|<span data-ttu-id="48b5e-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="48b5e-146">**Element**</span></span>|<span data-ttu-id="48b5e-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48b5e-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48b5e-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="48b5e-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="48b5e-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="48b5e-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="48b5e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="48b5e-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="48b5e-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="48b5e-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="48b5e-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="48b5e-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="48b5e-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="48b5e-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="48b5e-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="48b5e-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="48b5e-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="48b5e-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="48b5e-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="48b5e-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="48b5e-157">Items</span><span class="sxs-lookup"><span data-stu-id="48b5e-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="48b5e-158">Enthält ein Array zurückgegebener Elemente.</span><span class="sxs-lookup"><span data-stu-id="48b5e-158">Contains an array of returned items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48b5e-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48b5e-159">Parent elements</span></span>

|<span data-ttu-id="48b5e-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="48b5e-160">**Element**</span></span>|<span data-ttu-id="48b5e-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48b5e-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48b5e-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="48b5e-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="48b5e-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="48b5e-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48b5e-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b5e-164">Remarks</span></span>

<span data-ttu-id="48b5e-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="48b5e-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48b5e-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="48b5e-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48b5e-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="48b5e-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="48b5e-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="48b5e-168">Schema Name</span></span>  <br/> |<span data-ttu-id="48b5e-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="48b5e-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="48b5e-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="48b5e-170">Validation File</span></span>  <br/> |<span data-ttu-id="48b5e-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="48b5e-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="48b5e-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="48b5e-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="48b5e-173">False</span><span class="sxs-lookup"><span data-stu-id="48b5e-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48b5e-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b5e-174">See also</span></span>

- [<span data-ttu-id="48b5e-175">GetItem</span><span class="sxs-lookup"><span data-stu-id="48b5e-175">GetItem</span></span>](getitem.md)
- [<span data-ttu-id="48b5e-176">GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="48b5e-176">GetItem operation</span></span>](getitem-operation.md)

