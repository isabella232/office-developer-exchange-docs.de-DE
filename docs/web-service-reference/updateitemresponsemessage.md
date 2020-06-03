---
title: UpdateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItemResponseMessage
api_type:
- schema
ms.assetid: dc585b05-5afc-4c74-8763-5a54f9a650ec
description: Das UpdateItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen UpdateItem-Vorgangsanforderung.
ms.openlocfilehash: ef25dcf26e06f199587cef885d8cbc9e93b52bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457942"
---
# <a name="updateitemresponsemessage"></a><span data-ttu-id="d896a-103">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d896a-103">UpdateItemResponseMessage</span></span>

<span data-ttu-id="d896a-104">Das **UpdateItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [UpdateItem-Vorgangs](updateitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d896a-104">The **UpdateItemResponseMessage** element contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="d896a-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="d896a-105">UpdateItemResponse</span></span>](updateitemresponse.md)
- [<span data-ttu-id="d896a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d896a-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="d896a-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d896a-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
```xml
<UpdateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
   <ConflictResults/>
</UpdateItemResponseMessage>
```

 <span data-ttu-id="d896a-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d896a-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d896a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d896a-109">Attributes and elements</span></span>

<span data-ttu-id="d896a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d896a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d896a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d896a-111">Attributes</span></span>

|<span data-ttu-id="d896a-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d896a-112">**Attribute**</span></span>|<span data-ttu-id="d896a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d896a-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d896a-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d896a-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d896a-115">Beschreibt den Status einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="d896a-115">Describes the status of an [UpdateItem operation](updateitem-operation.md) response.</span></span> <br/><br/><span data-ttu-id="d896a-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d896a-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d896a-117">-Success</span><span class="sxs-lookup"><span data-stu-id="d896a-117">-  Success</span></span>  <br/><span data-ttu-id="d896a-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d896a-118">-  Warning</span></span>  <br/><span data-ttu-id="d896a-119">-Error</span><span class="sxs-lookup"><span data-stu-id="d896a-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d896a-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="d896a-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="d896a-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d896a-121">**Value**</span></span>|<span data-ttu-id="d896a-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d896a-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d896a-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="d896a-123">**Success**</span></span> <br/> |<span data-ttu-id="d896a-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d896a-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d896a-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d896a-125">**Warning**</span></span> <br/> | <span data-ttu-id="d896a-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d896a-126">Describes a request that was not processed.</span></span> <span data-ttu-id="d896a-127">Eine Warnung wird möglicherweise zurückgegeben, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde und nachfolgende Elemente nicht verarbeitet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="d896a-127">A warning may be returned if an error occurred while an item in the request was processed and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="d896a-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d896a-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="d896a-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="d896a-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d896a-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d896a-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d896a-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="d896a-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="d896a-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d896a-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d896a-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d896a-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="d896a-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="d896a-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="d896a-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="d896a-135">**Error**</span></span> <br/> | <span data-ttu-id="d896a-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d896a-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d896a-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="d896a-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d896a-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="d896a-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="d896a-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="d896a-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="d896a-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="d896a-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="d896a-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="d896a-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="d896a-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="d896a-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="d896a-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="d896a-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="d896a-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d896a-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d896a-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d896a-145">Child elements</span></span>

|<span data-ttu-id="d896a-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="d896a-146">**Element**</span></span>|<span data-ttu-id="d896a-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d896a-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d896a-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="d896a-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="d896a-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d896a-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="d896a-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d896a-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="d896a-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d896a-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="d896a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d896a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="d896a-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d896a-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="d896a-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="d896a-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="d896a-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="d896a-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="d896a-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="d896a-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="d896a-157">Elemente</span><span class="sxs-lookup"><span data-stu-id="d896a-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="d896a-158">Enthält ein Array aktualisierter Elemente.</span><span class="sxs-lookup"><span data-stu-id="d896a-158">Contains an array of updated items.</span></span>  <br/> |
|[<span data-ttu-id="d896a-159">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="d896a-159">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="d896a-160">Enthält die Anzahl von Konflikten in einer [UpdateItem-Vorgangs](updateitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="d896a-160">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d896a-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d896a-161">Parent elements</span></span>

|<span data-ttu-id="d896a-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="d896a-162">**Element**</span></span>|<span data-ttu-id="d896a-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d896a-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d896a-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d896a-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d896a-165">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d896a-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d896a-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d896a-166">Remarks</span></span>

<span data-ttu-id="d896a-167">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d896a-167">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d896a-168">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d896a-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d896a-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="d896a-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d896a-170">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d896a-170">Schema Name</span></span>  <br/> |<span data-ttu-id="d896a-171">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d896a-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d896a-172">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d896a-172">Validation File</span></span>  <br/> |<span data-ttu-id="d896a-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d896a-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d896a-174">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d896a-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="d896a-175">False</span><span class="sxs-lookup"><span data-stu-id="d896a-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d896a-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d896a-176">See also</span></span>

- [<span data-ttu-id="d896a-177">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d896a-177">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="d896a-178">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="d896a-178">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="d896a-179">Aktualisieren von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="d896a-179">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

