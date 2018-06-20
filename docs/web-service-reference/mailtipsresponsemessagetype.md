---
title: MailTipsResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: Das MailTipsResponseMessageType-Element darstellt, e-Mail-Tipps-Einstellungen.
ms.openlocfilehash: 76a1e33ae189b96a96a41d1bc7a8f79116761c4f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830334"
---
# <a name="mailtipsresponsemessagetype"></a><span data-ttu-id="3f946-103">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="3f946-103">MailTipsResponseMessageType</span></span>

<span data-ttu-id="3f946-104">Das **MailTipsResponseMessageType** -Element darstellt, e-Mail-Tipps-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="3f946-104">The **MailTipsResponseMessageType** element represents mail tips settings.</span></span> 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 <span data-ttu-id="3f946-105">**MailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3f946-105">**MailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f946-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3f946-106">Attributes and elements</span></span>

<span data-ttu-id="3f946-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3f946-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f946-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f946-108">Attributes</span></span>

|<span data-ttu-id="3f946-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3f946-109">**Attribute**</span></span>|<span data-ttu-id="3f946-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f946-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f946-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="3f946-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="3f946-112">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="3f946-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="3f946-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="3f946-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="3f946-114">-Success</span><span class="sxs-lookup"><span data-stu-id="3f946-114">-  Success</span></span>  <br/><span data-ttu-id="3f946-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="3f946-115">-  Warning</span></span>  <br/><span data-ttu-id="3f946-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="3f946-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="3f946-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3f946-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="3f946-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3f946-118">**Value**</span></span>|<span data-ttu-id="3f946-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f946-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f946-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="3f946-120">**Success**</span></span> <br/> |<span data-ttu-id="3f946-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3f946-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="3f946-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="3f946-122">**Warning**</span></span> <br/> | <span data-ttu-id="3f946-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="3f946-123">Describes a request that was not processed.</span></span> <span data-ttu-id="3f946-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3f946-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="3f946-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="3f946-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="3f946-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="3f946-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="3f946-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="3f946-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="3f946-128">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f946-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="3f946-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="3f946-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="3f946-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="3f946-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="3f946-131">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="3f946-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="3f946-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="3f946-132">**Error**</span></span> <br/> | <span data-ttu-id="3f946-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f946-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="3f946-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="3f946-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="3f946-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="3f946-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="3f946-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="3f946-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="3f946-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="3f946-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="3f946-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="3f946-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="3f946-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="3f946-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="3f946-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="3f946-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="3f946-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="3f946-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f946-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f946-142">Child elements</span></span>

|<span data-ttu-id="3f946-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f946-143">**Element**</span></span>|<span data-ttu-id="3f946-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f946-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f946-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="3f946-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3f946-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="3f946-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3f946-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3f946-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3f946-148">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="3f946-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="3f946-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3f946-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3f946-150">Derzeit nicht verwendet wird und für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3f946-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="3f946-151">Dieses Element enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="3f946-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="3f946-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3f946-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3f946-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="3f946-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3f946-154">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="3f946-154">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="3f946-155">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="3f946-155">Represents values for various types of mail tips.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f946-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f946-156">Parent elements</span></span>

|<span data-ttu-id="3f946-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f946-157">**Element**</span></span>|<span data-ttu-id="3f946-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3f946-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f946-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="3f946-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="3f946-160">Stellt eine Liste der e-Mail-Tipps Antwortnachrichten dar.</span><span class="sxs-lookup"><span data-stu-id="3f946-160">Represents a list of mail tips response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3f946-161">Textwert</span><span class="sxs-lookup"><span data-stu-id="3f946-161">Text value</span></span>

<span data-ttu-id="3f946-162">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f946-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f946-163">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f946-163">Remarks</span></span>

<span data-ttu-id="3f946-164">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3f946-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f946-165">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3f946-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f946-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f946-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f946-167">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3f946-167">Schema Name</span></span>  <br/> |<span data-ttu-id="3f946-168">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3f946-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f946-169">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3f946-169">Validation File</span></span>  <br/> |<span data-ttu-id="3f946-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3f946-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f946-171">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3f946-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f946-172">False</span><span class="sxs-lookup"><span data-stu-id="3f946-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f946-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f946-173">See also</span></span>

- [<span data-ttu-id="3f946-174">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3f946-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

