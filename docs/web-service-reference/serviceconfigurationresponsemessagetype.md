---
title: ServiceConfigurationResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServiceConfigurationResponseMessageType
api_type:
- schema
ms.assetid: ccfb0578-c648-44c2-ac4d-7620d881363e
description: Das ServiceConfigurationResponseMessageType-Element enthält Webdienst-Konfigurationseinstellungen.
ms.openlocfilehash: fb7841f346083017319cece4479fea8bbfb6de17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831393"
---
# <a name="serviceconfigurationresponsemessagetype"></a><span data-ttu-id="1aa6a-103">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="1aa6a-103">ServiceConfigurationResponseMessageType</span></span>

<span data-ttu-id="1aa6a-104">Das **ServiceConfigurationResponseMessageType** -Element enthält Webdienst-Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-104">The **ServiceConfigurationResponseMessageType** element contains service configuration settings.</span></span> 
  
```XML
<ServiceConfigurationResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTipsConfiguration/>
   <UnifiedMessagingConfiguration/>
   <ProtectionRulesConfiguration/>
</ServiceConfigurationResponseMessageType>
```

 <span data-ttu-id="1aa6a-105">**ServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-105">**ServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aa6a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1aa6a-106">Attributes and elements</span></span>

<span data-ttu-id="1aa6a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aa6a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1aa6a-108">Attributes</span></span>

|<span data-ttu-id="1aa6a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-109">**Attribute**</span></span>|<span data-ttu-id="1aa6a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1aa6a-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1aa6a-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="1aa6a-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1aa6a-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="1aa6a-114">-Success</span><span class="sxs-lookup"><span data-stu-id="1aa6a-114">-  Success</span></span>  <br/><span data-ttu-id="1aa6a-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1aa6a-115">-  Warning</span></span>  <br/><span data-ttu-id="1aa6a-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="1aa6a-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1aa6a-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1aa6a-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1aa6a-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-118">**Value**</span></span>|<span data-ttu-id="1aa6a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1aa6a-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-120">**Success**</span></span> <br/> |<span data-ttu-id="1aa6a-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1aa6a-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-122">**Warning**</span></span> <br/> | <span data-ttu-id="1aa6a-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1aa6a-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="1aa6a-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="1aa6a-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1aa6a-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1aa6a-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1aa6a-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1aa6a-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1aa6a-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1aa6a-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1aa6a-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-132">**Error**</span></span> <br/> | <span data-ttu-id="1aa6a-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1aa6a-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="1aa6a-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1aa6a-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1aa6a-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1aa6a-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="1aa6a-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="1aa6a-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="1aa6a-138">-Ein Attribut oder ein Element ist nicht gültig in den Kontext</span><span class="sxs-lookup"><span data-stu-id="1aa6a-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="1aa6a-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="1aa6a-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1aa6a-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1aa6a-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1aa6a-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1aa6a-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1aa6a-142">Child elements</span></span>

|<span data-ttu-id="1aa6a-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-143">**Element**</span></span>|<span data-ttu-id="1aa6a-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa6a-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1aa6a-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1aa6a-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1aa6a-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1aa6a-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1aa6a-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1aa6a-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1aa6a-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1aa6a-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1aa6a-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="1aa6a-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="1aa6a-155">Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-155">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-156">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa6a-156">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="1aa6a-157">Service-Konfigurationsinformationen für die Unified Messaging-Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-157">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
|[<span data-ttu-id="1aa6a-158">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa6a-158">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="1aa6a-159">Enthält Konfigurationsinformationen für den Schutz Regeln Dienst Service.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-159">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1aa6a-160">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1aa6a-160">Parent elements</span></span>

|<span data-ttu-id="1aa6a-161">**Element**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-161">**Element**</span></span>|<span data-ttu-id="1aa6a-162">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1aa6a-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa6a-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="1aa6a-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="1aa6a-164">Enthält ein Array von Service Configuration Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-164">Contains an array of service configuration response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1aa6a-165">Textwert</span><span class="sxs-lookup"><span data-stu-id="1aa6a-165">Text value</span></span>

<span data-ttu-id="1aa6a-166">Keine.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1aa6a-167">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1aa6a-167">Remarks</span></span>

<span data-ttu-id="1aa6a-168">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1aa6a-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aa6a-169">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1aa6a-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aa6a-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="1aa6a-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1aa6a-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1aa6a-171">Schema Name</span></span>  <br/> |<span data-ttu-id="1aa6a-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1aa6a-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1aa6a-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1aa6a-173">Validation File</span></span>  <br/> |<span data-ttu-id="1aa6a-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1aa6a-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1aa6a-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1aa6a-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="1aa6a-176">False</span><span class="sxs-lookup"><span data-stu-id="1aa6a-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1aa6a-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aa6a-177">See also</span></span>

- [<span data-ttu-id="1aa6a-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1aa6a-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

