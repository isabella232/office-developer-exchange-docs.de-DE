---
title: CreateManagedFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolderResponseMessage
api_type:
- schema
ms.assetid: a72eefc3-ef0b-4b44-a74b-e6907b5b5f68
description: Das CreateManagedFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CreateManagedFolder Vorgang.
ms.openlocfilehash: e561cac949ebebc647b16578c6acbcd6132eeef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757798"
---
# <a name="createmanagedfolderresponsemessage"></a><span data-ttu-id="bdadd-103">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdadd-103">CreateManagedFolderResponseMessage</span></span>

<span data-ttu-id="bdadd-104">Das **CreateManagedFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdadd-104">The **CreateManagedFolderResponseMessage** element contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="bdadd-105">CreateManagedFolderResponse</span><span class="sxs-lookup"><span data-stu-id="bdadd-105">CreateManagedFolderResponse</span></span>](createmanagedfolderresponse.md)  
- [<span data-ttu-id="bdadd-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bdadd-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="bdadd-107">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bdadd-107">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md)
  
```xml
<CreateManagedFolderResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateManagedFolderResponseMessage>
```

<span data-ttu-id="bdadd-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="bdadd-108">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bdadd-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bdadd-109">Attributes and elements</span></span>

<span data-ttu-id="bdadd-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bdadd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdadd-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="bdadd-111">Attributes</span></span>

|<span data-ttu-id="bdadd-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bdadd-112">**Attribute**</span></span>|<span data-ttu-id="bdadd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdadd-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdadd-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="bdadd-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="bdadd-115">Beschreibt den Status einer Antwort [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bdadd-115">Describes the status of a [CreateManagedFolder operation](createmanagedfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="bdadd-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="bdadd-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="bdadd-117">-Success</span><span class="sxs-lookup"><span data-stu-id="bdadd-117">-  Success</span></span>  <br/><span data-ttu-id="bdadd-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="bdadd-118">-  Warning</span></span>  <br/><span data-ttu-id="bdadd-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="bdadd-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="bdadd-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="bdadd-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="bdadd-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bdadd-121">**Value**</span></span>|<span data-ttu-id="bdadd-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdadd-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bdadd-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="bdadd-123">**Success**</span></span> <br/> |<span data-ttu-id="bdadd-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="bdadd-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="bdadd-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="bdadd-125">**Warning**</span></span> <br/> | <span data-ttu-id="bdadd-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="bdadd-126">Describes a request that was not processed.</span></span> <span data-ttu-id="bdadd-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="bdadd-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="bdadd-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="bdadd-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="bdadd-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="bdadd-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="bdadd-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="bdadd-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="bdadd-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="bdadd-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="bdadd-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="bdadd-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="bdadd-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="bdadd-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="bdadd-134">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="bdadd-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="bdadd-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="bdadd-135">**Error**</span></span> <br/> | <span data-ttu-id="bdadd-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bdadd-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="bdadd-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="bdadd-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="bdadd-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="bdadd-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="bdadd-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="bdadd-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="bdadd-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="bdadd-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="bdadd-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="bdadd-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="bdadd-142">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="bdadd-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="bdadd-143">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="bdadd-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="bdadd-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="bdadd-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bdadd-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdadd-145">Child elements</span></span>

|<span data-ttu-id="bdadd-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdadd-146">**Element**</span></span>|<span data-ttu-id="bdadd-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdadd-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdadd-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="bdadd-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="bdadd-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="bdadd-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="bdadd-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bdadd-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="bdadd-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="bdadd-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="bdadd-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="bdadd-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="bdadd-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="bdadd-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="bdadd-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="bdadd-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="bdadd-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="bdadd-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="bdadd-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="bdadd-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="bdadd-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="bdadd-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bdadd-158">Enthält ein Array von erstellte verwaltete Ordner.</span><span class="sxs-lookup"><span data-stu-id="bdadd-158">Contains an array of created managed folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdadd-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdadd-159">Parent elements</span></span>

|<span data-ttu-id="bdadd-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdadd-160">**Element**</span></span>|<span data-ttu-id="bdadd-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdadd-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdadd-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bdadd-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="bdadd-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bdadd-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdadd-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdadd-164">Remarks</span></span>

<span data-ttu-id="bdadd-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bdadd-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdadd-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bdadd-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdadd-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdadd-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bdadd-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bdadd-168">Schema Name</span></span>  <br/> |<span data-ttu-id="bdadd-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bdadd-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bdadd-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bdadd-170">Validation File</span></span>  <br/> |<span data-ttu-id="bdadd-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bdadd-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bdadd-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bdadd-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdadd-173">False</span><span class="sxs-lookup"><span data-stu-id="bdadd-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdadd-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdadd-174">See also</span></span>

- [<span data-ttu-id="bdadd-175">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bdadd-175">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
- [<span data-ttu-id="bdadd-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="bdadd-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="bdadd-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bdadd-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

