---
title: GetServiceConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfigurationResponse
api_type:
- schema
ms.assetid: 313dac99-0e5c-4198-bafa-89e749934ac7
description: Das GetServiceConfigurationResponse-Element definiert eine Antwort auf eine GetServiceConfiguration an.
ms.openlocfilehash: 7abc81222125334de2a6ab6e4a618b48fe0caf4f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829668"
---
# <a name="getserviceconfigurationresponse"></a><span data-ttu-id="7a6e1-103">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="7a6e1-103">GetServiceConfigurationResponse</span></span>

<span data-ttu-id="7a6e1-104">Das **GetServiceConfigurationResponse** -Element definiert eine Antwort auf eine GetServiceConfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-104">The **GetServiceConfigurationResponse** element defines a response to a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfigurationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ResponseMessages/>
</GetServiceConfigurationResponse>
```

 <span data-ttu-id="7a6e1-105">**GetServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-105">**GetServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a6e1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6e1-106">Attributes and elements</span></span>

<span data-ttu-id="7a6e1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a6e1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a6e1-108">Attributes</span></span>

|<span data-ttu-id="7a6e1-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-109">**Attribute**</span></span>|<span data-ttu-id="7a6e1-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a6e1-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="7a6e1-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="7a6e1-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="7a6e1-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="7a6e1-114">-Success</span><span class="sxs-lookup"><span data-stu-id="7a6e1-114">-  Success</span></span>  <br/><span data-ttu-id="7a6e1-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="7a6e1-115">-  Warning</span></span>  <br/><span data-ttu-id="7a6e1-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="7a6e1-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="7a6e1-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="7a6e1-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="7a6e1-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-118">**Value**</span></span>|<span data-ttu-id="7a6e1-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a6e1-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-120">**Success**</span></span> <br/> |<span data-ttu-id="7a6e1-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="7a6e1-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-122">**Warning**</span></span> <br/> | <span data-ttu-id="7a6e1-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-123">Describes a request that was not processed.</span></span> <span data-ttu-id="7a6e1-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="7a6e1-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="7a6e1-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="7a6e1-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="7a6e1-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="7a6e1-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="7a6e1-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="7a6e1-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="7a6e1-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="7a6e1-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-132">**Error**</span></span> <br/> | <span data-ttu-id="7a6e1-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="7a6e1-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="7a6e1-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="7a6e1-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6e1-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="7a6e1-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="7a6e1-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="7a6e1-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="7a6e1-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="7a6e1-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="7a6e1-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="7a6e1-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="7a6e1-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="7a6e1-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7a6e1-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6e1-142">Child elements</span></span>

|<span data-ttu-id="7a6e1-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-143">**Element**</span></span>|<span data-ttu-id="7a6e1-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a6e1-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a6e1-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="7a6e1-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="7a6e1-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="7a6e1-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7a6e1-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="7a6e1-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="7a6e1-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7a6e1-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="7a6e1-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="7a6e1-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="7a6e1-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7a6e1-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="7a6e1-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="7a6e1-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="7a6e1-154">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="7a6e1-155">Enthält ein Array von Service Configuration Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-155">Contains an array of service configuration response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a6e1-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a6e1-156">Parent elements</span></span>

<span data-ttu-id="7a6e1-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7a6e1-158">Textwert</span><span class="sxs-lookup"><span data-stu-id="7a6e1-158">Text value</span></span>

<span data-ttu-id="7a6e1-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a6e1-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a6e1-160">Remarks</span></span>

<span data-ttu-id="7a6e1-161">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a6e1-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a6e1-162">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7a6e1-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a6e1-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a6e1-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a6e1-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a6e1-164">Schema Name</span></span>  <br/> |<span data-ttu-id="7a6e1-165">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7a6e1-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a6e1-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a6e1-166">Validation File</span></span>  <br/> |<span data-ttu-id="7a6e1-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7a6e1-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a6e1-168">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a6e1-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a6e1-169">False</span><span class="sxs-lookup"><span data-stu-id="7a6e1-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a6e1-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a6e1-170">See also</span></span>

- [<span data-ttu-id="7a6e1-171">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a6e1-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

