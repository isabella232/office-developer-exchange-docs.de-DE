---
title: CreateItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItemResponseMessage
api_type:
- schema
ms.assetid: 595d36c2-f87a-4d50-8e8b-f58d7641564b
description: Das CreateItemResponseMessage-Element enthält den Status und das Ergebnis einer einzelnen CreateItem-Vorgangsanforderung.
ms.openlocfilehash: 6304d2c7a3c9253c03c07eb37e9a57226e794a24
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457851"
---
# <a name="createitemresponsemessage"></a><span data-ttu-id="8cfb8-103">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8cfb8-103">CreateItemResponseMessage</span></span>

<span data-ttu-id="8cfb8-104">Das **CreateItemResponseMessage** -Element enthält den Status und das Ergebnis einer einzelnen [CreateItem-Vorgangs](createitem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-104">The **CreateItemResponseMessage** element contains the status and result of a single [CreateItem operation](createitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="8cfb8-105">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="8cfb8-105">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="8cfb8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8cfb8-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="8cfb8-107">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8cfb8-107">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
  
```xml
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 <span data-ttu-id="8cfb8-108">**ItemInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-108">**ItemInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8cfb8-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8cfb8-109">Attributes and elements</span></span>

<span data-ttu-id="8cfb8-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cfb8-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="8cfb8-111">Attributes</span></span>

|<span data-ttu-id="8cfb8-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-112">**Attribute**</span></span>|<span data-ttu-id="8cfb8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cfb8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="8cfb8-115">Beschreibt den Status einer [CreateItem-Vorgangs](createitem-operation.md) Antwort.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-115">Describes the status of a [CreateItem operation](createitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="8cfb8-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="8cfb8-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="8cfb8-117">-Success</span><span class="sxs-lookup"><span data-stu-id="8cfb8-117">-  Success</span></span>  <br/><span data-ttu-id="8cfb8-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="8cfb8-118">-  Warning</span></span>  <br/><span data-ttu-id="8cfb8-119">-Error</span><span class="sxs-lookup"><span data-stu-id="8cfb8-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="8cfb8-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="8cfb8-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="8cfb8-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-121">**Value**</span></span>|<span data-ttu-id="8cfb8-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cfb8-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-123">**Success**</span></span> <br/> |<span data-ttu-id="8cfb8-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="8cfb8-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-125">**Warning**</span></span> <br/> | <span data-ttu-id="8cfb8-126">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-126">Describes a request that was not processed.</span></span> <span data-ttu-id="8cfb8-127">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="8cfb8-128">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="8cfb8-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="8cfb8-129">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-129">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="8cfb8-130">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-130">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="8cfb8-131">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="8cfb8-132">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-132">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="8cfb8-133">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="8cfb8-134">-Ein Kontingent wird überschritten.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="8cfb8-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-135">**Error**</span></span> <br/> | <span data-ttu-id="8cfb8-136">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="8cfb8-137">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="8cfb8-137">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="8cfb8-138">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="8cfb8-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="8cfb8-139">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="8cfb8-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="8cfb8-140">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="8cfb8-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="8cfb8-141">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="8cfb8-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="8cfb8-142">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="8cfb8-142">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="8cfb8-143">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="8cfb8-143">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="8cfb8-144">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="8cfb8-144">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8cfb8-145">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cfb8-145">Child elements</span></span>

|<span data-ttu-id="8cfb8-146">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-146">**Element**</span></span>|<span data-ttu-id="8cfb8-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cfb8-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="8cfb8-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="8cfb8-149">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="8cfb8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8cfb8-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="8cfb8-151">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="8cfb8-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8cfb8-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="8cfb8-153">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="8cfb8-154">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="8cfb8-155">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="8cfb8-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="8cfb8-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-156">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="8cfb8-157">Elemente</span><span class="sxs-lookup"><span data-stu-id="8cfb8-157">Items</span></span>](items.md) <br/> |<span data-ttu-id="8cfb8-158">Enthält ein Array erstellter Elemente.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-158">Contains an array of created items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8cfb8-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cfb8-159">Parent elements</span></span>

|<span data-ttu-id="8cfb8-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-160">**Element**</span></span>|<span data-ttu-id="8cfb8-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cfb8-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cfb8-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8cfb8-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8cfb8-163">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cfb8-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cfb8-164">Remarks</span></span>

<span data-ttu-id="8cfb8-165">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cfb8-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8cfb8-166">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8cfb8-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cfb8-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cfb8-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8cfb8-168">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8cfb8-168">Schema Name</span></span>  <br/> |<span data-ttu-id="8cfb8-169">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8cfb8-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8cfb8-170">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8cfb8-170">Validation File</span></span>  <br/> |<span data-ttu-id="8cfb8-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8cfb8-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8cfb8-172">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8cfb8-172">Can be Empty</span></span>  <br/> |<span data-ttu-id="8cfb8-173">False</span><span class="sxs-lookup"><span data-stu-id="8cfb8-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cfb8-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cfb8-174">See also</span></span>

- [<span data-ttu-id="8cfb8-175">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8cfb8-175">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="8cfb8-176">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="8cfb8-176">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="8cfb8-177">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cfb8-177">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

