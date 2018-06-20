---
title: FindFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolderResponseMessage
api_type:
- schema
ms.assetid: 538d64fe-51ae-41d2-bfab-91698678aa1b
description: Das FindFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung FindFolder Vorgang.
ms.openlocfilehash: 5623e5e538e617e5bd4bbc4444328ac83d7b8065
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758451"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="68e77-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="68e77-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="68e77-104">Das **FindFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [FindFolder Vorgang](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="68e77-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="68e77-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="68e77-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="68e77-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="68e77-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="68e77-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="68e77-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="68e77-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="68e77-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68e77-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68e77-109">Attributes and elements</span></span>

<span data-ttu-id="68e77-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68e77-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68e77-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="68e77-111">Attributes</span></span>

|<span data-ttu-id="68e77-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68e77-112">**Attribute**</span></span>|<span data-ttu-id="68e77-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68e77-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68e77-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="68e77-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="68e77-115">Beschreibt den Status einer Antwort [FindFolder Vorgang](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="68e77-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="68e77-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="68e77-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="68e77-117">-Success</span><span class="sxs-lookup"><span data-stu-id="68e77-117">-  Success</span></span>  <br/><span data-ttu-id="68e77-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="68e77-118">-  Warning</span></span>  <br/><span data-ttu-id="68e77-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="68e77-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="68e77-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="68e77-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="68e77-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="68e77-121">**Value**</span></span>|<span data-ttu-id="68e77-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68e77-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68e77-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="68e77-123">**Success**</span></span> <br/> |<span data-ttu-id="68e77-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="68e77-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="68e77-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="68e77-125">**Warning**</span></span> <br/> | <span data-ttu-id="68e77-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="68e77-126">Describes a request that was not processed.</span></span> <span data-ttu-id="68e77-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="68e77-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="68e77-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="68e77-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="68e77-129">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="68e77-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="68e77-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="68e77-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="68e77-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="68e77-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="68e77-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="68e77-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="68e77-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="68e77-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="68e77-134">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="68e77-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="68e77-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="68e77-135">**Error**</span></span> <br/> | <span data-ttu-id="68e77-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="68e77-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="68e77-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="68e77-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="68e77-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="68e77-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="68e77-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="68e77-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="68e77-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="68e77-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="68e77-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="68e77-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="68e77-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="68e77-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="68e77-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="68e77-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="68e77-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="68e77-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68e77-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68e77-145">Child elements</span></span>

|<span data-ttu-id="68e77-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="68e77-146">**Element**</span></span>|<span data-ttu-id="68e77-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68e77-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68e77-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="68e77-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="68e77-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="68e77-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="68e77-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="68e77-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="68e77-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="68e77-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="68e77-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="68e77-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="68e77-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="68e77-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="68e77-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="68e77-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="68e77-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="68e77-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="68e77-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="68e77-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="68e77-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="68e77-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="68e77-158">Enthält die Ergebnisse einer Suche in einer einzelnen Stammordner während einer [FindFolder Vorgang](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="68e77-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="68e77-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68e77-159">Parent elements</span></span>

|<span data-ttu-id="68e77-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="68e77-160">**Element**</span></span>|<span data-ttu-id="68e77-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68e77-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68e77-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="68e77-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="68e77-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="68e77-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68e77-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68e77-164">Remarks</span></span>

<span data-ttu-id="68e77-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="68e77-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68e77-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68e77-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68e77-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="68e77-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="68e77-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68e77-168">Schema name</span></span>  <br/> |<span data-ttu-id="68e77-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="68e77-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="68e77-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68e77-170">Validation file</span></span>  <br/> |<span data-ttu-id="68e77-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="68e77-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="68e77-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="68e77-172">Can be empty</span></span>  <br/> |<span data-ttu-id="68e77-173">False</span><span class="sxs-lookup"><span data-stu-id="68e77-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68e77-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68e77-174">See also</span></span>

- [<span data-ttu-id="68e77-175">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="68e77-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="68e77-176">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="68e77-176">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

