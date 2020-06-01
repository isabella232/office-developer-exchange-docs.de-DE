---
title: GetPhoneCallInformationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformationResponse
api_type:
- schema
ms.assetid: 17f79875-46ec-4289-b974-b3c35af429cd
description: Das GetPhoneCallInformationResponse-Element definiert eine Antwort auf eine einzelne GetPhoneCallInformation-Anforderung.
ms.openlocfilehash: 5bc060504ea734ec2d7e01707ef6bbdb0aa665d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457886"
---
# <a name="getphonecallinformationresponse"></a><span data-ttu-id="1904d-103">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="1904d-103">GetPhoneCallInformationResponse</span></span>

<span data-ttu-id="1904d-104">Das **GetPhoneCallInformationResponse** -Element definiert eine Antwort auf eine einzelne GetPhoneCallInformation-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1904d-104">The **GetPhoneCallInformationResponse** element defines a response to a single GetPhoneCallInformation request.</span></span> 
  
```xml
<GetPhoneCallInformationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <PhoneCallInformation/>
</GetPhoneCallInformationResponse>
```

 <span data-ttu-id="1904d-105">**GetPhoneCallInformationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1904d-105">**GetPhoneCallInformationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1904d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1904d-106">Attributes and elements</span></span>

<span data-ttu-id="1904d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1904d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1904d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1904d-108">Attributes</span></span>

|<span data-ttu-id="1904d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1904d-109">**Attribute**</span></span>|<span data-ttu-id="1904d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1904d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1904d-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1904d-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1904d-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1904d-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="1904d-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1904d-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="1904d-114">-Success</span><span class="sxs-lookup"><span data-stu-id="1904d-114">-  Success</span></span>  <br/><span data-ttu-id="1904d-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1904d-115">-  Warning</span></span>  <br/><span data-ttu-id="1904d-116">-Error</span><span class="sxs-lookup"><span data-stu-id="1904d-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1904d-117">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="1904d-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="1904d-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1904d-118">**Value**</span></span>|<span data-ttu-id="1904d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1904d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1904d-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="1904d-120">**Success**</span></span> <br/> |<span data-ttu-id="1904d-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1904d-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1904d-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1904d-122">**Warning**</span></span> <br/> | <span data-ttu-id="1904d-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1904d-123">Describes a request that was not processed.</span></span> <span data-ttu-id="1904d-124">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1904d-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="1904d-125">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="1904d-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="1904d-126">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="1904d-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1904d-127">-Der Active Directory Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="1904d-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="1904d-128">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="1904d-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1904d-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1904d-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1904d-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1904d-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="1904d-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1904d-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1904d-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="1904d-132">**Error**</span></span> <br/> | <span data-ttu-id="1904d-133">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1904d-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1904d-134">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="1904d-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1904d-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1904d-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1904d-136">-Attribute oder Elemente außerhalb des Bereichs</span><span class="sxs-lookup"><span data-stu-id="1904d-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="1904d-137">-Unbekanntes Tag</span><span class="sxs-lookup"><span data-stu-id="1904d-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="1904d-138">-Attribut oder Element im Kontext ungültig</span><span class="sxs-lookup"><span data-stu-id="1904d-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="1904d-139">-Nicht autorisierter Zugriff durch einen Client</span><span class="sxs-lookup"><span data-stu-id="1904d-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1904d-140">-Server seitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1904d-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1904d-141">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="1904d-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1904d-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1904d-142">Child elements</span></span>

|<span data-ttu-id="1904d-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="1904d-143">**Element**</span></span>|<span data-ttu-id="1904d-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1904d-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1904d-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="1904d-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1904d-146">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1904d-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1904d-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1904d-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1904d-148">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1904d-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1904d-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1904d-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1904d-150">Wird derzeit nicht verwendet und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1904d-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="1904d-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="1904d-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1904d-152">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="1904d-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1904d-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1904d-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="1904d-154">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="1904d-154">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="1904d-155">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="1904d-155">Specifies the state information for a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1904d-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1904d-156">Parent elements</span></span>

<span data-ttu-id="1904d-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="1904d-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1904d-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1904d-158">Remarks</span></span>

<span data-ttu-id="1904d-159">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1904d-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1904d-160">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1904d-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1904d-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="1904d-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1904d-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1904d-162">Schema Name</span></span>  <br/> |<span data-ttu-id="1904d-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1904d-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1904d-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1904d-164">Validation File</span></span>  <br/> |<span data-ttu-id="1904d-165">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1904d-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1904d-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1904d-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="1904d-167">False</span><span class="sxs-lookup"><span data-stu-id="1904d-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1904d-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1904d-168">See also</span></span>

- [<span data-ttu-id="1904d-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1904d-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

