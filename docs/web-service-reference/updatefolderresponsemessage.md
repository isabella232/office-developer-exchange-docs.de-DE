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
description: Das UpdateFolderResponseMessage-Element enthält den Status und das Ergebnis der durch das FolderChange-Element einer UpdateFolder-Vorgangsanforderung definierten Aktualisierungen.
ms.openlocfilehash: bbe01583072e6203e099d440f2a171012f51e7df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466584"
---
# <a name="updatefolderresponsemessage"></a><span data-ttu-id="faa13-103">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="faa13-103">UpdateFolderResponseMessage</span></span>

<span data-ttu-id="faa13-104">Das **UpdateFolderResponseMessage** -Element enthält den Status und das Ergebnis der durch das [FolderChange](folderchange.md) -Element einer [UpdateFolder-Vorgangs](updatefolder-operation.md) Anforderung definierten Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="faa13-104">The **UpdateFolderResponseMessage** element contains the status and result of updates defined by the [FolderChange](folderchange.md) element of an [UpdateFolder operation](updatefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="faa13-105">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="faa13-105">UpdateFolderResponse</span></span>](updatefolderresponse.md) 
- [<span data-ttu-id="faa13-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="faa13-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="faa13-107">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="faa13-107">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
  
```xml
<UpdateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</UpdateFolderResponseMessage>
```

 <span data-ttu-id="faa13-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="faa13-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="faa13-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="faa13-109">Attributes and elements</span></span>

<span data-ttu-id="faa13-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="faa13-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="faa13-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="faa13-111">Attributes</span></span>

|<span data-ttu-id="faa13-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="faa13-112">**Attribute**</span></span>|<span data-ttu-id="faa13-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="faa13-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="faa13-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="faa13-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="faa13-115">Beschreibt den Status einer [UpdateFolder-Vorgangs](updatefolder-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="faa13-115">Describes the status of an [UpdateFolder operation](updatefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="faa13-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="faa13-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="faa13-117">-Success</span><span class="sxs-lookup"><span data-stu-id="faa13-117">-  Success</span></span>  <br/><span data-ttu-id="faa13-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="faa13-118">-  Warning</span></span>  <br/><span data-ttu-id="faa13-119">-Error</span><span class="sxs-lookup"><span data-stu-id="faa13-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="faa13-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="faa13-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="faa13-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="faa13-121">**Value**</span></span>|<span data-ttu-id="faa13-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="faa13-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="faa13-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="faa13-123">**Success**</span></span> <br/> |<span data-ttu-id="faa13-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="faa13-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="faa13-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="faa13-125">**Warning**</span></span> <br/> | <span data-ttu-id="faa13-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="faa13-126">Describes a request that was not processed.</span></span> <span data-ttu-id="faa13-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="faa13-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="faa13-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="faa13-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="faa13-129">-Die Exchange-Informationsspeicher ist offline.</span><span class="sxs-lookup"><span data-stu-id="faa13-129">-  The Exchange store is offline.</span></span>  <br/><span data-ttu-id="faa13-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="faa13-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="faa13-131">– Ein Postfach wird verschoben.</span><span class="sxs-lookup"><span data-stu-id="faa13-131">-  A mailbox is moved.</span></span>  <br/><span data-ttu-id="faa13-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="faa13-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="faa13-133">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="faa13-133">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="faa13-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="faa13-134">**Error**</span></span> <br/> | <span data-ttu-id="faa13-135">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="faa13-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="faa13-136">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="faa13-136">The following are examples of sources for errors:</span></span>  <br/><br/><span data-ttu-id="faa13-137">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="faa13-137">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="faa13-138">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="faa13-138">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="faa13-139">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="faa13-139">-  Unknown tag</span></span>  <br/><span data-ttu-id="faa13-140">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="faa13-140">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="faa13-141">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="faa13-141">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="faa13-142">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="faa13-142">-  Server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="faa13-143">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="faa13-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="faa13-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="faa13-144">Child elements</span></span>

|<span data-ttu-id="faa13-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="faa13-145">**Element**</span></span>|<span data-ttu-id="faa13-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="faa13-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faa13-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="faa13-147">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="faa13-148">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="faa13-148">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="faa13-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="faa13-149">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="faa13-150">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="faa13-150">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="faa13-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="faa13-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="faa13-152">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="faa13-152">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="faa13-153">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="faa13-153">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="faa13-154">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="faa13-154">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="faa13-155">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="faa13-155">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="faa13-156">Ordner</span><span class="sxs-lookup"><span data-stu-id="faa13-156">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="faa13-157">Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faa13-157">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="faa13-158">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="faa13-158">Parent elements</span></span>

|<span data-ttu-id="faa13-159">**Element**</span><span class="sxs-lookup"><span data-stu-id="faa13-159">**Element**</span></span>|<span data-ttu-id="faa13-160">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="faa13-160">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faa13-161">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="faa13-161">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="faa13-162">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="faa13-162">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faa13-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faa13-163">Remarks</span></span>

<span data-ttu-id="faa13-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="faa13-164">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faa13-165">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="faa13-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faa13-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="faa13-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="faa13-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="faa13-167">Schema Name</span></span>  <br/> |<span data-ttu-id="faa13-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="faa13-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="faa13-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="faa13-169">Validation File</span></span>  <br/> |<span data-ttu-id="faa13-170">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="faa13-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="faa13-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="faa13-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="faa13-172">False</span><span class="sxs-lookup"><span data-stu-id="faa13-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faa13-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa13-173">See also</span></span>

- [<span data-ttu-id="faa13-174">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="faa13-174">UpdateFolder operation</span></span>](updatefolder-operation.md)

