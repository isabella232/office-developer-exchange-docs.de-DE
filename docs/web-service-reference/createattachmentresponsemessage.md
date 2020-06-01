---
title: CreateAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponseMessage
api_type:
- schema
ms.assetid: b326e616-3ce0-4dcb-ba75-4ce4b9867211
description: Das CreateAttachmentResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateAttachment-Vorgangsanforderung.
ms.openlocfilehash: 14d8d1936b3cfd52bdb816343c86606cb8ccf76f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458922"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="2c8a8-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c8a8-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="2c8a8-104">Das **CreateAttachmentResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CreateAttachment-Vorgangs](createattachment-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2c8a8-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="2c8a8-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="2c8a8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2c8a8-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="2c8a8-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c8a8-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="2c8a8-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2c8a8-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c8a8-109">Attributes and elements</span></span>

<span data-ttu-id="2c8a8-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c8a8-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c8a8-111">Attributes</span></span>

|<span data-ttu-id="2c8a8-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-112">**Attribute**</span></span>|<span data-ttu-id="2c8a8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c8a8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2c8a8-115">Beschreibt den Status einer [CreateAttachment-Vorgangs](createattachment-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="2c8a8-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="2c8a8-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="2c8a8-117">-Success</span><span class="sxs-lookup"><span data-stu-id="2c8a8-117">-  Success</span></span>  <br/><span data-ttu-id="2c8a8-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="2c8a8-118">-  Warning</span></span>  <br/><span data-ttu-id="2c8a8-119">-Error</span><span class="sxs-lookup"><span data-stu-id="2c8a8-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2c8a8-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="2c8a8-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="2c8a8-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-121">**Value**</span></span>|<span data-ttu-id="2c8a8-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c8a8-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-123">**Success**</span></span> <br/> |<span data-ttu-id="2c8a8-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2c8a8-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-125">**Warning**</span></span> <br/> | <span data-ttu-id="2c8a8-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-126">Describes a request that was not processed.</span></span> <span data-ttu-id="2c8a8-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="2c8a8-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="2c8a8-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="2c8a8-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="2c8a8-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="2c8a8-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="2c8a8-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="2c8a8-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="2c8a8-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="2c8a8-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-135">**Error**</span></span> <br/> | <span data-ttu-id="2c8a8-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="2c8a8-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="2c8a8-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2c8a8-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="2c8a8-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="2c8a8-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="2c8a8-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="2c8a8-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="2c8a8-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="2c8a8-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="2c8a8-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="2c8a8-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="2c8a8-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="2c8a8-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="2c8a8-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="2c8a8-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="2c8a8-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c8a8-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c8a8-145">Child elements</span></span>

|<span data-ttu-id="2c8a8-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-146">**Element**</span></span>|<span data-ttu-id="2c8a8-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c8a8-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="2c8a8-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2c8a8-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2c8a8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c8a8-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2c8a8-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2c8a8-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2c8a8-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2c8a8-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2c8a8-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2c8a8-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="2c8a8-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2c8a8-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2c8a8-157">Anlagen</span><span class="sxs-lookup"><span data-stu-id="2c8a8-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2c8a8-158">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c8a8-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c8a8-159">Parent elements</span></span>

|<span data-ttu-id="2c8a8-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-160">**Element**</span></span>|<span data-ttu-id="2c8a8-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c8a8-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c8a8-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2c8a8-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2c8a8-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c8a8-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c8a8-164">Remarks</span></span>

<span data-ttu-id="2c8a8-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c8a8-166">Wenn mehrere Anlagen an ein Element in einem einzelnen Roundtrip angefügt werden, ist das **RootItemChangeKey** -Attribut in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, das die Anlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="2c8a8-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2c8a8-167">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2c8a8-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c8a8-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c8a8-168">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2c8a8-169">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c8a8-169">Schema Name</span></span>  <br/> |<span data-ttu-id="2c8a8-170">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2c8a8-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2c8a8-171">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c8a8-171">Validation File</span></span>  <br/> |<span data-ttu-id="2c8a8-172">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2c8a8-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2c8a8-173">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2c8a8-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c8a8-174">False</span><span class="sxs-lookup"><span data-stu-id="2c8a8-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c8a8-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c8a8-175">See also</span></span>

- [<span data-ttu-id="2c8a8-176">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c8a8-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="2c8a8-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="2c8a8-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="2c8a8-178">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="2c8a8-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="2c8a8-179">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c8a8-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

