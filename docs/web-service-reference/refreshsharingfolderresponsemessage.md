---
title: RefreshSharingFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolderResponseMessage
api_type:
- schema
ms.assetid: 53ee65bd-cf75-4e04-9b27-eff1b040ae82
description: Das RefreshSharingFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung RefreshSharingFolder Vorgang.
ms.openlocfilehash: 9dbb66c294439f33a9307d51c03dd1cd127e95e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831052"
---
# <a name="refreshsharingfolderresponsemessage"></a><span data-ttu-id="1555a-103">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1555a-103">RefreshSharingFolderResponseMessage</span></span>

<span data-ttu-id="1555a-104">Das **RefreshSharingFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [RefreshSharingFolder Vorgang](refreshsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1555a-104">The **RefreshSharingFolderResponseMessage** element contains the status and result of a single [RefreshSharingFolder operation](refreshsharingfolder-operation.md) request.</span></span> 
  
```xml
<RefreshSharingFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RefreshSharingFolderResponseMessage>
```

 <span data-ttu-id="1555a-105">**RefreshSharingFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1555a-105">**RefreshSharingFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1555a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1555a-106">Attributes and elements</span></span>

<span data-ttu-id="1555a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1555a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1555a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1555a-108">Attributes</span></span>

|<span data-ttu-id="1555a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1555a-109">**Attribute**</span></span>|<span data-ttu-id="1555a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1555a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1555a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1555a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1555a-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1555a-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="1555a-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1555a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1555a-114">-Success</span><span class="sxs-lookup"><span data-stu-id="1555a-114">-  Success</span></span>  <br/><span data-ttu-id="1555a-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1555a-115">-  Warning</span></span>  <br/><span data-ttu-id="1555a-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="1555a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1555a-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1555a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1555a-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1555a-118">**Value**</span></span>|<span data-ttu-id="1555a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1555a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1555a-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="1555a-120">**Success**</span></span> <br/> |<span data-ttu-id="1555a-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1555a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1555a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1555a-122">**Warning**</span></span> <br/> | <span data-ttu-id="1555a-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1555a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1555a-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1555a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1555a-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="1555a-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="1555a-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="1555a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1555a-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="1555a-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="1555a-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="1555a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1555a-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1555a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1555a-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1555a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1555a-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1555a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1555a-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="1555a-132">**Error**</span></span> <br/> | <span data-ttu-id="1555a-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1555a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1555a-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="1555a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1555a-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1555a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1555a-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="1555a-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1555a-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="1555a-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="1555a-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1555a-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1555a-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="1555a-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1555a-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1555a-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1555a-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1555a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1555a-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1555a-142">Child elements</span></span>

|<span data-ttu-id="1555a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1555a-143">**Element**</span></span>|<span data-ttu-id="1555a-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1555a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1555a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1555a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1555a-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1555a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1555a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1555a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1555a-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="1555a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1555a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1555a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1555a-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1555a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1555a-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1555a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1555a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1555a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1555a-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1555a-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1555a-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1555a-154">Parent elements</span></span>

|<span data-ttu-id="1555a-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="1555a-155">**Element**</span></span>|<span data-ttu-id="1555a-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1555a-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1555a-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1555a-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1555a-158">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1555a-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1555a-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1555a-159">Remarks</span></span>

<span data-ttu-id="1555a-160">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1555a-160">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1555a-161">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1555a-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1555a-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="1555a-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1555a-163">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1555a-163">Schema Name</span></span>  <br/> |<span data-ttu-id="1555a-164">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1555a-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1555a-165">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1555a-165">Validation File</span></span>  <br/> |<span data-ttu-id="1555a-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1555a-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1555a-167">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1555a-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="1555a-168">False</span><span class="sxs-lookup"><span data-stu-id="1555a-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1555a-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1555a-169">See also</span></span>

- [<span data-ttu-id="1555a-170">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1555a-170">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md)
- [<span data-ttu-id="1555a-171">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1555a-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

