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
description: Das GetPhoneCallInformationResponse-Element definiert eine Antwort auf eine einzelne Anforderung GetPhoneCallInformation.
ms.openlocfilehash: 5a03d63198cd00997b8975b18a5ae0eb5fca1af2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758779"
---
# <a name="getphonecallinformationresponse"></a><span data-ttu-id="9d5a2-103">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="9d5a2-103">GetPhoneCallInformationResponse</span></span>

<span data-ttu-id="9d5a2-104">Das **GetPhoneCallInformationResponse** -Element definiert eine Antwort auf eine einzelne Anforderung GetPhoneCallInformation.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-104">The **GetPhoneCallInformationResponse** element defines a response to a single GetPhoneCallInformation request.</span></span> 
  
```xml
<GetPhoneCallInformationResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>   <PhoneCallInformation/>
</GetPhoneCallInformationResponse>
```

 <span data-ttu-id="9d5a2-105">**GetPhoneCallInformationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-105">**GetPhoneCallInformationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d5a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5a2-106">Attributes and elements</span></span>

<span data-ttu-id="9d5a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d5a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d5a2-108">Attributes</span></span>

|<span data-ttu-id="9d5a2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-109">**Attribute**</span></span>|<span data-ttu-id="9d5a2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d5a2-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9d5a2-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="9d5a2-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="9d5a2-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="9d5a2-114">-Success</span><span class="sxs-lookup"><span data-stu-id="9d5a2-114">-  Success</span></span>  <br/><span data-ttu-id="9d5a2-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="9d5a2-115">-  Warning</span></span>  <br/><span data-ttu-id="9d5a2-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="9d5a2-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="9d5a2-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="9d5a2-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="9d5a2-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-118">**Value**</span></span>|<span data-ttu-id="9d5a2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d5a2-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-120">**Success**</span></span> <br/> |<span data-ttu-id="9d5a2-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9d5a2-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-122">**Warning**</span></span> <br/> | <span data-ttu-id="9d5a2-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9d5a2-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="9d5a2-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="9d5a2-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="9d5a2-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9d5a2-127">– Der Active Directory-Verzeichnisdienst ist offline.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-127">-  The Active Directory directory service is offline.</span></span>  <br/><span data-ttu-id="9d5a2-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="9d5a2-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9d5a2-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="9d5a2-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="9d5a2-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-132">**Error**</span></span> <br/> | <span data-ttu-id="9d5a2-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9d5a2-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="9d5a2-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9d5a2-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5a2-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9d5a2-136">-Attribute oder Elemente außerhalb des gültigen Bereichs</span><span class="sxs-lookup"><span data-stu-id="9d5a2-136">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="9d5a2-137">-Unbekanntes tag</span><span class="sxs-lookup"><span data-stu-id="9d5a2-137">-  Unknown tag</span></span>  <br/><span data-ttu-id="9d5a2-138">-Attribut oder ein Element im Kontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-138">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="9d5a2-139">-Versuch von jedem Client Zugriff</span><span class="sxs-lookup"><span data-stu-id="9d5a2-139">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9d5a2-140">-Server-Side-Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="9d5a2-140">-  Server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9d5a2-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d5a2-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5a2-142">Child elements</span></span>

|<span data-ttu-id="9d5a2-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-143">**Element**</span></span>|<span data-ttu-id="9d5a2-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d5a2-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d5a2-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9d5a2-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9d5a2-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9d5a2-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9d5a2-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9d5a2-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="9d5a2-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9d5a2-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9d5a2-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="9d5a2-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9d5a2-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9d5a2-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9d5a2-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9d5a2-154">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="9d5a2-154">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="9d5a2-155">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-155">Specifies the state information for a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d5a2-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d5a2-156">Parent elements</span></span>

<span data-ttu-id="9d5a2-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d5a2-158">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d5a2-158">Remarks</span></span>

<span data-ttu-id="9d5a2-159">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d5a2-159">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d5a2-160">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d5a2-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d5a2-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d5a2-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d5a2-162">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d5a2-162">Schema Name</span></span>  <br/> |<span data-ttu-id="9d5a2-163">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9d5a2-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d5a2-164">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d5a2-164">Validation File</span></span>  <br/> |<span data-ttu-id="9d5a2-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d5a2-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d5a2-166">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d5a2-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d5a2-167">False</span><span class="sxs-lookup"><span data-stu-id="9d5a2-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d5a2-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d5a2-168">See also</span></span>

- [<span data-ttu-id="9d5a2-169">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9d5a2-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

