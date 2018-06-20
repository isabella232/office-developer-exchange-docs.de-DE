---
title: DeleteUserConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfigurationResponseMessage
api_type:
- schema
ms.assetid: 543b1743-7e1c-4acb-93bd-34532e7fe79b
description: Das DeleteUserConfigurationResponseMessage-Element enthält den Status und das Ergebnis einer DeleteUserConfiguration Anforderung.
ms.openlocfilehash: 3e07917688ad1f25f7ca3fa06d6db51cf9905503
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757942"
---
# <a name="deleteuserconfigurationresponsemessage"></a><span data-ttu-id="e288c-103">DeleteUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e288c-103">DeleteUserConfigurationResponseMessage</span></span>

<span data-ttu-id="e288c-104">Das **DeleteUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer **DeleteUserConfiguration** Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e288c-104">The **DeleteUserConfigurationResponseMessage** element contains the status and result of a single **DeleteUserConfiguration** request.</span></span> 
  
```xml
<DeleteUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteUserConfigurationResponseMessage>
```

 <span data-ttu-id="e288c-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e288c-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e288c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e288c-106">Attributes and elements</span></span>

<span data-ttu-id="e288c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e288c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e288c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e288c-108">Attributes</span></span>

|<span data-ttu-id="e288c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e288c-109">**Attribute**</span></span>|<span data-ttu-id="e288c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e288c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e288c-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="e288c-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="e288c-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e288c-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="e288c-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="e288c-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="e288c-114">-Success</span><span class="sxs-lookup"><span data-stu-id="e288c-114">-  Success</span></span>  <br/><span data-ttu-id="e288c-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="e288c-115">-  Warning</span></span>  <br/><span data-ttu-id="e288c-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="e288c-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="e288c-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="e288c-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="e288c-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e288c-118">**Value**</span></span>|<span data-ttu-id="e288c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e288c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e288c-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="e288c-120">**Success**</span></span> <br/> |<span data-ttu-id="e288c-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="e288c-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="e288c-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="e288c-122">**Warning**</span></span> <br/> | <span data-ttu-id="e288c-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e288c-123">Describes a request that was not processed.</span></span> <span data-ttu-id="e288c-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e288c-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="e288c-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="e288c-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="e288c-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="e288c-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="e288c-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e288c-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="e288c-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="e288c-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="e288c-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="e288c-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="e288c-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="e288c-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="e288c-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="e288c-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="e288c-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="e288c-132">**Error**</span></span> <br/> | <span data-ttu-id="e288c-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e288c-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="e288c-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="e288c-134">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="e288c-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="e288c-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="e288c-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="e288c-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="e288c-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="e288c-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="e288c-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e288c-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="e288c-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="e288c-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="e288c-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="e288c-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="e288c-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="e288c-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e288c-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e288c-142">Child elements</span></span>

|<span data-ttu-id="e288c-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="e288c-143">**Element**</span></span>|<span data-ttu-id="e288c-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e288c-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e288c-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="e288c-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="e288c-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e288c-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="e288c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e288c-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="e288c-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="e288c-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="e288c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e288c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="e288c-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e288c-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="e288c-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="e288c-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="e288c-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="e288c-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="e288c-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="e288c-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e288c-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e288c-154">Parent elements</span></span>

|<span data-ttu-id="e288c-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="e288c-155">**Element**</span></span>|<span data-ttu-id="e288c-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e288c-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e288c-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e288c-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="e288c-158">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e288c-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e288c-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="e288c-159">Text value</span></span>

<span data-ttu-id="e288c-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="e288c-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e288c-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e288c-161">Remarks</span></span>

<span data-ttu-id="e288c-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e288c-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e288c-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e288c-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e288c-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="e288c-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e288c-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e288c-165">Schema Name</span></span>  <br/> |<span data-ttu-id="e288c-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e288c-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e288c-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e288c-167">Validation File</span></span>  <br/> |<span data-ttu-id="e288c-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e288c-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e288c-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e288c-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="e288c-170">False</span><span class="sxs-lookup"><span data-stu-id="e288c-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e288c-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e288c-171">See also</span></span>

- [<span data-ttu-id="e288c-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e288c-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

