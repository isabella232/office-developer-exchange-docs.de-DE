---
title: EmptyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 678dd5ce-8d9e-4939-bf1b-a8e148f4f449
description: Das EmptyFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen EmptyFolder-Anforderung.
ms.openlocfilehash: ebdaac28cdd16a55811276ef0d11c03b00d3897a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758213"
---
# <a name="emptyfolderresponsemessage"></a><span data-ttu-id="a0f04-103">EmptyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a0f04-103">EmptyFolderResponseMessage</span></span>

<span data-ttu-id="a0f04-104">Das **EmptyFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [EmptyFolder](emptyfolder.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a0f04-104">The **EmptyFolderResponseMessage** element contains the status and result of a single [EmptyFolder](emptyfolder.md) request.</span></span> 
  
```XML
<EmptyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</EmptyFolderResponseMessage>
```

 <span data-ttu-id="a0f04-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a0f04-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0f04-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0f04-106">Attributes and elements</span></span>

<span data-ttu-id="a0f04-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0f04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0f04-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0f04-108">Attributes</span></span>

|<span data-ttu-id="a0f04-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a0f04-109">**Attribute**</span></span>|<span data-ttu-id="a0f04-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0f04-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0f04-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="a0f04-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="a0f04-112">Beschreibt den Status einer Antwort [EmptyFolder-Vorgang](emptyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f04-112">Describes the status of an [EmptyFolder operation](emptyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="a0f04-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="a0f04-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="a0f04-114">-Success</span><span class="sxs-lookup"><span data-stu-id="a0f04-114">-  Success</span></span>  <br/><span data-ttu-id="a0f04-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="a0f04-115">-  Warning</span></span>  <br/><span data-ttu-id="a0f04-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="a0f04-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="a0f04-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="a0f04-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="a0f04-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a0f04-118">**Value**</span></span>|<span data-ttu-id="a0f04-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0f04-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0f04-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="a0f04-120">**Success**</span></span> <br/> |<span data-ttu-id="a0f04-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="a0f04-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="a0f04-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="a0f04-122">**Warning**</span></span> <br/> | <span data-ttu-id="a0f04-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a0f04-123">Describes a request that was not processed.</span></span> <span data-ttu-id="a0f04-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="a0f04-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="a0f04-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="a0f04-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="a0f04-126">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="a0f04-126">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="a0f04-127">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="a0f04-127">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="a0f04-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="a0f04-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="a0f04-129">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="a0f04-129">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="a0f04-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="a0f04-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="a0f04-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="a0f04-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="a0f04-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="a0f04-132">**Error**</span></span> <br/> | <span data-ttu-id="a0f04-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0f04-133">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="a0f04-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="a0f04-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="a0f04-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="a0f04-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="a0f04-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="a0f04-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="a0f04-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="a0f04-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="a0f04-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a0f04-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="a0f04-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="a0f04-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="a0f04-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="a0f04-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="a0f04-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a0f04-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0f04-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0f04-142">Child elements</span></span>

|<span data-ttu-id="a0f04-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0f04-143">**Element**</span></span>|<span data-ttu-id="a0f04-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0f04-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0f04-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="a0f04-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="a0f04-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="a0f04-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="a0f04-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a0f04-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="a0f04-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="a0f04-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="a0f04-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a0f04-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="a0f04-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a0f04-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="a0f04-151">Es enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="a0f04-151">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="a0f04-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="a0f04-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="a0f04-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="a0f04-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a0f04-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0f04-154">Parent elements</span></span>

|<span data-ttu-id="a0f04-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0f04-155">**Element**</span></span>|<span data-ttu-id="a0f04-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0f04-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0f04-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a0f04-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a0f04-158">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a0f04-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a0f04-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="a0f04-159">Text value</span></span>

<span data-ttu-id="a0f04-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="a0f04-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0f04-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0f04-161">Remarks</span></span>

<span data-ttu-id="a0f04-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a0f04-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0f04-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a0f04-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0f04-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0f04-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0f04-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a0f04-165">Schema Name</span></span>  <br/> |<span data-ttu-id="a0f04-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a0f04-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0f04-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a0f04-167">Validation File</span></span>  <br/> |<span data-ttu-id="a0f04-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a0f04-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0f04-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a0f04-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="a0f04-170">False</span><span class="sxs-lookup"><span data-stu-id="a0f04-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0f04-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0f04-171">See also</span></span>

- [<span data-ttu-id="a0f04-172">EmptyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0f04-172">EmptyFolder operation</span></span>](emptyfolder-operation.md)
- [<span data-ttu-id="a0f04-173">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="a0f04-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="a0f04-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a0f04-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

