---
title: CreateFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolderResponseMessage
api_type:
- schema
ms.assetid: 1301dd15-b008-4fd9-8c89-b15a20b186e2
description: Das CreateFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung CreateFolder-Vorgang.
ms.openlocfilehash: c587cca1f935b295a0ed30ab2210de40af28d06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757768"
---
# <a name="createfolderresponsemessage"></a><span data-ttu-id="448dc-103">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="448dc-103">CreateFolderResponseMessage</span></span>

<span data-ttu-id="448dc-104">Das **CreateFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [CreateFolder-Vorgang](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="448dc-104">The **CreateFolderResponseMessage** element contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span> 
  
```xml
<CreateFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</CreateFolderResponseMessage>
```

<span data-ttu-id="448dc-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="448dc-105">**FolderInfoResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="448dc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="448dc-106">Attributes and elements</span></span>

<span data-ttu-id="448dc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="448dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="448dc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="448dc-108">Attributes</span></span>

|<span data-ttu-id="448dc-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="448dc-109">**Attribute**</span></span>|<span data-ttu-id="448dc-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="448dc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="448dc-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="448dc-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="448dc-112">Beschreibt den Status einer Antwort [CreateFolder-Vorgang](createfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="448dc-112">Describes the status of a [CreateFolder operation](createfolder-operation.md) response.</span></span><br/><br/><span data-ttu-id="448dc-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="448dc-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="448dc-114">-Success</span><span class="sxs-lookup"><span data-stu-id="448dc-114">-  Success</span></span>  <br/><span data-ttu-id="448dc-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="448dc-115">-  Warning</span></span>  <br/><span data-ttu-id="448dc-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="448dc-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="448dc-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="448dc-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="448dc-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="448dc-118">**Value**</span></span>|<span data-ttu-id="448dc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="448dc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="448dc-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="448dc-120">**Success**</span></span> <br/> |<span data-ttu-id="448dc-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="448dc-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="448dc-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="448dc-122">**Warning**</span></span> <br/> | <span data-ttu-id="448dc-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="448dc-123">Describes a request that was not processed.</span></span> <span data-ttu-id="448dc-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="448dc-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="448dc-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="448dc-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="448dc-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="448dc-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="448dc-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="448dc-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="448dc-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="448dc-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="448dc-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="448dc-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="448dc-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="448dc-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="448dc-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="448dc-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="448dc-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="448dc-132">**Error**</span></span> <br/> | <span data-ttu-id="448dc-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="448dc-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="448dc-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="448dc-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="448dc-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="448dc-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="448dc-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="448dc-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="448dc-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="448dc-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="448dc-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="448dc-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="448dc-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="448dc-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="448dc-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="448dc-140">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="448dc-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="448dc-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="448dc-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="448dc-142">Child elements</span></span>

|<span data-ttu-id="448dc-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="448dc-143">**Element**</span></span>|<span data-ttu-id="448dc-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="448dc-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="448dc-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="448dc-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="448dc-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="448dc-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="448dc-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="448dc-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="448dc-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="448dc-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="448dc-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="448dc-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="448dc-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="448dc-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="448dc-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="448dc-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="448dc-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="448dc-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="448dc-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="448dc-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="448dc-154">Ordner</span><span class="sxs-lookup"><span data-stu-id="448dc-154">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="448dc-155">Enthält ein Array von erstellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="448dc-155">Contains an array of created folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="448dc-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="448dc-156">Parent elements</span></span>

|<span data-ttu-id="448dc-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="448dc-157">**Element**</span></span>|<span data-ttu-id="448dc-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="448dc-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="448dc-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="448dc-159">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="448dc-160">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="448dc-160">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="448dc-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="448dc-161">Remarks</span></span>

<span data-ttu-id="448dc-162">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="448dc-162">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="448dc-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="448dc-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="448dc-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="448dc-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="448dc-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="448dc-165">Schema Name</span></span>  <br/> |<span data-ttu-id="448dc-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="448dc-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="448dc-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="448dc-167">Validation File</span></span>  <br/> |<span data-ttu-id="448dc-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="448dc-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="448dc-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="448dc-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="448dc-170">False</span><span class="sxs-lookup"><span data-stu-id="448dc-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="448dc-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="448dc-171">See also</span></span>

- [<span data-ttu-id="448dc-172">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="448dc-172">CreateFolder operation</span></span>](createfolder-operation.md)
- [<span data-ttu-id="448dc-173">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="448dc-173">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md) 
- [<span data-ttu-id="448dc-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="448dc-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

