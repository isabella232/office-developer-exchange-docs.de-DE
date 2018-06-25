---
title: MoveFolderResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolderResponseMessage
api_type:
- schema
ms.assetid: 54917251-96af-44c2-ae90-d545f0a16e2e
description: Das MoveFolderResponseMessage-Element enthält den Status und das Ergebnis einer Anforderung MoveFolder-Vorgang.
ms.openlocfilehash: 777520bf6a093882da95a7bfd466b66acdab957c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830496"
---
# <a name="movefolderresponsemessage"></a><span data-ttu-id="67fe3-103">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="67fe3-103">MoveFolderResponseMessage</span></span>

<span data-ttu-id="67fe3-104">Das **MoveFolderResponseMessage** -Element enthält, der Status und das Ergebnis einer einzelnen Anforderung [MoveFolder-Vorgang](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="67fe3-104">The **MoveFolderResponseMessage** element contains the status and result of a single [MoveFolder operation](movefolder-operation.md) request.</span></span> 
  
- [<span data-ttu-id="67fe3-105">MoveFolderResponse</span><span class="sxs-lookup"><span data-stu-id="67fe3-105">MoveFolderResponse</span></span>](movefolderresponse.md)
- [<span data-ttu-id="67fe3-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="67fe3-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="67fe3-107">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="67fe3-107">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md)
  
```xml
<MoveFolderResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Folders/>
</MoveFolderResponseMessage>
```

 <span data-ttu-id="67fe3-108">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="67fe3-108">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67fe3-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="67fe3-109">Attributes and elements</span></span>

<span data-ttu-id="67fe3-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="67fe3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67fe3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="67fe3-111">Attributes</span></span>

|<span data-ttu-id="67fe3-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="67fe3-112">**Attribute**</span></span>|<span data-ttu-id="67fe3-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67fe3-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67fe3-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="67fe3-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="67fe3-115">Beschreibt den Status einer Antwort [MoveFolder-Vorgang](movefolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="67fe3-115">Describes the status of a [MoveFolder operation](movefolder-operation.md) response.</span></span> <br/><br/><span data-ttu-id="67fe3-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="67fe3-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="67fe3-117">-Success</span><span class="sxs-lookup"><span data-stu-id="67fe3-117">-  Success</span></span>  <br/><span data-ttu-id="67fe3-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="67fe3-118">-  Warning</span></span>  <br/><span data-ttu-id="67fe3-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="67fe3-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="67fe3-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="67fe3-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="67fe3-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="67fe3-121">**Value**</span></span>|<span data-ttu-id="67fe3-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67fe3-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67fe3-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="67fe3-123">**Success**</span></span> <br/> |<span data-ttu-id="67fe3-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="67fe3-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="67fe3-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="67fe3-125">**Warning**</span></span> <br/> | <span data-ttu-id="67fe3-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="67fe3-126">Describes a request that was not processed.</span></span> <span data-ttu-id="67fe3-127">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="67fe3-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="67fe3-128">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="67fe3-128">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="67fe3-129">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="67fe3-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="67fe3-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="67fe3-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="67fe3-131">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="67fe3-131">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="67fe3-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="67fe3-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="67fe3-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="67fe3-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="67fe3-134">-Ein Kontingent überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="67fe3-134">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="67fe3-135">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="67fe3-135">**Error**</span></span> <br/> | <span data-ttu-id="67fe3-136">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="67fe3-136">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="67fe3-137">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="67fe3-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="67fe3-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="67fe3-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="67fe3-139">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="67fe3-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="67fe3-140">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="67fe3-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="67fe3-141">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="67fe3-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="67fe3-142">-Alle Versuch nicht autorisierten Zugriff von jedem client</span><span class="sxs-lookup"><span data-stu-id="67fe3-142">-  Any unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="67fe3-143">-Alle serverseitigen Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="67fe3-143">-  Any server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="67fe3-144">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="67fe3-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67fe3-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67fe3-145">Child elements</span></span>

|<span data-ttu-id="67fe3-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="67fe3-146">**Element**</span></span>|<span data-ttu-id="67fe3-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67fe3-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67fe3-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="67fe3-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="67fe3-149">Beschreibender Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="67fe3-149">A text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="67fe3-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="67fe3-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="67fe3-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="67fe3-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="67fe3-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="67fe3-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="67fe3-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="67fe3-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="67fe3-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="67fe3-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="67fe3-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="67fe3-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="67fe3-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="67fe3-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="67fe3-157">Ordner</span><span class="sxs-lookup"><span data-stu-id="67fe3-157">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="67fe3-158">Enthält ein Array von verschobenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="67fe3-158">Contains an array of moved folders.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67fe3-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67fe3-159">Parent elements</span></span>

|<span data-ttu-id="67fe3-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="67fe3-160">**Element**</span></span>|<span data-ttu-id="67fe3-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67fe3-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67fe3-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="67fe3-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="67fe3-163">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="67fe3-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67fe3-164">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67fe3-164">Remarks</span></span>

<span data-ttu-id="67fe3-165">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="67fe3-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67fe3-166">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="67fe3-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67fe3-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="67fe3-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67fe3-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="67fe3-168">Schema Name</span></span>  <br/> |<span data-ttu-id="67fe3-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="67fe3-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="67fe3-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="67fe3-170">Validation File</span></span>  <br/> |<span data-ttu-id="67fe3-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="67fe3-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67fe3-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="67fe3-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="67fe3-173">False</span><span class="sxs-lookup"><span data-stu-id="67fe3-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67fe3-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67fe3-174">See also</span></span>

- [<span data-ttu-id="67fe3-175">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="67fe3-175">MoveFolder</span></span>](movefolder.md)
- [<span data-ttu-id="67fe3-176">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="67fe3-176">MoveFolder operation</span></span>](movefolder-operation.md)

