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
description: Das ResolveNamesResponseMessage-Element enthält den Status und das Ergebnis einer ResolveNames-Vorgangsanforderung.
ms.openlocfilehash: 12f32008dbbc603fca7adf26057f1f1904d3cfb2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455597"
---
# <a name="resolvenamesresponsemessage"></a><span data-ttu-id="39b06-103">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39b06-103">ResolveNamesResponseMessage</span></span>

<span data-ttu-id="39b06-104">Das **ResolveNamesResponseMessage** -Element enthält den Status und das Ergebnis einer [ResolveNames-Vorgangs](resolvenames-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39b06-104">The **ResolveNamesResponseMessage** element contains the status and result of a [ResolveNames operation](resolvenames-operation.md) request.</span></span> 
  
- [<span data-ttu-id="39b06-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="39b06-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md) 
- [<span data-ttu-id="39b06-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39b06-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="39b06-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39b06-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
```xml
<ResolveNamesResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResolutionSet/>
</ResolveNamesResponseMessage>
```

 <span data-ttu-id="39b06-108">**ResolveNamesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="39b06-108">**ResolveNamesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39b06-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39b06-109">Attributes and elements</span></span>

<span data-ttu-id="39b06-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39b06-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39b06-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="39b06-111">Attributes</span></span>

|<span data-ttu-id="39b06-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="39b06-112">**Attribute**</span></span>|<span data-ttu-id="39b06-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39b06-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39b06-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="39b06-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="39b06-115">Beschreibt den Status einer [ResolveNames-Vorgangs](resolvenames-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="39b06-115">Describes the status of a [ResolveNames operation](resolvenames-operation.md) response.</span></span> <br/><br/><span data-ttu-id="39b06-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="39b06-116">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="39b06-117">-Success</span><span class="sxs-lookup"><span data-stu-id="39b06-117">-  Success</span></span>  <br/><span data-ttu-id="39b06-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="39b06-118">-  Warning</span></span>  <br/><span data-ttu-id="39b06-119">-Error</span><span class="sxs-lookup"><span data-stu-id="39b06-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="39b06-120">ResponseClass-Attribut</span><span class="sxs-lookup"><span data-stu-id="39b06-120">ResponseClass Attribute</span></span>

|<span data-ttu-id="39b06-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="39b06-121">**Value**</span></span>|<span data-ttu-id="39b06-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39b06-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39b06-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="39b06-123">**Success**</span></span> <br/> |<span data-ttu-id="39b06-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="39b06-124">Describes a request that is fulfilled.</span></span> <span data-ttu-id="39b06-125">Dies tritt auf, wenn der angeforderte Name eindeutig ist und die Antwort einen einzelnen Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="39b06-125">This occurs when the requested name is unambiguous and the response contains a single recipient.</span></span>  <br/> |
|<span data-ttu-id="39b06-126">**Warning**</span><span class="sxs-lookup"><span data-stu-id="39b06-126">**Warning**</span></span> <br/> | <span data-ttu-id="39b06-127">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="39b06-127">Describes a request that was not processed.</span></span> <span data-ttu-id="39b06-128">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="39b06-128">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="39b06-129">Im folgenden finden Sie ein Beispiel für Warn Quellen:</span><span class="sxs-lookup"><span data-stu-id="39b06-129">The following are example of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="39b06-130">– Der Exchange-Informationsspeicher wird während des Batches offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="39b06-130">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="39b06-131">-Active Directory-Domänendienste (AD DS) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="39b06-131">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="39b06-132">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="39b06-132">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="39b06-133">-Die Postfachdatenbank (MDB) wird offline geschaltet.</span><span class="sxs-lookup"><span data-stu-id="39b06-133">-  The mailbox database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="39b06-134">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="39b06-134">-  A password is expired.</span></span>  <br/><span data-ttu-id="39b06-135">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="39b06-135">-  A quota is exceeded.</span></span>  <br/><span data-ttu-id="39b06-136">-Der angeforderte Name ist mehrdeutig, und die Antwort enthält mehrere Empfänger.</span><span class="sxs-lookup"><span data-stu-id="39b06-136">-  The requested name is ambiguous and the response contains multiple recipients.</span></span>  <br/> |
|<span data-ttu-id="39b06-137">**Error**</span><span class="sxs-lookup"><span data-stu-id="39b06-137">**Error**</span></span> <br/> | <span data-ttu-id="39b06-138">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="39b06-138">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="39b06-139">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="39b06-139">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="39b06-140">-Der angeforderte Name konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="39b06-140">-  The requested name could not be resolved.</span></span>  <br/><span data-ttu-id="39b06-141">-Attribute oder Elemente sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="39b06-141">-  Attributes or elements are invalid.</span></span>  <br/><span data-ttu-id="39b06-142">-Attribute oder Elemente liegen außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="39b06-142">-  Attributes or elements are out of range.</span></span>  <br/><span data-ttu-id="39b06-143">-Ein Tag ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="39b06-143">-  A tag is unknown.</span></span>  <br/><span data-ttu-id="39b06-144">-Ein Attribut oder Element ist im Kontext ungültig.</span><span class="sxs-lookup"><span data-stu-id="39b06-144">-  An attribute or element is not valid in the context.</span></span>  <br/><span data-ttu-id="39b06-145">-Ein nicht autorisierter Zugriff durch einen Client ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="39b06-145">-  An unauthorized access attempt by any client occurred.</span></span>  <br/><span data-ttu-id="39b06-146">-Ein serverseitiger Fehler trat als Reaktion auf einen gültigen clientseitigen Anruf auf.</span><span class="sxs-lookup"><span data-stu-id="39b06-146">-  A server-side failure occurred in response to a valid client-side call.</span></span>  <br/>  <br/><span data-ttu-id="39b06-147">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="39b06-147">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39b06-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39b06-148">Child elements</span></span>

|<span data-ttu-id="39b06-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="39b06-149">**Element**</span></span>|<span data-ttu-id="39b06-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39b06-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39b06-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="39b06-151">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="39b06-152">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="39b06-152">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="39b06-153">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39b06-153">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="39b06-154">Enthält Fehlerinformationen zur Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39b06-154">Provides error information about the request.</span></span>  <br/> |
|[<span data-ttu-id="39b06-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="39b06-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="39b06-156">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="39b06-156">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="39b06-157">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="39b06-157">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="39b06-158">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="39b06-158">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="39b06-159">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="39b06-159">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="39b06-160">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="39b06-160">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="39b06-161">Enthält ein Array von Auflösungen für einen eindeutigen Namen.</span><span class="sxs-lookup"><span data-stu-id="39b06-161">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39b06-162">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39b06-162">Parent elements</span></span>

|<span data-ttu-id="39b06-163">**Element**</span><span class="sxs-lookup"><span data-stu-id="39b06-163">**Element**</span></span>|<span data-ttu-id="39b06-164">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39b06-164">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39b06-165">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39b06-165">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="39b06-166">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39b06-166">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39b06-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39b06-167">Remarks</span></span>

<span data-ttu-id="39b06-168">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="39b06-168">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39b06-169">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="39b06-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39b06-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="39b06-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39b06-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39b06-171">Schema name</span></span>  <br/> |<span data-ttu-id="39b06-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="39b06-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="39b06-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39b06-173">Validation file</span></span>  <br/> |<span data-ttu-id="39b06-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="39b06-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39b06-175">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="39b06-175">Can be empty</span></span>  <br/> |<span data-ttu-id="39b06-176">False</span><span class="sxs-lookup"><span data-stu-id="39b06-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39b06-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39b06-177">See also</span></span>

- [<span data-ttu-id="39b06-178">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="39b06-178">ResolveNames</span></span>](resolvenames.md)
- [<span data-ttu-id="39b06-179">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="39b06-179">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
- [<span data-ttu-id="39b06-180">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39b06-180">ResolveNames operation</span></span>](resolvenames-operation.md)

