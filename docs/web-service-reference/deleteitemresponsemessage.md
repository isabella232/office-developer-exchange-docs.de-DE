---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: Das DeleteItemResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung DeleteItem Vorgang.
ms.openlocfilehash: 1f0cc3d49bfa5fba6da32cf65df6b6718ccfbded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757939"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="97641-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="97641-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="97641-104">Das **DeleteItemResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [DeleteItem Vorgang](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="97641-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="97641-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="97641-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="97641-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="97641-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="97641-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="97641-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="97641-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="97641-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97641-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="97641-109">Attributes and elements</span></span>

<span data-ttu-id="97641-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="97641-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97641-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="97641-111">Attributes</span></span>

|<span data-ttu-id="97641-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="97641-112">**Attribute**</span></span>|<span data-ttu-id="97641-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97641-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97641-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="97641-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="97641-115">Beschreibt den Status einer Antwort [DeleteItem Vorgang](deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="97641-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="97641-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="97641-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="97641-117">-Success</span><span class="sxs-lookup"><span data-stu-id="97641-117">- Success</span></span>  <br/><span data-ttu-id="97641-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="97641-118">-  Warning</span></span>  <br/><span data-ttu-id="97641-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="97641-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="97641-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="97641-120">ResponseClass attribute</span></span>

|<span data-ttu-id="97641-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="97641-121">**Value**</span></span>|<span data-ttu-id="97641-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97641-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97641-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="97641-123">**Success**</span></span> <br/> |<span data-ttu-id="97641-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="97641-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="97641-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="97641-125">**Warning**</span></span> <br/> | <span data-ttu-id="97641-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="97641-126">Describes a request that was not processed.</span></span> <span data-ttu-id="97641-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="97641-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="97641-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="97641-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="97641-129">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="97641-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="97641-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="97641-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="97641-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="97641-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="97641-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="97641-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="97641-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="97641-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="97641-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="97641-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="97641-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="97641-135">**Error**</span></span> <br/> | <span data-ttu-id="97641-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="97641-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="97641-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="97641-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="97641-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="97641-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="97641-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="97641-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="97641-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="97641-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="97641-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="97641-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="97641-142">-Ein Client versuchen, den Protokolliergrad Fehler oberhalb der maximalen Ebene festlegen, der vom Administrator zulässig ist</span><span class="sxs-lookup"><span data-stu-id="97641-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="97641-143">-Ein Client versuchen, den Fehler Schweregrad unterhalb der Standardebene festlegen, der vom Administrator angegeben wird</span><span class="sxs-lookup"><span data-stu-id="97641-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="97641-144">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="97641-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="97641-145">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="97641-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="97641-146">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="97641-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97641-147">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97641-147">Child elements</span></span>

|<span data-ttu-id="97641-148">**Element**</span><span class="sxs-lookup"><span data-stu-id="97641-148">**Element**</span></span>|<span data-ttu-id="97641-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97641-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97641-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="97641-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="97641-151">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="97641-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="97641-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="97641-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="97641-153">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="97641-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="97641-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="97641-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="97641-155">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="97641-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="97641-156">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="97641-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="97641-157">MessageXml</span><span class="sxs-lookup"><span data-stu-id="97641-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="97641-158">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="97641-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="97641-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97641-159">Parent elements</span></span>

|<span data-ttu-id="97641-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="97641-160">**Element**</span></span>|<span data-ttu-id="97641-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97641-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97641-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="97641-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="97641-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="97641-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97641-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97641-164">Remarks</span></span>

<span data-ttu-id="97641-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="97641-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="97641-166">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="97641-166">Version differences</span></span>

<span data-ttu-id="97641-167">In Versionen von Exchange, beginnend mit Build 15.00.0986.00 ist das **DeleteItemResponseMessage** -Element vom Typ **DeleteItemResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="97641-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="97641-168">In früheren Versionen ist das Element vom Typ **ResponseMessageType**.</span><span class="sxs-lookup"><span data-stu-id="97641-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97641-169">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="97641-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97641-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="97641-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="97641-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="97641-171">Schema Name</span></span>  <br/> |<span data-ttu-id="97641-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="97641-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="97641-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="97641-173">Validation File</span></span>  <br/> |<span data-ttu-id="97641-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="97641-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="97641-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="97641-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="97641-176">False</span><span class="sxs-lookup"><span data-stu-id="97641-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97641-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97641-177">See also</span></span>

- [<span data-ttu-id="97641-178">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="97641-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="97641-179">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="97641-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="97641-180">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="97641-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="97641-181">Löschen von Elementen (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="97641-181">Deleting Items (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

