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
description: Das ServiceConfigurationResponseMessageType-Element enthält Dienst Konfigurationseinstellungen.
ms.openlocfilehash: 4c84a49b2403343a1defd00696858489497d6214
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44439105"
---
# <a name="serviceconfigurationresponsemessagetype"></a><span data-ttu-id="880f9-103">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="880f9-103">ServiceConfigurationResponseMessageType</span></span>

<span data-ttu-id="880f9-104">Das **ServiceConfigurationResponseMessageType** -Element enthält Dienst Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="880f9-104">The **ServiceConfigurationResponseMessageType** element contains service configuration settings.</span></span> 
  
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

 <span data-ttu-id="880f9-105">**ServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="880f9-105">**ServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="880f9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="880f9-106">Attributes and elements</span></span>

<span data-ttu-id="880f9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="880f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="880f9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="880f9-108">Attributes</span></span>

|<span data-ttu-id="880f9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="880f9-109">**Attribute**</span></span>|<span data-ttu-id="880f9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="880f9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="880f9-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="880f9-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="880f9-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="880f9-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="880f9-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="880f9-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="880f9-114">-Success</span><span class="sxs-lookup"><span data-stu-id="880f9-114">-  Success</span></span>  <br/><span data-ttu-id="880f9-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="880f9-115">-  Warning</span></span>  <br/><span data-ttu-id="880f9-116">-Error</span><span class="sxs-lookup"><span data-stu-id="880f9-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="880f9-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="880f9-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="880f9-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="880f9-118">**Value**</span></span>|<span data-ttu-id="880f9-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="880f9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="880f9-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="880f9-120">**Success**</span></span> <br/> |<span data-ttu-id="880f9-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="880f9-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="880f9-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="880f9-122">**Warning**</span></span> <br/> | <span data-ttu-id="880f9-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="880f9-123">Describes a request that was not processed.</span></span> <span data-ttu-id="880f9-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="880f9-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="880f9-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="880f9-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="880f9-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="880f9-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="880f9-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="880f9-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="880f9-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="880f9-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="880f9-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="880f9-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="880f9-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="880f9-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="880f9-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="880f9-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="880f9-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="880f9-132">**Error**</span></span> <br/> | <span data-ttu-id="880f9-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="880f9-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="880f9-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="880f9-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="880f9-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="880f9-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="880f9-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="880f9-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="880f9-137">-Ein unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="880f9-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="880f9-138">-Ein Attribut oder Element ist im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="880f9-138">-  An attribute or element is not valid in the context</span></span>  <br/><span data-ttu-id="880f9-139">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client</span><span class="sxs-lookup"><span data-stu-id="880f9-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="880f9-140">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="880f9-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="880f9-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="880f9-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="880f9-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="880f9-142">Child elements</span></span>

|<span data-ttu-id="880f9-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="880f9-143">**Element**</span></span>|<span data-ttu-id="880f9-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="880f9-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="880f9-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="880f9-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="880f9-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="880f9-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="880f9-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="880f9-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="880f9-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="880f9-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="880f9-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="880f9-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="880f9-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="880f9-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="880f9-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="880f9-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="880f9-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="880f9-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="880f9-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="880f9-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="880f9-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="880f9-154">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="880f9-155">Enthält Dienstkonfigurationsinformationen für den e-Mail-Spitzen Dienst.</span><span class="sxs-lookup"><span data-stu-id="880f9-155">Contains service configuration information for the mail tips service.</span></span>  <br/> |
|[<span data-ttu-id="880f9-156">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="880f9-156">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="880f9-157">Enthält Dienstkonfigurationsinformationen für den Unified Messaging-Dienst.</span><span class="sxs-lookup"><span data-stu-id="880f9-157">Contains service configuration information for the Unified Messaging service.</span></span>  <br/> |
|[<span data-ttu-id="880f9-158">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="880f9-158">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="880f9-159">Enthält Dienstkonfigurationsinformationen für den Schutz Regeldienst.</span><span class="sxs-lookup"><span data-stu-id="880f9-159">Contains service configuration information for the protection rules service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="880f9-160">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="880f9-160">Parent elements</span></span>

|<span data-ttu-id="880f9-161">**Element**</span><span class="sxs-lookup"><span data-stu-id="880f9-161">**Element**</span></span>|<span data-ttu-id="880f9-162">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="880f9-162">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="880f9-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="880f9-163">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>](responsemessages-arrayofserviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="880f9-164">Enthält ein Array von Dienst Konfigurations Antwortmeldungen.</span><span class="sxs-lookup"><span data-stu-id="880f9-164">Contains an array of service configuration response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="880f9-165">Textwert</span><span class="sxs-lookup"><span data-stu-id="880f9-165">Text value</span></span>

<span data-ttu-id="880f9-166">Keine.</span><span class="sxs-lookup"><span data-stu-id="880f9-166">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="880f9-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="880f9-167">Remarks</span></span>

<span data-ttu-id="880f9-168">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="880f9-168">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="880f9-169">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="880f9-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="880f9-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="880f9-170">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="880f9-171">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="880f9-171">Schema Name</span></span>  <br/> |<span data-ttu-id="880f9-172">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="880f9-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="880f9-173">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="880f9-173">Validation File</span></span>  <br/> |<span data-ttu-id="880f9-174">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="880f9-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="880f9-175">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="880f9-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="880f9-176">False</span><span class="sxs-lookup"><span data-stu-id="880f9-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="880f9-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="880f9-177">See also</span></span>

- [<span data-ttu-id="880f9-178">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="880f9-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

