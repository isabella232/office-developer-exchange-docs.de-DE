---
title: DeleteFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponseMessage
api_type:
- schema
ms.assetid: de4c63ff-80b2-40c2-bc06-ef0c23beacd4
description: Das DeleteFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung DeleteFolder-Vorgang.
ms.openlocfilehash: 5601fe2e48ad002e0fab60d812e7d70c7398f3ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757922"
---
# <a name="deletefolderresponsemessage"></a><span data-ttu-id="1a4d9-103">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1a4d9-103">DeleteFolderResponseMessage</span></span>

<span data-ttu-id="1a4d9-104">Das **DeleteFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [DeleteFolder-Vorgang](deletefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4d9-104">The **DeleteFolderResponseMessage** element contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="1a4d9-105">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="1a4d9-105">DeleteFolderResponse</span></span>](deletefolderresponse.md)  
- [<span data-ttu-id="1a4d9-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a4d9-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="1a4d9-107">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1a4d9-107">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 <span data-ttu-id="1a4d9-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a4d9-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1a4d9-109">Attributes and elements</span></span>

<span data-ttu-id="1a4d9-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a4d9-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="1a4d9-111">Attributes</span></span>

|<span data-ttu-id="1a4d9-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-112">**Attribute**</span></span>|<span data-ttu-id="1a4d9-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a4d9-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1a4d9-115">Beschreibt den Status einer Antwort [DeleteFolder-Vorgang](deletefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4d9-115">Describes the status of a [DeleteFolder operation](deletefolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="1a4d9-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1a4d9-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="1a4d9-117">-Success</span><span class="sxs-lookup"><span data-stu-id="1a4d9-117">-  Success</span></span>  <br/><span data-ttu-id="1a4d9-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1a4d9-118">-  Warning</span></span>  <br/><span data-ttu-id="1a4d9-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="1a4d9-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1a4d9-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1a4d9-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="1a4d9-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-121">**Value**</span></span>|<span data-ttu-id="1a4d9-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a4d9-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-123">**Success**</span></span> <br/> |<span data-ttu-id="1a4d9-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1a4d9-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-125">**Warning**</span></span> <br/> | <span data-ttu-id="1a4d9-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-126">Describes a request that was not processed.</span></span> <span data-ttu-id="1a4d9-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="1a4d9-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="1a4d9-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="1a4d9-129">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-129">- The Exchange store goes offline during the batch.</span></span><br/><span data-ttu-id="1a4d9-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-130">- Active Directory Domain Services (AD DS) goes offline.</span></span><br/><span data-ttu-id="1a4d9-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="1a4d9-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-132">- The message database (MDB) goes offline.</span></span><br/><span data-ttu-id="1a4d9-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-133">- A password is expired.</span></span><br/><span data-ttu-id="1a4d9-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-134">- A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="1a4d9-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-135">**Error**</span></span> <br/> | <span data-ttu-id="1a4d9-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="1a4d9-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="1a4d9-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="1a4d9-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1a4d9-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="1a4d9-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="1a4d9-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="1a4d9-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="1a4d9-140">- Unknown tag</span></span><br/><span data-ttu-id="1a4d9-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="1a4d9-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="1a4d9-142">- Unauthorized access attempt by any client</span></span><br/><span data-ttu-id="1a4d9-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1a4d9-143">- Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1a4d9-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1a4d9-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a4d9-145">Child elements</span></span>

|<span data-ttu-id="1a4d9-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-146">**Element**</span></span>|<span data-ttu-id="1a4d9-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a4d9-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="1a4d9-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1a4d9-149">Beschreibender Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1a4d9-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1a4d9-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1a4d9-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1a4d9-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1a4d9-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1a4d9-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1a4d9-154">Es enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1a4d9-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1a4d9-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1a4d9-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a4d9-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a4d9-157">Parent elements</span></span>

|<span data-ttu-id="1a4d9-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-158">**Element**</span></span>|<span data-ttu-id="1a4d9-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a4d9-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a4d9-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1a4d9-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="1a4d9-161">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a4d9-162">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a4d9-162">Remarks</span></span>

<span data-ttu-id="1a4d9-163">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1a4d9-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a4d9-164">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1a4d9-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a4d9-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a4d9-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a4d9-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1a4d9-166">Schema Name</span></span>  <br/> |<span data-ttu-id="1a4d9-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1a4d9-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1a4d9-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1a4d9-168">Validation File</span></span>  <br/> |<span data-ttu-id="1a4d9-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1a4d9-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a4d9-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1a4d9-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a4d9-171">False</span><span class="sxs-lookup"><span data-stu-id="1a4d9-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a4d9-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a4d9-172">See also</span></span>

- [<span data-ttu-id="1a4d9-173">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1a4d9-173">DeleteFolder operation</span></span>](deletefolder-operation.md)
- [<span data-ttu-id="1a4d9-174">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="1a4d9-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="1a4d9-175">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1a4d9-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="1a4d9-176">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="1a4d9-176">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

