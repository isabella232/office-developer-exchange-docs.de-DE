---
title: UpdateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolderResponseMessage
api_type:
- schema
ms.assetid: 914bb683-49ee-44a2-b59d-ef560244dfb8
description: Das UpdateFolderResponseMessage-Element enthält den Status und das Ergebnis der Updates vom einer UpdateFolder Vorgang Anforderung FolderChange-Element definiert.
ms.openlocfilehash: 4cd00232bcc233f6534d844418f523c248ce54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839364"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="e39ee-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e39ee-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="e39ee-104">Das **UpdateFolderResponseMessage** -Element enthält den Status und das Ergebnis der Updates vom einer Anforderung [UpdateFolder Vorgang](updatefolder-operation.md) [FolderChange](folderchange.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="e39ee-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="e39ee-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="e39ee-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="e39ee-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e39ee-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="e39ee-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e39ee-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="e39ee-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e39ee-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e39ee-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e39ee-109">Attributes and elements</span></span>

<span data-ttu-id="e39ee-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e39ee-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e39ee-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="e39ee-111">Attributes</span></span>

|<span data-ttu-id="e39ee-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e39ee-112">**Attribute**</span></span>|<span data-ttu-id="e39ee-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e39ee-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e39ee-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e39ee-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e39ee-115">Beschreibt den Status einer Antwort [UpdateFolder Vorgang](updatefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e39ee-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="e39ee-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="e39ee-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="e39ee-117">-Success</span><span class="sxs-lookup"><span data-stu-id="e39ee-117">-  Success</span></span>  <br/><span data-ttu-id="e39ee-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="e39ee-118">-  Warning</span></span>  <br/><span data-ttu-id="e39ee-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="e39ee-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e39ee-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e39ee-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="e39ee-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e39ee-121">**Value**</span></span>|<span data-ttu-id="e39ee-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e39ee-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e39ee-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="e39ee-123">**Success**</span></span> <br/> |<span data-ttu-id="e39ee-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="e39ee-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e39ee-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="e39ee-125">**Warning**</span></span> <br/> | <span data-ttu-id="e39ee-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e39ee-126">Describes a request that was not processed.</span></span> <span data-ttu-id="e39ee-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e39ee-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="e39ee-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="e39ee-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="e39ee-129">-Offline ist Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e39ee-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="e39ee-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e39ee-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e39ee-131">-Ein Postfach verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e39ee-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="e39ee-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="e39ee-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="e39ee-133">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="e39ee-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="e39ee-134">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="e39ee-134">**Error**</span></span> <br/> | <span data-ttu-id="e39ee-135">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e39ee-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="e39ee-136">Es folgen Beispiele für Datenquellen für Fehler:</span><span class="sxs-lookup"><span data-stu-id="e39ee-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="e39ee-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="e39ee-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e39ee-138">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="e39ee-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="e39ee-139">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="e39ee-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="e39ee-140">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e39ee-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="e39ee-141">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="e39ee-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e39ee-142">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="e39ee-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="e39ee-143">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e39ee-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e39ee-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e39ee-144">Child elements</span></span>

|<span data-ttu-id="e39ee-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="e39ee-145">**Element**</span></span>|<span data-ttu-id="e39ee-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e39ee-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e39ee-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="e39ee-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e39ee-148">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e39ee-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e39ee-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e39ee-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e39ee-150">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="e39ee-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e39ee-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e39ee-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e39ee-152">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e39ee-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="e39ee-153">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="e39ee-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e39ee-154">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e39ee-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e39ee-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="e39ee-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="e39ee-156">Ordner</span><span class="sxs-lookup"><span data-stu-id="e39ee-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e39ee-157">Enthält ein Array von Ordnern im Ordner Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="e39ee-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e39ee-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e39ee-158">Parent elements</span></span>

|<span data-ttu-id="e39ee-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="e39ee-159">**Element**</span></span>|<span data-ttu-id="e39ee-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e39ee-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e39ee-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e39ee-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e39ee-162">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e39ee-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e39ee-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e39ee-163">Remarks</span></span>

<span data-ttu-id="e39ee-164">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e39ee-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e39ee-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e39ee-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e39ee-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="e39ee-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e39ee-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e39ee-167">Schema Name</span></span>  <br/> |<span data-ttu-id="e39ee-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e39ee-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e39ee-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e39ee-169">Validation File</span></span>  <br/> |<span data-ttu-id="e39ee-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e39ee-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e39ee-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e39ee-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="e39ee-172">False</span><span class="sxs-lookup"><span data-stu-id="e39ee-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e39ee-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e39ee-173">See also</span></span>

- [<span data-ttu-id="e39ee-174">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e39ee-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

