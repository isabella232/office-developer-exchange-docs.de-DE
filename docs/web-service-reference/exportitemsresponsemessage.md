---
title: ExportItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItemsResponseMessage
api_type:
- schema
ms.assetid: 830fb008-3c45-4988-9041-91a3da3fe689
description: Das ExportItemsResponseMessage-Element enthält den Status und die Ergebnisse einer Anforderung zum Exportieren eines einzelnen Post Fach Elements.
ms.openlocfilehash: 3265836ce6d9d6ef97a4e598bbb3f50e7c5047c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468946"
---
# <a name="exportitemsresponsemessage"></a><span data-ttu-id="491b4-103">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="491b4-103">ExportItemsResponseMessage</span></span>

<span data-ttu-id="491b4-104">Das **ExportItemsResponseMessage** -Element enthält den Status und die Ergebnisse einer Anforderung zum Exportieren eines einzelnen Post Fach Elements.</span><span class="sxs-lookup"><span data-stu-id="491b4-104">The **ExportItemsResponseMessage** element contains the status and results of a request to export a single mailbox item.</span></span> 
  
- [<span data-ttu-id="491b4-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="491b4-105">ExportItemsResponse</span></span>](exportitemsresponse.md)  
- [<span data-ttu-id="491b4-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="491b4-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="491b4-107">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="491b4-107">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
  
```XML
<ExportItemsResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ItemId/>
   <Data/>
</ExportItemsResponseMessage>
```

<span data-ttu-id="491b4-108">**ExportItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="491b4-108">**ExportItemsResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="491b4-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="491b4-109">Attributes and elements</span></span>

<span data-ttu-id="491b4-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="491b4-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="491b4-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="491b4-111">Attributes</span></span>

|<span data-ttu-id="491b4-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="491b4-112">**Attribute**</span></span>|<span data-ttu-id="491b4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="491b4-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="491b4-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="491b4-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="491b4-115">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="491b4-115">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="491b4-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="491b4-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="491b4-117">-Success</span><span class="sxs-lookup"><span data-stu-id="491b4-117">-  Success</span></span>  <br/><span data-ttu-id="491b4-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="491b4-118">-  Warning</span></span>  <br/><span data-ttu-id="491b4-119">-Error</span><span class="sxs-lookup"><span data-stu-id="491b4-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="491b4-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="491b4-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="491b4-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="491b4-121">**Value**</span></span>|<span data-ttu-id="491b4-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="491b4-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="491b4-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="491b4-123">**Success**</span></span> <br/> |<span data-ttu-id="491b4-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="491b4-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="491b4-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="491b4-125">**Warning**</span></span> <br/> | <span data-ttu-id="491b4-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="491b4-126">Describes a request that was not processed.</span></span> <span data-ttu-id="491b4-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="491b4-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="491b4-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="491b4-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="491b4-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="491b4-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="491b4-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="491b4-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="491b4-131">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="491b4-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="491b4-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="491b4-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="491b4-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="491b4-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="491b4-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="491b4-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="491b4-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="491b4-135">**Error**</span></span> <br/> | <span data-ttu-id="491b4-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="491b4-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="491b4-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="491b4-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="491b4-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="491b4-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="491b4-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="491b4-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="491b4-140">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="491b4-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="491b4-141">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="491b4-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="491b4-142">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="491b4-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="491b4-143">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="491b4-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="491b4-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="491b4-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="491b4-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="491b4-145">Child elements</span></span>

|<span data-ttu-id="491b4-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="491b4-146">**Element**</span></span>|<span data-ttu-id="491b4-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="491b4-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="491b4-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="491b4-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="491b4-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="491b4-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="491b4-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="491b4-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="491b4-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="491b4-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="491b4-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="491b4-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="491b4-153">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="491b4-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="491b4-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="491b4-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="491b4-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="491b4-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="491b4-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="491b4-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="491b4-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="491b4-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="491b4-158">Enthält den Elementbezeichner eines exportierten Elements.</span><span class="sxs-lookup"><span data-stu-id="491b4-158">Contains the item identifier of an exported item.</span></span>  <br/> |
|[<span data-ttu-id="491b4-159">Data (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="491b4-159">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="491b4-160">Enthält den Inhalt eines exportierten Elements.</span><span class="sxs-lookup"><span data-stu-id="491b4-160">Contains the contents of an exported item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="491b4-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="491b4-161">Parent elements</span></span>

|<span data-ttu-id="491b4-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="491b4-162">**Element**</span></span>|<span data-ttu-id="491b4-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="491b4-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="491b4-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="491b4-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="491b4-165">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="491b4-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="491b4-166">Textwert</span><span class="sxs-lookup"><span data-stu-id="491b4-166">Text value</span></span>

<span data-ttu-id="491b4-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="491b4-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="491b4-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="491b4-168">Remarks</span></span>

<span data-ttu-id="491b4-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="491b4-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="491b4-170">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="491b4-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="491b4-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="491b4-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="491b4-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="491b4-172">Schema Name</span></span>  <br/> |<span data-ttu-id="491b4-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="491b4-173">Message schema</span></span>  <br/> |
|<span data-ttu-id="491b4-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="491b4-174">Validation File</span></span>  <br/> |<span data-ttu-id="491b4-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="491b4-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="491b4-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="491b4-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="491b4-177">False</span><span class="sxs-lookup"><span data-stu-id="491b4-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="491b4-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="491b4-178">See also</span></span>

- [<span data-ttu-id="491b4-179">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="491b4-179">ExportItems operation</span></span>](exportitems-operation.md) 
- [<span data-ttu-id="491b4-180">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="491b4-180">UploadItems operation</span></span>](uploaditems-operation.md)

