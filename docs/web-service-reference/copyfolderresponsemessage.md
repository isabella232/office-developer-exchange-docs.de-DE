---
title: CopyFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolderResponseMessage
api_type:
- schema
ms.assetid: c82092a9-50ff-4ae1-b819-ebabbf89262b
description: Das CopyFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CopyFolder-Vorgang.
ms.openlocfilehash: 2bb2b407e0ae6b854d214c4b9d68ac8ed65b2c7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757723"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="9b3ad-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9b3ad-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="9b3ad-104">Das **CopyFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CopyFolder-Vorgang](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9b3ad-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="9b3ad-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="9b3ad-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="9b3ad-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b3ad-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="9b3ad-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9b3ad-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="9b3ad-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b3ad-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3ad-109">Attributes and elements</span></span>

<span data-ttu-id="9b3ad-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b3ad-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b3ad-111">Attributes</span></span>

|<span data-ttu-id="9b3ad-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-112">**Attribute**</span></span>|<span data-ttu-id="9b3ad-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3ad-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9b3ad-115">Beschreibt den Status einer Antwort [CopyFolder-Vorgang](copyfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9b3ad-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="9b3ad-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="9b3ad-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="9b3ad-117">-Success</span><span class="sxs-lookup"><span data-stu-id="9b3ad-117">- Success</span></span>  <br/><span data-ttu-id="9b3ad-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="9b3ad-118">-  Warning</span></span>  <br/><span data-ttu-id="9b3ad-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="9b3ad-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9b3ad-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9b3ad-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="9b3ad-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-121">**Value**</span></span>|<span data-ttu-id="9b3ad-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3ad-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-123">**Success**</span></span> <br/> |<span data-ttu-id="9b3ad-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9b3ad-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-125">**Warning**</span></span> <br/> | <span data-ttu-id="9b3ad-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-126">Describes a request that was not processed.</span></span> <span data-ttu-id="9b3ad-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="9b3ad-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="9b3ad-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="9b3ad-129">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="9b3ad-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="9b3ad-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="9b3ad-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="9b3ad-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="9b3ad-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="9b3ad-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-135">**Error**</span></span> <br/> | <span data-ttu-id="9b3ad-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="9b3ad-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="9b3ad-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9b3ad-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3ad-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9b3ad-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="9b3ad-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9b3ad-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="9b3ad-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="9b3ad-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="9b3ad-142">-Nicht autorisierten Zugriff von jedem Client versucht</span><span class="sxs-lookup"><span data-stu-id="9b3ad-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="9b3ad-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="9b3ad-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="9b3ad-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b3ad-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3ad-145">Child elements</span></span>

|<span data-ttu-id="9b3ad-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-146">**Element**</span></span>|<span data-ttu-id="9b3ad-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b3ad-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="9b3ad-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9b3ad-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9b3ad-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9b3ad-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9b3ad-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9b3ad-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9b3ad-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9b3ad-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9b3ad-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9b3ad-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9b3ad-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9b3ad-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9b3ad-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="9b3ad-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9b3ad-158">Enthält ein Array der kopierten Ordner.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b3ad-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3ad-159">Parent elements</span></span>

|<span data-ttu-id="9b3ad-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-160">**Element**</span></span>|<span data-ttu-id="9b3ad-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3ad-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b3ad-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9b3ad-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9b3ad-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b3ad-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b3ad-164">Remarks</span></span>

<span data-ttu-id="9b3ad-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9b3ad-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b3ad-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9b3ad-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b3ad-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b3ad-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b3ad-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b3ad-168">Schema name</span></span>  <br/> |<span data-ttu-id="9b3ad-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9b3ad-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b3ad-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b3ad-170">Validation file</span></span>  <br/> |<span data-ttu-id="9b3ad-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b3ad-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b3ad-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9b3ad-172">Can be empty</span></span>  <br/> |<span data-ttu-id="9b3ad-173">False</span><span class="sxs-lookup"><span data-stu-id="9b3ad-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b3ad-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b3ad-174">See also</span></span>

- [<span data-ttu-id="9b3ad-175">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b3ad-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="9b3ad-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="9b3ad-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="9b3ad-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9b3ad-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

