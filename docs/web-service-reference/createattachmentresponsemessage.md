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
description: Das CreateAttachmentResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CreateAttachment Vorgang.
ms.openlocfilehash: a6d3adde07dedb7a2533d6e9c7fc6ff0497792bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757750"
---
# <a name="createattachmentresponsemessage"></a><span data-ttu-id="4946e-103">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4946e-103">CreateAttachmentResponseMessage</span></span>

<span data-ttu-id="4946e-104">Das **CreateAttachmentResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CreateAttachment Vorgang](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4946e-104">The **CreateAttachmentResponseMessage** element contains the status and result of a single [CreateAttachment operation](createattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="4946e-105">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="4946e-105">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
- [<span data-ttu-id="4946e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4946e-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="4946e-107">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4946e-107">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
  
```xml
<CreateAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</CreateAttachmentResponseMessage>
```

<span data-ttu-id="4946e-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4946e-108">**AttachmentInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4946e-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4946e-109">Attributes and elements</span></span>

<span data-ttu-id="4946e-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4946e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4946e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="4946e-111">Attributes</span></span>

|<span data-ttu-id="4946e-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4946e-112">**Attribute**</span></span>|<span data-ttu-id="4946e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4946e-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4946e-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4946e-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4946e-115">Beschreibt den Status einer Antwort [CreateAttachment Vorgang](createattachment-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4946e-115">Describes the status of a [CreateAttachment operation](createattachment-operation.md) response.</span></span> <br/><br/><span data-ttu-id="4946e-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="4946e-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="4946e-117">-Success</span><span class="sxs-lookup"><span data-stu-id="4946e-117">-  Success</span></span>  <br/><span data-ttu-id="4946e-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="4946e-118">-  Warning</span></span>  <br/><span data-ttu-id="4946e-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="4946e-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4946e-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4946e-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="4946e-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4946e-121">**Value**</span></span>|<span data-ttu-id="4946e-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4946e-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4946e-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="4946e-123">**Success**</span></span> <br/> |<span data-ttu-id="4946e-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="4946e-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4946e-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4946e-125">**Warning**</span></span> <br/> | <span data-ttu-id="4946e-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4946e-126">Describes a request that was not processed.</span></span> <span data-ttu-id="4946e-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="4946e-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="4946e-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="4946e-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="4946e-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="4946e-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4946e-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4946e-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4946e-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="4946e-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="4946e-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="4946e-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4946e-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="4946e-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="4946e-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="4946e-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="4946e-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="4946e-135">**Error**</span></span> <br/> | <span data-ttu-id="4946e-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4946e-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="4946e-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="4946e-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="4946e-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="4946e-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="4946e-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="4946e-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="4946e-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="4946e-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="4946e-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4946e-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="4946e-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="4946e-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4946e-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="4946e-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="4946e-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4946e-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4946e-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4946e-145">Child elements</span></span>

|<span data-ttu-id="4946e-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="4946e-146">**Element**</span></span>|<span data-ttu-id="4946e-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4946e-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4946e-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="4946e-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4946e-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="4946e-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4946e-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4946e-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4946e-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="4946e-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4946e-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4946e-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4946e-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4946e-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="4946e-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="4946e-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4946e-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4946e-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4946e-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="4946e-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4946e-157">Anlagen</span><span class="sxs-lookup"><span data-stu-id="4946e-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4946e-158">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4946e-158">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4946e-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4946e-159">Parent elements</span></span>

|<span data-ttu-id="4946e-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="4946e-160">**Element**</span></span>|<span data-ttu-id="4946e-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4946e-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4946e-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4946e-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4946e-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4946e-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4946e-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4946e-164">Remarks</span></span>

<span data-ttu-id="4946e-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4946e-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4946e-166">Wenn mehrere Anlagen Roundtrip zu einem Element in einem einzigen angefügt sind, ist das **RootItemChangeKey** -Attribut in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, die Anlagen wurde.</span><span class="sxs-lookup"><span data-stu-id="4946e-166">If multiple attachments are attached to an item in a single round trip, the **RootItemChangeKey** attribute in the last response message is the one that represents the new change key of the item that has the attachments.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4946e-167">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4946e-167">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4946e-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="4946e-168">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4946e-169">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4946e-169">Schema Name</span></span>  <br/> |<span data-ttu-id="4946e-170">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4946e-170">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4946e-171">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4946e-171">Validation File</span></span>  <br/> |<span data-ttu-id="4946e-172">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4946e-172">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4946e-173">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4946e-173">Can be Empty</span></span>  <br/> |<span data-ttu-id="4946e-174">False</span><span class="sxs-lookup"><span data-stu-id="4946e-174">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4946e-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4946e-175">See also</span></span>

- [<span data-ttu-id="4946e-176">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4946e-176">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="4946e-177">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="4946e-177">CreateAttachment</span></span>](createattachment.md)
- [<span data-ttu-id="4946e-178">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="4946e-178">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="4946e-179">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4946e-179">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

