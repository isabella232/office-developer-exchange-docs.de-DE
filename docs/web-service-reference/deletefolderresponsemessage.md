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
description: Das DeleteFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen DeleteFolder-Vorgangsanforderung.
ms.openlocfilehash: 6c593e0d6e8820452bb27a6baa569980e329ef10
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455737"
---
# <a name="deletefolderresponsemessage"></a><span data-ttu-id="2789d-103">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2789d-103">DeleteFolderResponseMessage</span></span>

<span data-ttu-id="2789d-104">Das **DeleteFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [DeleteFolder-Vorgangs](deletefolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2789d-104">The **DeleteFolderResponseMessage** element contains the status and result of a single [DeleteFolder operation](deletefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2789d-105">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="2789d-105">DeleteFolderResponse</span></span>](deletefolderresponse.md)  
- [<span data-ttu-id="2789d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2789d-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="2789d-107">DeleteFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2789d-107">DeleteFolderResponseMessage</span></span>](deletefolderresponsemessage.md)
  
```xml
<DeleteFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteFolderResponseMessage>
```

 <span data-ttu-id="2789d-108">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2789d-108">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2789d-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2789d-109">Attributes and elements</span></span>

<span data-ttu-id="2789d-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2789d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2789d-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2789d-111">Attributes</span></span>

|<span data-ttu-id="2789d-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2789d-112">**Attribute**</span></span>|<span data-ttu-id="2789d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2789d-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2789d-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2789d-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2789d-115">Beschreibt den Status einer [DeleteFolder-Vorgangs](deletefolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="2789d-115">Describes the status of a [DeleteFolder operation](deletefolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="2789d-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="2789d-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="2789d-117">-Success</span><span class="sxs-lookup"><span data-stu-id="2789d-117">-  Success</span></span>  <br/><span data-ttu-id="2789d-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="2789d-118">-  Warning</span></span>  <br/><span data-ttu-id="2789d-119">-Error</span><span class="sxs-lookup"><span data-stu-id="2789d-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="2789d-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="2789d-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="2789d-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2789d-121">**Value**</span></span>|<span data-ttu-id="2789d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2789d-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2789d-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="2789d-123">**Success**</span></span> <br/> |<span data-ttu-id="2789d-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2789d-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="2789d-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2789d-125">**Warning**</span></span> <br/> | <span data-ttu-id="2789d-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2789d-126">Describes a request that was not processed.</span></span> <span data-ttu-id="2789d-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2789d-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="2789d-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="2789d-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="2789d-129">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2789d-129">- The Exchange store goes offline during the batch.</span></span><br/><span data-ttu-id="2789d-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2789d-130">- Active Directory Domain Services (AD DS) goes offline.</span></span><br/><span data-ttu-id="2789d-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="2789d-131">- Mailboxes are moved.</span></span><br/><span data-ttu-id="2789d-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2789d-132">- The message database (MDB) goes offline.</span></span><br/><span data-ttu-id="2789d-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="2789d-133">- A password is expired.</span></span><br/><span data-ttu-id="2789d-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="2789d-134">- A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="2789d-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="2789d-135">**Error**</span></span> <br/> | <span data-ttu-id="2789d-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2789d-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="2789d-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="2789d-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="2789d-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="2789d-138">- Invalid attributes or elements</span></span><br/><span data-ttu-id="2789d-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="2789d-139">- Attributes or elements out of range</span></span><br/><span data-ttu-id="2789d-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="2789d-140">- Unknown tag</span></span><br/><span data-ttu-id="2789d-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="2789d-141">- Attribute or element not valid in the context</span></span><br/><span data-ttu-id="2789d-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="2789d-142">- Unauthorized access attempt by any client</span></span><br/><span data-ttu-id="2789d-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="2789d-143">- Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="2789d-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="2789d-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2789d-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2789d-145">Child elements</span></span>

|<span data-ttu-id="2789d-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="2789d-146">**Element**</span></span>|<span data-ttu-id="2789d-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2789d-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2789d-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="2789d-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2789d-149">Eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2789d-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2789d-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2789d-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2789d-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2789d-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="2789d-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2789d-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2789d-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2789d-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2789d-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="2789d-154">It contains the value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2789d-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="2789d-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2789d-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="2789d-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2789d-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2789d-157">Parent elements</span></span>

|<span data-ttu-id="2789d-158">**Element**</span><span class="sxs-lookup"><span data-stu-id="2789d-158">**Element**</span></span>|<span data-ttu-id="2789d-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2789d-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2789d-160">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2789d-160">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2789d-161">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2789d-161">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2789d-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2789d-162">Remarks</span></span>

<span data-ttu-id="2789d-163">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2789d-163">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2789d-164">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2789d-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2789d-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="2789d-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2789d-166">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2789d-166">Schema Name</span></span>  <br/> |<span data-ttu-id="2789d-167">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2789d-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2789d-168">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2789d-168">Validation File</span></span>  <br/> |<span data-ttu-id="2789d-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2789d-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2789d-170">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2789d-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="2789d-171">False</span><span class="sxs-lookup"><span data-stu-id="2789d-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2789d-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2789d-172">See also</span></span>

- [<span data-ttu-id="2789d-173">DeleteFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2789d-173">DeleteFolder operation</span></span>](deletefolder-operation.md)
- [<span data-ttu-id="2789d-174">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="2789d-174">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="2789d-175">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2789d-175">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2789d-176">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="2789d-176">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

