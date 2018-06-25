---
title: FindConversationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversationResponse
api_type:
- schema
ms.assetid: a689e29d-5f3d-4deb-81ee-8b6cc60f6dea
description: Das FindConversationResponse-Element definiert eine Antwort auf eine FindConversation Vorgang an.
ms.openlocfilehash: 5754ea7540fa6daac8cd725386ca213d5bf05c8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758441"
---
# <a name="findconversationresponse"></a><span data-ttu-id="1597b-103">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="1597b-103">FindConversationResponse</span></span>

<span data-ttu-id="1597b-104">Das **FindConversationResponse** -Element definiert eine Antwort auf eine [FindConversation Vorgang](findconversation-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="1597b-104">The **FindConversationResponse** element defines a response to a [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
[<span data-ttu-id="1597b-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="1597b-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
```XML
<FindConversationResponse ResponseClass="">
   <Conversations/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</FindConversationResponse>

```

 <span data-ttu-id="1597b-106">**FindConversationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1597b-106">**FindConversationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1597b-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1597b-107">Attributes and elements</span></span>

<span data-ttu-id="1597b-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1597b-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1597b-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="1597b-109">Attributes</span></span>

|<span data-ttu-id="1597b-110">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1597b-110">**Attribute**</span></span>|<span data-ttu-id="1597b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1597b-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1597b-112">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="1597b-112">**ResponseClass**</span></span> <br/> | <span data-ttu-id="1597b-113">Beschreibt den Status einer Antwort [FindConversation Vorgang](findconversation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1597b-113">Describes the status of a [FindConversation operation](findconversation-operation.md) response.</span></span> <br/><br/><span data-ttu-id="1597b-114">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="1597b-114">The following values are valid for this attribute:</span></span><br/>  <br/><span data-ttu-id="1597b-115">-Success</span><span class="sxs-lookup"><span data-stu-id="1597b-115">-  Success</span></span>  <br/><span data-ttu-id="1597b-116">-Warnung</span><span class="sxs-lookup"><span data-stu-id="1597b-116">-  Warning</span></span>  <br/><span data-ttu-id="1597b-117">-Fehler</span><span class="sxs-lookup"><span data-stu-id="1597b-117">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="1597b-118">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="1597b-118">ResponseClass attribute values</span></span>

|<span data-ttu-id="1597b-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1597b-119">**Value**</span></span>|<span data-ttu-id="1597b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1597b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1597b-121">**Success**</span><span class="sxs-lookup"><span data-stu-id="1597b-121">**Success**</span></span> <br/> |<span data-ttu-id="1597b-122">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="1597b-122">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="1597b-123">**Warning**</span><span class="sxs-lookup"><span data-stu-id="1597b-123">**Warning**</span></span> <br/> | <span data-ttu-id="1597b-124">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1597b-124">Describes a request that was not processed.</span></span> <span data-ttu-id="1597b-125">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1597b-125">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="1597b-126">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="1597b-126">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="1597b-127">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="1597b-127">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="1597b-128">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1597b-128">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="1597b-129">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="1597b-129">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="1597b-130">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="1597b-130">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="1597b-131">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="1597b-131">-  A password is expired.</span></span>  <br/><span data-ttu-id="1597b-132">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="1597b-132">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="1597b-133">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="1597b-133">**Error**</span></span> <br/> | <span data-ttu-id="1597b-134">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1597b-134">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="1597b-135">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="1597b-135">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="1597b-136">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="1597b-136">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="1597b-137">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="1597b-137">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="1597b-138">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="1597b-138">-  An unknown tag</span></span>  <br/><span data-ttu-id="1597b-139">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="1597b-139">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="1597b-140">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="1597b-140">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="1597b-141">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="1597b-141">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="1597b-142">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1597b-142">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1597b-143">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1597b-143">Child elements</span></span>

|<span data-ttu-id="1597b-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="1597b-144">**Element**</span></span>|<span data-ttu-id="1597b-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1597b-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1597b-146">Conversations</span><span class="sxs-lookup"><span data-stu-id="1597b-146">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1597b-147">Enthält ein Array von Unterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="1597b-147">Contains an array of conversations.</span></span>  <br/> |
|[<span data-ttu-id="1597b-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="1597b-148">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="1597b-149">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="1597b-149">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="1597b-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1597b-150">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="1597b-151">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="1597b-151">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="1597b-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1597b-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="1597b-153">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="1597b-153">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="1597b-154">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="1597b-154">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="1597b-155">MessageXml</span><span class="sxs-lookup"><span data-stu-id="1597b-155">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="1597b-156">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="1597b-156">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1597b-157">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1597b-157">Parent elements</span></span>

<span data-ttu-id="1597b-158">Keine.</span><span class="sxs-lookup"><span data-stu-id="1597b-158">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1597b-159">Textwert</span><span class="sxs-lookup"><span data-stu-id="1597b-159">Text value</span></span>

<span data-ttu-id="1597b-160">Keine.</span><span class="sxs-lookup"><span data-stu-id="1597b-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1597b-161">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1597b-161">Remarks</span></span>

<span data-ttu-id="1597b-162">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1597b-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1597b-163">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1597b-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1597b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="1597b-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1597b-165">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1597b-165">Schema name</span></span>  <br/> |<span data-ttu-id="1597b-166">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1597b-166">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1597b-167">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1597b-167">Validation file</span></span>  <br/> |<span data-ttu-id="1597b-168">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1597b-168">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1597b-169">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1597b-169">Can be empty</span></span>  <br/> |<span data-ttu-id="1597b-170">False</span><span class="sxs-lookup"><span data-stu-id="1597b-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1597b-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1597b-171">See also</span></span>

- [<span data-ttu-id="1597b-172">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="1597b-172">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="1597b-173">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1597b-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="1597b-174">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="1597b-174">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

