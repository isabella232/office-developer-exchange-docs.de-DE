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
description: Das FindFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen FindFolder-Vorgangsanforderung.
ms.openlocfilehash: 318a09e371043252d43a5197211e9623f34229fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462563"
---
# <a name="findfolderresponsemessage"></a><span data-ttu-id="92d83-103">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="92d83-103">FindFolderResponseMessage</span></span>

<span data-ttu-id="92d83-104">Das **FindFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [FindFolder-Vorgangs](findfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="92d83-104">The **FindFolderResponseMessage** element contains the status and result of a single [FindFolder operation](findfolder-operation.md) request.</span></span> 
  
[<span data-ttu-id="92d83-105">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="92d83-105">FindFolderResponse</span></span>](findfolderresponse.md)
  
[<span data-ttu-id="92d83-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="92d83-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="92d83-107">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="92d83-107">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
  
```xml
<FindFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RootFolder/>
</FindFolderResponseMessage>
```

 <span data-ttu-id="92d83-108">**FindFolderResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="92d83-108">**FindFolderResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92d83-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="92d83-109">Attributes and elements</span></span>

<span data-ttu-id="92d83-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="92d83-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92d83-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="92d83-111">Attributes</span></span>

|<span data-ttu-id="92d83-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92d83-112">**Attribute**</span></span>|<span data-ttu-id="92d83-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92d83-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92d83-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="92d83-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="92d83-115">Beschreibt den Status einer [FindFolder-Vorgangs](findfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="92d83-115">Describes the status of a [FindFolder operation](findfolder-operation.md) response.</span></span><br/><br/> <span data-ttu-id="92d83-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="92d83-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="92d83-117">-Success</span><span class="sxs-lookup"><span data-stu-id="92d83-117">-  Success</span></span>  <br/><span data-ttu-id="92d83-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="92d83-118">-  Warning</span></span>  <br/><span data-ttu-id="92d83-119">-Error</span><span class="sxs-lookup"><span data-stu-id="92d83-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="92d83-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="92d83-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="92d83-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="92d83-121">**Value**</span></span>|<span data-ttu-id="92d83-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92d83-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92d83-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="92d83-123">**Success**</span></span> <br/> |<span data-ttu-id="92d83-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="92d83-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="92d83-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="92d83-125">**Warning**</span></span> <br/> | <span data-ttu-id="92d83-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="92d83-126">Describes a request that was not processed.</span></span> <span data-ttu-id="92d83-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="92d83-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="92d83-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="92d83-128">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="92d83-129">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="92d83-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="92d83-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="92d83-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="92d83-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="92d83-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="92d83-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="92d83-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="92d83-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="92d83-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="92d83-134">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="92d83-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="92d83-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="92d83-135">**Error**</span></span> <br/> | <span data-ttu-id="92d83-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="92d83-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="92d83-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="92d83-137">The following are examples of sources of errors:</span></span>  <br/><span data-ttu-id="92d83-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="92d83-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="92d83-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="92d83-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="92d83-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="92d83-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="92d83-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="92d83-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="92d83-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="92d83-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="92d83-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="92d83-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="92d83-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="92d83-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92d83-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92d83-145">Child elements</span></span>

|<span data-ttu-id="92d83-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="92d83-146">**Element**</span></span>|<span data-ttu-id="92d83-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92d83-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92d83-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="92d83-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="92d83-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="92d83-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="92d83-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="92d83-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="92d83-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="92d83-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="92d83-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="92d83-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="92d83-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="92d83-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="92d83-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="92d83-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="92d83-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="92d83-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="92d83-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="92d83-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="92d83-157">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="92d83-157">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="92d83-158">Enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindFolder- [Vorgangs](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="92d83-158">Contains the results from a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92d83-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92d83-159">Parent elements</span></span>

|<span data-ttu-id="92d83-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="92d83-160">**Element**</span></span>|<span data-ttu-id="92d83-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92d83-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92d83-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="92d83-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="92d83-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="92d83-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92d83-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92d83-164">Remarks</span></span>

<span data-ttu-id="92d83-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="92d83-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92d83-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="92d83-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92d83-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="92d83-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="92d83-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="92d83-168">Schema name</span></span>  <br/> |<span data-ttu-id="92d83-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="92d83-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="92d83-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="92d83-170">Validation file</span></span>  <br/> |<span data-ttu-id="92d83-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="92d83-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="92d83-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="92d83-172">Can be empty</span></span>  <br/> |<span data-ttu-id="92d83-173">False</span><span class="sxs-lookup"><span data-stu-id="92d83-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92d83-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92d83-174">See also</span></span>

- [<span data-ttu-id="92d83-175">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="92d83-175">FindFolder operation</span></span>](findfolder-operation.md)
- [<span data-ttu-id="92d83-176">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="92d83-176">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

