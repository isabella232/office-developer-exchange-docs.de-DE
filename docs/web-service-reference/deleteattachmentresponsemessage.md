---
title: DeleteAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachmentResponseMessage
api_type:
- schema
ms.assetid: 1edb085f-1674-48e5-8ec3-42351adeac7d
description: Das DeleteAttachmentResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen DeleteAttachment--Vorgangsanforderung.
ms.openlocfilehash: 3ff253a5c2b6cbd69b7b976f7f41ca8b83814a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464259"
---
# <a name="deleteattachmentresponsemessage"></a><span data-ttu-id="6fa2f-103">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6fa2f-103">DeleteAttachmentResponseMessage</span></span>

<span data-ttu-id="6fa2f-104">Das **DeleteAttachmentResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [DeleteAttachment--Vorgangs](deleteattachment-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-104">The **DeleteAttachmentResponseMessage** element contains the status and result of a single [DeleteAttachment operation](deleteattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="6fa2f-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="6fa2f-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)  
- [<span data-ttu-id="6fa2f-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6fa2f-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="6fa2f-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6fa2f-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
```xml
<DeleteAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootItemId/>
</DeleteAttachmentResponseMessage>
```

<span data-ttu-id="6fa2f-108">**DeleteAttachmentResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-108">**DeleteAttachmentResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6fa2f-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fa2f-109">Attributes and elements</span></span>

<span data-ttu-id="6fa2f-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fa2f-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fa2f-111">Attributes</span></span>

|<span data-ttu-id="6fa2f-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-112">**Attribute**</span></span>|<span data-ttu-id="6fa2f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6fa2f-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6fa2f-115">Beschreibt den Status einer [DeleteAttachment--Vorgangs](deleteattachment-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-115">Describes the status of a [DeleteAttachment operation](deleteattachment-operation.md) response.</span></span><br/><br/><span data-ttu-id="6fa2f-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="6fa2f-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="6fa2f-117">-Success</span><span class="sxs-lookup"><span data-stu-id="6fa2f-117">-  Success</span></span>  <br/><span data-ttu-id="6fa2f-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="6fa2f-118">-  Warning</span></span>  <br/><span data-ttu-id="6fa2f-119">-Error</span><span class="sxs-lookup"><span data-stu-id="6fa2f-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6fa2f-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="6fa2f-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="6fa2f-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-121">**Value**</span></span>|<span data-ttu-id="6fa2f-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6fa2f-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-123">**Success**</span></span> <br/> |<span data-ttu-id="6fa2f-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6fa2f-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-125">**Warning**</span></span> <br/> | <span data-ttu-id="6fa2f-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-126">Describes a request that was not processed.</span></span> <span data-ttu-id="6fa2f-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="6fa2f-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="6fa2f-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="6fa2f-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-129">- The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="6fa2f-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="6fa2f-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="6fa2f-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="6fa2f-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="6fa2f-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="6fa2f-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-135">**Error**</span></span> <br/> | <span data-ttu-id="6fa2f-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="6fa2f-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="6fa2f-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="6fa2f-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="6fa2f-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6fa2f-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="6fa2f-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="6fa2f-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="6fa2f-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="6fa2f-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="6fa2f-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="6fa2f-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="6fa2f-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6fa2f-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="6fa2f-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="6fa2f-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa2f-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6fa2f-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fa2f-145">Child elements</span></span>

|<span data-ttu-id="6fa2f-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-146">**Element**</span></span>|<span data-ttu-id="6fa2f-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fa2f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="6fa2f-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6fa2f-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6fa2f-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6fa2f-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6fa2f-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6fa2f-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6fa2f-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6fa2f-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="6fa2f-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6fa2f-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="6fa2f-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6fa2f-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6fa2f-157">RootItemId</span><span class="sxs-lookup"><span data-stu-id="6fa2f-157">RootItemId</span></span>](rootitemid.md) <br/> |<span data-ttu-id="6fa2f-158">Gibt das übergeordnete Element einer gelöschten Anlage an.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-158">Identifies the parent item of a deleted attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6fa2f-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fa2f-159">Parent elements</span></span>

|<span data-ttu-id="6fa2f-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-160">**Element**</span></span>|<span data-ttu-id="6fa2f-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fa2f-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6fa2f-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6fa2f-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6fa2f-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6fa2f-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fa2f-164">Remarks</span></span>

<span data-ttu-id="6fa2f-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6fa2f-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fa2f-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6fa2f-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fa2f-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fa2f-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6fa2f-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6fa2f-168">Schema Name</span></span>  <br/> |<span data-ttu-id="6fa2f-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6fa2f-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6fa2f-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6fa2f-170">Validation File</span></span>  <br/> |<span data-ttu-id="6fa2f-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6fa2f-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6fa2f-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6fa2f-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="6fa2f-173">False</span><span class="sxs-lookup"><span data-stu-id="6fa2f-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fa2f-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fa2f-174">See also</span></span>

- [<span data-ttu-id="6fa2f-175">DeleteAttachment-</span><span class="sxs-lookup"><span data-stu-id="6fa2f-175">DeleteAttachment</span></span>](deleteattachment.md) 
- [<span data-ttu-id="6fa2f-176">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6fa2f-176">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="6fa2f-177">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="6fa2f-177">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="6fa2f-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6fa2f-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

