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
description: Das CopyFolderResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CopyFolder-Vorgangsanforderung.
ms.openlocfilehash: 796ec57116e4b4943ca370e45cf0abefe7782c08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458509"
---
# <a name="copyfolderresponsemessage"></a><span data-ttu-id="81d88-103">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="81d88-103">CopyFolderResponseMessage</span></span>

<span data-ttu-id="81d88-104">Das **CopyFolderResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CopyFolder-Vorgangs](copyfolder-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="81d88-104">The **CopyFolderResponseMessage** element contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="81d88-105">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="81d88-105">CopyFolderResponse</span></span>](copyfolderresponse.md) 
- [<span data-ttu-id="81d88-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="81d88-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="81d88-107">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="81d88-107">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md)
  
```xml
<CopyFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CopyFolderResponseMessage>
```

 <span data-ttu-id="81d88-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="81d88-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81d88-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81d88-109">Attributes and elements</span></span>

<span data-ttu-id="81d88-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81d88-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81d88-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="81d88-111">Attributes</span></span>

|<span data-ttu-id="81d88-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="81d88-112">**Attribute**</span></span>|<span data-ttu-id="81d88-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81d88-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81d88-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="81d88-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="81d88-115">Beschreibt den Status einer [CopyFolder-Vorgangs](copyfolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="81d88-115">Describes the status of a [CopyFolder operation](copyfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="81d88-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="81d88-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="81d88-117">-Success</span><span class="sxs-lookup"><span data-stu-id="81d88-117">- Success</span></span>  <br/><span data-ttu-id="81d88-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="81d88-118">-  Warning</span></span>  <br/><span data-ttu-id="81d88-119">-Error</span><span class="sxs-lookup"><span data-stu-id="81d88-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="81d88-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="81d88-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="81d88-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="81d88-121">**Value**</span></span>|<span data-ttu-id="81d88-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81d88-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81d88-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="81d88-123">**Success**</span></span> <br/> |<span data-ttu-id="81d88-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="81d88-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="81d88-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="81d88-125">**Warning**</span></span> <br/> | <span data-ttu-id="81d88-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="81d88-126">Describes a request that was not processed.</span></span> <span data-ttu-id="81d88-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="81d88-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="81d88-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="81d88-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="81d88-129">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="81d88-129">- The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="81d88-130">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="81d88-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="81d88-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="81d88-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="81d88-132">-Die Nachrichtendatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="81d88-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="81d88-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="81d88-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="81d88-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="81d88-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="81d88-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="81d88-135">**Error**</span></span> <br/> | <span data-ttu-id="81d88-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="81d88-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="81d88-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="81d88-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="81d88-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="81d88-138">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="81d88-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="81d88-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="81d88-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="81d88-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="81d88-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="81d88-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="81d88-142">-Nicht autorisierter Zugriff durch einen Client versucht</span><span class="sxs-lookup"><span data-stu-id="81d88-142">-  Unauthorized access attempted by any client</span></span>  <br/><span data-ttu-id="81d88-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="81d88-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="81d88-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="81d88-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81d88-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81d88-145">Child elements</span></span>

|<span data-ttu-id="81d88-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="81d88-146">**Element**</span></span>|<span data-ttu-id="81d88-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81d88-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81d88-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="81d88-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="81d88-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="81d88-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="81d88-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="81d88-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="81d88-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="81d88-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="81d88-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="81d88-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="81d88-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="81d88-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="81d88-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="81d88-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="81d88-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="81d88-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="81d88-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="81d88-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="81d88-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="81d88-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="81d88-158">Enthält ein Array kopierter Ordner.</span><span class="sxs-lookup"><span data-stu-id="81d88-158">Contains an array of copied folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81d88-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81d88-159">Parent elements</span></span>

|<span data-ttu-id="81d88-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="81d88-160">**Element**</span></span>|<span data-ttu-id="81d88-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81d88-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81d88-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="81d88-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="81d88-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="81d88-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81d88-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81d88-164">Remarks</span></span>

<span data-ttu-id="81d88-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="81d88-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81d88-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="81d88-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81d88-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="81d88-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="81d88-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81d88-168">Schema name</span></span>  <br/> |<span data-ttu-id="81d88-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="81d88-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="81d88-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81d88-170">Validation file</span></span>  <br/> |<span data-ttu-id="81d88-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="81d88-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="81d88-172">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="81d88-172">Can be empty</span></span>  <br/> |<span data-ttu-id="81d88-173">False</span><span class="sxs-lookup"><span data-stu-id="81d88-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81d88-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81d88-174">See also</span></span>

- [<span data-ttu-id="81d88-175">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81d88-175">CopyFolder operation</span></span>](copyfolder-operation.md)
- [<span data-ttu-id="81d88-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="81d88-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="81d88-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="81d88-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

