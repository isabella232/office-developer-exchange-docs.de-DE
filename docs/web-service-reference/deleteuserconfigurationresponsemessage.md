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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757942"
---
# <a name="deleteuserconfigurationresponsemessage"></a><span data-ttu-id="73457-103">DeleteUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73457-103">DeleteUserConfigurationResponseMessage</span></span>

<span data-ttu-id="73457-104">Das **DeleteUserConfigurationResponseMessage** -Element enthält den Status und das Ergebnis einer **DeleteUserConfiguration** Anforderung.</span><span class="sxs-lookup"><span data-stu-id="73457-104">The **DeleteUserConfigurationResponseMessage** element contains the status and result of a single **DeleteUserConfiguration** request.</span></span> 
  
```xml
<DeleteUserConfigurationResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteUserConfigurationResponseMessage>
```

 <span data-ttu-id="73457-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="73457-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73457-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73457-106">Attributes and elements</span></span>

<span data-ttu-id="73457-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73457-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73457-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73457-108">Attributes</span></span>

|<span data-ttu-id="73457-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="73457-109">**Attribute**</span></span>|<span data-ttu-id="73457-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73457-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73457-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="73457-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="73457-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="73457-112">Describes the status of the response.</span></span><br/><br/><span data-ttu-id="73457-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="73457-113">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="73457-114">-Success</span><span class="sxs-lookup"><span data-stu-id="73457-114">-  Success</span></span>  <br/><span data-ttu-id="73457-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="73457-115">-  Warning</span></span>  <br/><span data-ttu-id="73457-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="73457-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="73457-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="73457-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="73457-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="73457-118">**Value**</span></span>|<span data-ttu-id="73457-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73457-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73457-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="73457-120">**Success**</span></span> <br/> |<span data-ttu-id="73457-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="73457-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="73457-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="73457-122">**Warning**</span></span> <br/> | <span data-ttu-id="73457-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="73457-123">Describes a request that was not processed.</span></span> <span data-ttu-id="73457-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="73457-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="73457-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="73457-125">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="73457-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="73457-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="73457-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="73457-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="73457-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="73457-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="73457-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="73457-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="73457-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="73457-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="73457-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="73457-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="73457-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="73457-132">**Error**</span></span> <br/> | <span data-ttu-id="73457-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="73457-133">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="73457-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="73457-134">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="73457-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="73457-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="73457-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="73457-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="73457-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="73457-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="73457-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="73457-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="73457-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="73457-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="73457-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="73457-140">-  A server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="73457-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="73457-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73457-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73457-142">Child elements</span></span>

|<span data-ttu-id="73457-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="73457-143">**Element**</span></span>|<span data-ttu-id="73457-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73457-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73457-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="73457-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="73457-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="73457-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="73457-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="73457-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="73457-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="73457-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="73457-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="73457-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="73457-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="73457-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="73457-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="73457-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="73457-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="73457-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="73457-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="73457-153">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73457-154">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73457-154">Parent elements</span></span>

|<span data-ttu-id="73457-155">**Element**</span><span class="sxs-lookup"><span data-stu-id="73457-155">**Element**</span></span>|<span data-ttu-id="73457-156">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73457-156">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73457-157">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="73457-157">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="73457-158">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="73457-158">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="73457-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="73457-159">Text value</span></span>

<span data-ttu-id="73457-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="73457-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73457-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73457-161">Remarks</span></span>

<span data-ttu-id="73457-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="73457-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73457-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="73457-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73457-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="73457-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="73457-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73457-165">Schema Name</span></span>  <br/> |<span data-ttu-id="73457-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="73457-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="73457-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73457-167">Validation File</span></span>  <br/> |<span data-ttu-id="73457-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="73457-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="73457-169">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="73457-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="73457-170">False</span><span class="sxs-lookup"><span data-stu-id="73457-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73457-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73457-171">See also</span></span>

- [<span data-ttu-id="73457-172">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="73457-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

