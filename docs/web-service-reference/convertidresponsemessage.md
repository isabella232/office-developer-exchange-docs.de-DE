---
title: ConvertIdResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponseMessage
api_type:
- schema
ms.assetid: 7a439cae-0268-4328-9ded-af56ad642227
description: Das ConvertIdResponseMessage-Element enthält den Status und das Ergebnis einer ConvertId Vorgang Anforderung.
ms.openlocfilehash: 6668c0b3254191ca628413bae5ff957c3cb95b5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757721"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="28c9b-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28c9b-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="28c9b-104">Das **ConvertIdResponseMessage** -Element enthält den Status und das Ergebnis einer Anforderung [ConvertId Vorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28c9b-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="28c9b-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="28c9b-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="28c9b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="28c9b-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="28c9b-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28c9b-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="28c9b-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="28c9b-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28c9b-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28c9b-109">Attributes and elements</span></span>

<span data-ttu-id="28c9b-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28c9b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28c9b-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="28c9b-111">Attributes</span></span>

|<span data-ttu-id="28c9b-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="28c9b-112">**Attribute**</span></span>|<span data-ttu-id="28c9b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c9b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28c9b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="28c9b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="28c9b-115">Beschreibt den Status einer Antwort [ConvertId Vorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28c9b-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="28c9b-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="28c9b-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="28c9b-117">-Success</span><span class="sxs-lookup"><span data-stu-id="28c9b-117">- Success</span></span>  <br/><span data-ttu-id="28c9b-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="28c9b-118">-  Warning</span></span>  <br/><span data-ttu-id="28c9b-119">-Fehler</span><span class="sxs-lookup"><span data-stu-id="28c9b-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="28c9b-120">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="28c9b-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="28c9b-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="28c9b-121">**Value**</span></span>|<span data-ttu-id="28c9b-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c9b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28c9b-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="28c9b-123">**Success**</span></span> <br/> |<span data-ttu-id="28c9b-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="28c9b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="28c9b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="28c9b-125">**Warning**</span></span> <br/> | <span data-ttu-id="28c9b-126">Beschreibt eine Anforderung, die nicht vollständig verarbeitet oder für die ein unbeabsichtigten Ergebnis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="28c9b-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="28c9b-127">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="28c9b-127">**Error**</span></span> <br/> | <span data-ttu-id="28c9b-128">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="28c9b-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="28c9b-129">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="28c9b-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="28c9b-130">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="28c9b-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="28c9b-131">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="28c9b-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="28c9b-132">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="28c9b-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="28c9b-133">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="28c9b-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="28c9b-134">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="28c9b-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="28c9b-135">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="28c9b-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="28c9b-136">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="28c9b-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28c9b-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c9b-137">Child elements</span></span>

|<span data-ttu-id="28c9b-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="28c9b-138">**Element**</span></span>|<span data-ttu-id="28c9b-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c9b-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c9b-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="28c9b-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="28c9b-141">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="28c9b-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="28c9b-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="28c9b-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="28c9b-143">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="28c9b-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="28c9b-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="28c9b-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="28c9b-145">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="28c9b-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="28c9b-146">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="28c9b-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="28c9b-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="28c9b-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="28c9b-148">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="28c9b-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="28c9b-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="28c9b-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="28c9b-150">Beschreibt einen konvertierten Bezeichner in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="28c9b-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28c9b-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c9b-151">Parent elements</span></span>

|<span data-ttu-id="28c9b-152">**Element**</span><span class="sxs-lookup"><span data-stu-id="28c9b-152">**Element**</span></span>|<span data-ttu-id="28c9b-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c9b-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c9b-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="28c9b-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="28c9b-155">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="28c9b-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28c9b-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28c9b-156">Remarks</span></span>

<span data-ttu-id="28c9b-157">Eine Antwortnachricht pro konvertierten Bezeichner wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28c9b-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="28c9b-158">[AlternateId](alternateid.md) -Element wird in der Antwort nicht vorhanden sein, wenn ein Fehlercode Antwort zurückgegeben wird,</span><span class="sxs-lookup"><span data-stu-id="28c9b-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="28c9b-159">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="28c9b-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28c9b-160">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28c9b-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28c9b-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="28c9b-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28c9b-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28c9b-162">Schema Name</span></span>  <br/> |<span data-ttu-id="28c9b-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="28c9b-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28c9b-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28c9b-164">Validation File</span></span>  <br/> |<span data-ttu-id="28c9b-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28c9b-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28c9b-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28c9b-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="28c9b-167">False</span><span class="sxs-lookup"><span data-stu-id="28c9b-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28c9b-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28c9b-168">See also</span></span>

- [<span data-ttu-id="28c9b-169">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28c9b-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="28c9b-170">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28c9b-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

