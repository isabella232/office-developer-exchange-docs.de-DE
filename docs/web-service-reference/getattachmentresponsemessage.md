---
title: GetAttachmentResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachmentResponseMessage
api_type:
- schema
ms.assetid: f0a841af-422d-4c82-b710-41e2038dbee4
description: Das GetAttachmentResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen GetAttachment-Vorgangsanforderung.
ms.openlocfilehash: cfe36364431a8fe81c3f62e68356b634f00bee78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457795"
---
# <a name="getattachmentresponsemessage"></a><span data-ttu-id="12918-103">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="12918-103">GetAttachmentResponseMessage</span></span>

<span data-ttu-id="12918-104">Das **GetAttachmentResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [GetAttachment-Vorgangs](getattachment-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="12918-104">The **GetAttachmentResponseMessage** element contains the status and result of a single [GetAttachment operation](getattachment-operation.md) request.</span></span> 
  
- [<span data-ttu-id="12918-105">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="12918-105">GetAttachmentResponse</span></span>](getattachmentresponse.md) 
- [<span data-ttu-id="12918-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="12918-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="12918-107">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="12918-107">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
  
```xml
<GetAttachmentResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Attachments/>
</GetAttachmentResponseMessage>
```

 <span data-ttu-id="12918-108">**AttachmentInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="12918-108">**AttachmentInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12918-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="12918-109">Attributes and elements</span></span>

<span data-ttu-id="12918-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="12918-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12918-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="12918-111">Attributes</span></span>

|<span data-ttu-id="12918-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="12918-112">**Attribute**</span></span>|<span data-ttu-id="12918-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12918-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12918-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="12918-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="12918-115">Beschreibt den Status einer [GetAttachment-Vorgangs](getattachment-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="12918-115">Describes the status of a [GetAttachment operation](getattachment-operation.md) response.</span></span><br/><br/> <span data-ttu-id="12918-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="12918-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="12918-117">-Success</span><span class="sxs-lookup"><span data-stu-id="12918-117">-  Success</span></span>  <br/><span data-ttu-id="12918-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="12918-118">-  Warning</span></span>  <br/><span data-ttu-id="12918-119">-Error</span><span class="sxs-lookup"><span data-stu-id="12918-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="12918-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="12918-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="12918-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="12918-121">**Value**</span></span>|<span data-ttu-id="12918-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12918-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12918-123">Erfolg</span><span class="sxs-lookup"><span data-stu-id="12918-123">Success</span></span>  <br/> |<span data-ttu-id="12918-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="12918-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="12918-125">Warnung</span><span class="sxs-lookup"><span data-stu-id="12918-125">Warning</span></span>  <br/> | <span data-ttu-id="12918-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="12918-126">Describes a request that was not processed.</span></span> <span data-ttu-id="12918-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="12918-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="12918-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="12918-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="12918-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="12918-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="12918-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="12918-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="12918-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="12918-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="12918-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="12918-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="12918-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="12918-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="12918-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="12918-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="12918-135">Fehler (ungefährer Wortlaut)</span><span class="sxs-lookup"><span data-stu-id="12918-135">Error</span></span>  <br/> | <span data-ttu-id="12918-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="12918-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="12918-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="12918-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="12918-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="12918-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="12918-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="12918-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="12918-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="12918-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="12918-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="12918-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="12918-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="12918-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="12918-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="12918-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="12918-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="12918-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="12918-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12918-145">Child elements</span></span>

|<span data-ttu-id="12918-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="12918-146">**Element**</span></span>|<span data-ttu-id="12918-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12918-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12918-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="12918-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="12918-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="12918-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="12918-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="12918-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="12918-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="12918-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="12918-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="12918-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="12918-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="12918-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="12918-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="12918-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="12918-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="12918-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="12918-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="12918-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="12918-157">Anlagen</span><span class="sxs-lookup"><span data-stu-id="12918-157">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="12918-158">Enthält die Elemente oder Dateien, die für ein Element in der Exchange-Informationsspeicher ttached sind.</span><span class="sxs-lookup"><span data-stu-id="12918-158">Contains the items or files that are ttached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12918-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="12918-159">Parent elements</span></span>

|<span data-ttu-id="12918-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="12918-160">**Element**</span></span>|<span data-ttu-id="12918-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="12918-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12918-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="12918-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="12918-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="12918-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12918-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12918-164">Remarks</span></span>

<span data-ttu-id="12918-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="12918-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12918-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="12918-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12918-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="12918-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="12918-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="12918-168">Schema Name</span></span>  <br/> |<span data-ttu-id="12918-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="12918-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="12918-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="12918-170">Validation File</span></span>  <br/> |<span data-ttu-id="12918-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="12918-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="12918-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="12918-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="12918-173">False</span><span class="sxs-lookup"><span data-stu-id="12918-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12918-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12918-174">See also</span></span>

- [<span data-ttu-id="12918-175">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="12918-175">GetAttachment</span></span>](getattachment.md) 
- [<span data-ttu-id="12918-176">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="12918-176">GetAttachment operation</span></span>](getattachment-operation.md)

