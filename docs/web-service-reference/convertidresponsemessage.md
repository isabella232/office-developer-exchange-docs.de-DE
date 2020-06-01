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
description: Das ConvertIdResponseMessage-Element enthält den Status und das Ergebnis einer Convert-Anforderung für den Konvertierungsvorgang.
ms.openlocfilehash: cd0154f87390be3516ced4be53f5371d4a348c49
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456220"
---
# <a name="convertidresponsemessage"></a><span data-ttu-id="6e682-103">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6e682-103">ConvertIdResponseMessage</span></span>

<span data-ttu-id="6e682-104">Das **ConvertIdResponseMessage** -Element enthält den Status und das Ergebnis einer Convert-Anforderung für den [Konvertierungsvorgang](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6e682-104">The **ConvertIdResponseMessage** element contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span> 
  
- [<span data-ttu-id="6e682-105">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="6e682-105">ConvertIdResponse</span></span>](convertidresponse.md) 
- [<span data-ttu-id="6e682-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6e682-106">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="6e682-107">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6e682-107">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md)
  
```xml
<ConvertIdResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <AlternateId/>
</ConvertIdResponseMessage>
```

 <span data-ttu-id="6e682-108">**ConvertIdResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6e682-108">**ConvertIdResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e682-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e682-109">Attributes and elements</span></span>

<span data-ttu-id="6e682-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6e682-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e682-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e682-111">Attributes</span></span>

|<span data-ttu-id="6e682-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6e682-112">**Attribute**</span></span>|<span data-ttu-id="6e682-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e682-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e682-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="6e682-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="6e682-115">Beschreibt den Status einer Antwort auf eine [Konvertierung des Vorgangs](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6e682-115">Describes the status of a [ConvertId operation](convertid-operation.md) response.</span></span><br/><br/><span data-ttu-id="6e682-116">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="6e682-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="6e682-117">-Success</span><span class="sxs-lookup"><span data-stu-id="6e682-117">- Success</span></span>  <br/><span data-ttu-id="6e682-118">-Warnung</span><span class="sxs-lookup"><span data-stu-id="6e682-118">-  Warning</span></span>  <br/><span data-ttu-id="6e682-119">-Error</span><span class="sxs-lookup"><span data-stu-id="6e682-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="6e682-120">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="6e682-120">ResponseClass attribute values</span></span>

|<span data-ttu-id="6e682-121">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6e682-121">**Value**</span></span>|<span data-ttu-id="6e682-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e682-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e682-123">**Success**</span><span class="sxs-lookup"><span data-stu-id="6e682-123">**Success**</span></span> <br/> |<span data-ttu-id="6e682-124">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="6e682-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="6e682-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="6e682-125">**Warning**</span></span> <br/> | <span data-ttu-id="6e682-126">Beschreibt eine Anforderung, die nicht vollständig verarbeitet wurde oder für die ein unbeabsichtigtes Ergebnis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6e682-126">Describes a request that was not fully processed or for which an unintended result occurred.</span></span>  <br/> |
|<span data-ttu-id="6e682-127">**Error**</span><span class="sxs-lookup"><span data-stu-id="6e682-127">**Error**</span></span> <br/> | <span data-ttu-id="6e682-128">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e682-128">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="6e682-129">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="6e682-129">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="6e682-130">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="6e682-130">- Invalid attributes or elements</span></span>  <br/><span data-ttu-id="6e682-131">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="6e682-131">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="6e682-132">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="6e682-132">-  An unknown tag</span></span>  <br/><span data-ttu-id="6e682-133">-Ein Attribut oder Element, das im Kontext ungültig ist</span><span class="sxs-lookup"><span data-stu-id="6e682-133">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="6e682-134">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="6e682-134">- An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="6e682-135">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="6e682-135">-  A server-side failure in response to a valid client-side call</span></span><br/><br/><span data-ttu-id="6e682-136">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="6e682-136">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e682-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e682-137">Child elements</span></span>

|<span data-ttu-id="6e682-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e682-138">**Element**</span></span>|<span data-ttu-id="6e682-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e682-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e682-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="6e682-140">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6e682-141">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6e682-141">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6e682-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6e682-142">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6e682-143">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6e682-143">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="6e682-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6e682-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6e682-145">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6e682-145">Currently unused and reserved for future use.</span></span> <span data-ttu-id="6e682-146">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="6e682-146">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="6e682-147">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="6e682-147">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6e682-148">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="6e682-148">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6e682-149">AlternateId</span><span class="sxs-lookup"><span data-stu-id="6e682-149">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="6e682-150">Beschreibt einen konvertierten Bezeichner in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="6e682-150">Describes a converted identifier in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6e682-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e682-151">Parent elements</span></span>

|<span data-ttu-id="6e682-152">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e682-152">**Element**</span></span>|<span data-ttu-id="6e682-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6e682-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e682-154">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6e682-154">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6e682-155">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6e682-155">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e682-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e682-156">Remarks</span></span>

<span data-ttu-id="6e682-157">Es wird eine Antwortnachricht pro konvertierten Bezeichner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e682-157">One response message per converted identifier is returned.</span></span> <span data-ttu-id="6e682-158">Das [Alternate](alternateid.md) -Element wird in der Antwort fehlen, wenn ein Fehlerantwort Code zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e682-158">The [AlternateId](alternateid.md) element will be missing from the response if an error response code is returned,</span></span> 
  
<span data-ttu-id="6e682-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange 2010 ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e682-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e682-160">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6e682-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e682-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e682-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6e682-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6e682-162">Schema Name</span></span>  <br/> |<span data-ttu-id="6e682-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="6e682-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6e682-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6e682-164">Validation File</span></span>  <br/> |<span data-ttu-id="6e682-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6e682-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6e682-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6e682-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e682-167">False</span><span class="sxs-lookup"><span data-stu-id="6e682-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e682-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e682-168">See also</span></span>

- [<span data-ttu-id="6e682-169">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6e682-169">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="6e682-170">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6e682-170">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

