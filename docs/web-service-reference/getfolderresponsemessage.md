---
title: GetFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolderResponseMessage
api_type:
- schema
ms.assetid: 51359863-d110-4c12-b89f-aba5e3e40c1d
description: Das GetFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung GetFolder-Vorgang.
ms.openlocfilehash: a6b67907dba311a3ce482ff8f524378fb4be9694
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758682"
---
# <a name="getfolderresponsemessage"></a><span data-ttu-id="414c8-103">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="414c8-103">GetFolderResponseMessage</span></span>

<span data-ttu-id="414c8-104">Das **GetFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [GetFolder-Vorgang](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="414c8-104">The **GetFolderResponseMessage** element contains the status and result of a single [GetFolder operation](getfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="414c8-105">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="414c8-105">GetFolderResponse</span></span>](getfolderresponse.md) 
- [<span data-ttu-id="414c8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="414c8-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="414c8-107">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="414c8-107">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)
  
```xml
<GetFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</GetFolderResponseMessage>
```

 <span data-ttu-id="414c8-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="414c8-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="414c8-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="414c8-109">Attributes and elements</span></span>

<span data-ttu-id="414c8-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="414c8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="414c8-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="414c8-111">Attributes</span></span>

|<span data-ttu-id="414c8-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="414c8-112">**Attribute**</span></span>|<span data-ttu-id="414c8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414c8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="414c8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="414c8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="414c8-115">Beschreibt den Status einer Antwort [GetFolder-Vorgang](getfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="414c8-115">Describes the status of a [GetFolder operation](getfolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="414c8-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="414c8-116">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="414c8-117">-Success</span><span class="sxs-lookup"><span data-stu-id="414c8-117">-  Success</span></span>  <br/><span data-ttu-id="414c8-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="414c8-118">-  Warning</span></span>  <br/><span data-ttu-id="414c8-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="414c8-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="414c8-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="414c8-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="414c8-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="414c8-121">**Value**</span></span>|<span data-ttu-id="414c8-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414c8-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="414c8-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="414c8-123">**Success**</span></span> <br/> |<span data-ttu-id="414c8-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="414c8-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="414c8-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="414c8-125">**Warning**</span></span> <br/> | <span data-ttu-id="414c8-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="414c8-126">Describes a request that was not processed.</span></span> <span data-ttu-id="414c8-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="414c8-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="414c8-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="414c8-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="414c8-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="414c8-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="414c8-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="414c8-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="414c8-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="414c8-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="414c8-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="414c8-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="414c8-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="414c8-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="414c8-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="414c8-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="414c8-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="414c8-135">**Error**</span></span> <br/> | <span data-ttu-id="414c8-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="414c8-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="414c8-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="414c8-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="414c8-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="414c8-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="414c8-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="414c8-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="414c8-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="414c8-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="414c8-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="414c8-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="414c8-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="414c8-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="414c8-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="414c8-143">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="414c8-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="414c8-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="414c8-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="414c8-145">Child elements</span></span>

|<span data-ttu-id="414c8-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="414c8-146">**Element**</span></span>|<span data-ttu-id="414c8-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414c8-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414c8-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="414c8-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="414c8-149">Beschreibung des Status der Antwort enthält.</span><span class="sxs-lookup"><span data-stu-id="414c8-149">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="414c8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="414c8-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="414c8-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="414c8-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="414c8-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="414c8-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="414c8-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="414c8-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="414c8-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="414c8-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="414c8-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="414c8-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="414c8-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="414c8-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="414c8-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="414c8-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="414c8-158">Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="414c8-158">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="414c8-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="414c8-159">Parent elements</span></span>

|<span data-ttu-id="414c8-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="414c8-160">**Element**</span></span>|<span data-ttu-id="414c8-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="414c8-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="414c8-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="414c8-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="414c8-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="414c8-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="414c8-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="414c8-164">Remarks</span></span>

<span data-ttu-id="414c8-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="414c8-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="414c8-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="414c8-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="414c8-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="414c8-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="414c8-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="414c8-168">Schema Name</span></span>  <br/> |<span data-ttu-id="414c8-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="414c8-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="414c8-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="414c8-170">Validation File</span></span>  <br/> |<span data-ttu-id="414c8-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="414c8-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="414c8-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="414c8-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="414c8-173">False</span><span class="sxs-lookup"><span data-stu-id="414c8-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="414c8-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="414c8-174">See also</span></span>

- [<span data-ttu-id="414c8-175">GetFolder</span><span class="sxs-lookup"><span data-stu-id="414c8-175">GetFolder</span></span>](getfolder.md)
- [<span data-ttu-id="414c8-176">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="414c8-176">GetFolderResponse</span></span>](getfolderresponse.md) 
- [<span data-ttu-id="414c8-177">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="414c8-177">GetFolder operation</span></span>](getfolder-operation.md)

