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
description: Das ExportItemsResponseMessage-Element enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach-Element zu exportieren.
ms.openlocfilehash: 99c2ca3f95efff6562ff95350b30fc79c5fb51e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758327"
---
# <a name="exportitemsresponsemessage"></a><span data-ttu-id="99362-103">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99362-103">ExportItemsResponseMessage</span></span>

<span data-ttu-id="99362-104">Das **ExportItemsResponseMessage** -Element enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach-Element zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="99362-104">The **ExportItemsResponseMessage** element contains the status and results of a request to export a single mailbox item.</span></span> 
  
- [<span data-ttu-id="99362-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="99362-105">ExportItemsResponse</span></span>](exportitemsresponse.md)  
- [<span data-ttu-id="99362-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="99362-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="99362-107">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99362-107">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md)
  
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

<span data-ttu-id="99362-108">**ExportItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="99362-108">**ExportItemsResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="99362-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99362-109">Attributes and elements</span></span>

<span data-ttu-id="99362-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99362-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99362-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="99362-111">Attributes</span></span>

|<span data-ttu-id="99362-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="99362-112">**Attribute**</span></span>|<span data-ttu-id="99362-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99362-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99362-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="99362-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="99362-115">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="99362-115">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="99362-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="99362-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="99362-117">-Success</span><span class="sxs-lookup"><span data-stu-id="99362-117">-  Success</span></span>  <br/><span data-ttu-id="99362-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="99362-118">-  Warning</span></span>  <br/><span data-ttu-id="99362-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="99362-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="99362-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="99362-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="99362-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="99362-121">**Value**</span></span>|<span data-ttu-id="99362-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99362-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99362-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="99362-123">**Success**</span></span> <br/> |<span data-ttu-id="99362-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="99362-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="99362-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="99362-125">**Warning**</span></span> <br/> | <span data-ttu-id="99362-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="99362-126">Describes a request that was not processed.</span></span> <span data-ttu-id="99362-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="99362-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="99362-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="99362-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="99362-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="99362-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="99362-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="99362-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="99362-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="99362-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="99362-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="99362-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="99362-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="99362-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="99362-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="99362-134">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="99362-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="99362-135">**Error**</span></span> <br/> | <span data-ttu-id="99362-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="99362-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="99362-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="99362-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="99362-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="99362-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="99362-139">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="99362-139">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="99362-140">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="99362-140">-  An unknown tag</span></span>  <br/><span data-ttu-id="99362-141">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="99362-141">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="99362-142">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="99362-142">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="99362-143">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="99362-143">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="99362-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="99362-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99362-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99362-145">Child elements</span></span>

|<span data-ttu-id="99362-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="99362-146">**Element**</span></span>|<span data-ttu-id="99362-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99362-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99362-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="99362-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="99362-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="99362-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="99362-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="99362-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="99362-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="99362-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="99362-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="99362-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="99362-153">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="99362-153">Currently unused and reserved for future use.</span></span> <span data-ttu-id="99362-154">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="99362-154">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="99362-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="99362-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="99362-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="99362-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="99362-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="99362-157">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="99362-158">Enthält die Element-ID eines Elements exportierten.</span><span class="sxs-lookup"><span data-stu-id="99362-158">Contains the item identifier of an exported item.</span></span>  <br/> |
|[<span data-ttu-id="99362-159">Daten (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="99362-159">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="99362-160">Enthält den Inhalt eines exportierten Elements.</span><span class="sxs-lookup"><span data-stu-id="99362-160">Contains the contents of an exported item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99362-161">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99362-161">Parent elements</span></span>

|<span data-ttu-id="99362-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="99362-162">**Element**</span></span>|<span data-ttu-id="99362-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99362-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99362-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="99362-164">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="99362-165">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99362-165">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="99362-166">Textwert</span><span class="sxs-lookup"><span data-stu-id="99362-166">Text value</span></span>

<span data-ttu-id="99362-167">Keine.</span><span class="sxs-lookup"><span data-stu-id="99362-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99362-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99362-168">Remarks</span></span>

<span data-ttu-id="99362-169">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="99362-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99362-170">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="99362-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99362-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="99362-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99362-172">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99362-172">Schema Name</span></span>  <br/> |<span data-ttu-id="99362-173">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="99362-173">Message schema</span></span>  <br/> |
|<span data-ttu-id="99362-174">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99362-174">Validation File</span></span>  <br/> |<span data-ttu-id="99362-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="99362-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99362-176">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="99362-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="99362-177">False</span><span class="sxs-lookup"><span data-stu-id="99362-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99362-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99362-178">See also</span></span>

- [<span data-ttu-id="99362-179">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99362-179">ExportItems operation</span></span>](exportitems-operation.md) 
- [<span data-ttu-id="99362-180">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99362-180">UploadItems operation</span></span>](uploaditems-operation.md)

