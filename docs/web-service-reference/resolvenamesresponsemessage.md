---
title: ResolveNamesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNamesResponseMessage
api_type:
- schema
ms.assetid: edcdaf58-ef63-412e-8c58-409213e6ab0d
description: Das ResolveNamesResponseMessage-Element enthält den Status und das Ergebnis einer ResolveNames Vorgang Anforderung.
ms.openlocfilehash: 953a1f0b19c078d969ffe175c22df02b58c5e939
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831170"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="2c480-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c480-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="2c480-104">Das **ResolveNamesResponseMessage** -Element enthält den Status und das Ergebnis einer Anforderung [ResolveNames Vorgang](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c480-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="2c480-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2c480-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="2c480-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2c480-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="2c480-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c480-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="2c480-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2c480-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c480-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c480-109">Attributes and elements</span></span>

<span data-ttu-id="2c480-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c480-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c480-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c480-111">Attributes</span></span>

|<span data-ttu-id="2c480-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2c480-112">**Attribute**</span></span>|<span data-ttu-id="2c480-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c480-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c480-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="2c480-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="2c480-115">Beschreibt den Status einer Antwort [ResolveNames Vorgang](resolvenames-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="2c480-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="2c480-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="2c480-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="2c480-117">-Success</span><span class="sxs-lookup"><span data-stu-id="2c480-117">-  Success</span></span>  <br/><span data-ttu-id="2c480-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="2c480-118">-  Warning</span></span>  <br/><span data-ttu-id="2c480-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="2c480-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="2c480-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="2c480-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="2c480-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2c480-121">**Value**</span></span>|<span data-ttu-id="2c480-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c480-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c480-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="2c480-123">**Success**</span></span> <br/> |<span data-ttu-id="2c480-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="2c480-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="2c480-125">Dies tritt auf, wenn der angeforderte Name eindeutig ist und die Antwort einen einzelnen Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="2c480-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="2c480-126">**Warning**</span><span class="sxs-lookup"><span data-stu-id="2c480-126">**Warning**</span></span> <br/> | <span data-ttu-id="2c480-127">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2c480-127">Describes a request that was not processed.</span></span> <span data-ttu-id="2c480-128">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="2c480-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="2c480-129">Im folgenden sind die Quellen der Warnungen Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2c480-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="2c480-130">-Der Exchange-Speicher wird während der Batchaktualisierung offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2c480-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="2c480-131">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2c480-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="2c480-132">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="2c480-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="2c480-133">-Die Postfachdatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="2c480-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="2c480-134">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="2c480-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="2c480-135">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="2c480-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="2c480-136">-Der angeforderte Name ist nicht eindeutig und die Antwort enthält mehrere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2c480-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="2c480-137">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="2c480-137">**Error**</span></span> <br/> | <span data-ttu-id="2c480-138">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c480-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="2c480-139">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="2c480-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="2c480-140">-Der angeforderte Namen konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2c480-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="2c480-141">-Attribute oder Elemente sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="2c480-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="2c480-142">-Attribute oder Elemente sind außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="2c480-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="2c480-143">-Ein Tag ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2c480-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="2c480-144">-Eines Attributs oder Elements ist ungültig im Kontext.</span><span class="sxs-lookup"><span data-stu-id="2c480-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="2c480-145">-Ein nicht autorisierten Zugriffsversuch von einem Client aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2c480-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="2c480-146">-Serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="2c480-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="2c480-147">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2c480-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c480-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c480-148">Child elements</span></span>

|<span data-ttu-id="2c480-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c480-149">**Element**</span></span>|<span data-ttu-id="2c480-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c480-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c480-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="2c480-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2c480-152">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="2c480-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2c480-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c480-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2c480-154">Enthält Fehlerinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c480-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="2c480-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2c480-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2c480-156">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="2c480-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="2c480-157">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="2c480-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="2c480-158">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2c480-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2c480-159">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="2c480-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2c480-160">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="2c480-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="2c480-161">Enthält ein Array von Lösungen für ein mehrdeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="2c480-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c480-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c480-162">Parent elements</span></span>

|<span data-ttu-id="2c480-163">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c480-163">**Element**</span></span>|<span data-ttu-id="2c480-164">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c480-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c480-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2c480-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2c480-166">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c480-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c480-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c480-167">Remarks</span></span>

<span data-ttu-id="2c480-168">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c480-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c480-169">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2c480-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c480-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c480-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2c480-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c480-171">Schema name</span></span>  <br/> |<span data-ttu-id="2c480-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2c480-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2c480-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c480-173">Validation file</span></span>  <br/> |<span data-ttu-id="2c480-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2c480-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2c480-175">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2c480-175">Can be empty</span></span>  <br/> |<span data-ttu-id="2c480-176">False</span><span class="sxs-lookup"><span data-stu-id="2c480-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c480-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c480-177">See also</span></span>

- [<span data-ttu-id="2c480-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2c480-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="2c480-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2c480-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="2c480-180">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c480-180">ResolveNames operation</span></span>](resolvenames-operation.md)

