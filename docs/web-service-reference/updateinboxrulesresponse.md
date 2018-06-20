---
title: UpdateInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRulesResponse
api_type:
- schema
ms.assetid: 0947b6aa-0d95-421b-aebb-d03021ecc110
description: Das UpdateInboxRulesResponse-Element definiert eine Antwort auf eine Anforderung UpdateInboxRules.
ms.openlocfilehash: cd64e4546f8d9bf573062d9c982477be3fa4d925
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839370"
---
# <a name="updateinboxrulesresponse"></a><span data-ttu-id="ffba2-103">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ffba2-103">UpdateInboxRulesResponse</span></span>

<span data-ttu-id="ffba2-104">Das **UpdateInboxRulesResponse** -Element definiert eine Antwort auf eine Anforderung UpdateInboxRules.</span><span class="sxs-lookup"><span data-stu-id="ffba2-104">The **UpdateInboxRulesResponse** element defines a response to an UpdateInboxRules request.</span></span> 
  
```XML
<UpdateInboxRulesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RuleOperationErrors/>
</UpdateInboxRulesResponse>
```

 <span data-ttu-id="ffba2-105">**UpdateInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="ffba2-105">**UpdateInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffba2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ffba2-106">Attributes and elements</span></span>

<span data-ttu-id="ffba2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ffba2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffba2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffba2-108">Attributes</span></span>

|<span data-ttu-id="ffba2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ffba2-109">**Attribute**</span></span>|<span data-ttu-id="ffba2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffba2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffba2-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ffba2-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ffba2-112">Beschreibt den Status einer Antwort auf einen [Vorgang zum Abmelden](unsubscribe-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ffba2-112">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span><br/><br/> <span data-ttu-id="ffba2-113">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="ffba2-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ffba2-114">-Success</span><span class="sxs-lookup"><span data-stu-id="ffba2-114">-  Success</span></span>  <br/><span data-ttu-id="ffba2-115">-Warnung</span><span class="sxs-lookup"><span data-stu-id="ffba2-115">-  Warning</span></span>  <br/><span data-ttu-id="ffba2-116">-Fehler</span><span class="sxs-lookup"><span data-stu-id="ffba2-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ffba2-117">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ffba2-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ffba2-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ffba2-118">**Value**</span></span>|<span data-ttu-id="ffba2-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffba2-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ffba2-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="ffba2-120">**Success**</span></span> <br/> |<span data-ttu-id="ffba2-121">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ffba2-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ffba2-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ffba2-122">**Warning**</span></span> <br/> | <span data-ttu-id="ffba2-123">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ffba2-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ffba2-124">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ffba2-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ffba2-125">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="ffba2-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ffba2-126">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="ffba2-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ffba2-127">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ffba2-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ffba2-128">-Postfächer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="ffba2-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ffba2-129">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="ffba2-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ffba2-130">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ffba2-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ffba2-131">-Ein Kontingent überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="ffba2-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ffba2-132">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="ffba2-132">**Error**</span></span> <br/> | <span data-ttu-id="ffba2-133">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffba2-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ffba2-134">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="ffba2-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ffba2-135">-Ungültige Attribute oder Elemente</span><span class="sxs-lookup"><span data-stu-id="ffba2-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ffba2-136">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="ffba2-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ffba2-137">-Eine unbekannte Marke</span><span class="sxs-lookup"><span data-stu-id="ffba2-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ffba2-138">-Eines Attributs oder Elements, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ffba2-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ffba2-139">-Einen nicht autorisierten Zugriffsversuch von jedem client</span><span class="sxs-lookup"><span data-stu-id="ffba2-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ffba2-140">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf</span><span class="sxs-lookup"><span data-stu-id="ffba2-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ffba2-141">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="ffba2-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ffba2-142">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffba2-142">Child elements</span></span>

|<span data-ttu-id="ffba2-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffba2-143">**Element**</span></span>|<span data-ttu-id="ffba2-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffba2-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffba2-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ffba2-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ffba2-146">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="ffba2-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ffba2-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ffba2-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ffba2-148">Enthält Statusinformationen über die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ffba2-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="ffba2-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ffba2-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ffba2-150">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="ffba2-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ffba2-151">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="ffba2-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ffba2-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ffba2-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ffba2-153">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="ffba2-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ffba2-154">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="ffba2-154">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="ffba2-155">Stellt ein Array der Regel Validierungsfehler auf jede Regel dar, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="ffba2-155">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffba2-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffba2-156">Parent elements</span></span>

<span data-ttu-id="ffba2-157">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffba2-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ffba2-158">Textwert</span><span class="sxs-lookup"><span data-stu-id="ffba2-158">Text value</span></span>

<span data-ttu-id="ffba2-159">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffba2-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffba2-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffba2-160">Remarks</span></span>

<span data-ttu-id="ffba2-161">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ffba2-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffba2-162">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ffba2-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffba2-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffba2-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ffba2-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ffba2-164">Schema name</span></span>  <br/> |<span data-ttu-id="ffba2-165">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ffba2-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ffba2-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ffba2-166">Validation file</span></span>  <br/> |<span data-ttu-id="ffba2-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ffba2-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ffba2-168">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ffba2-168">Can be empty</span></span>  <br/> |<span data-ttu-id="ffba2-169">False</span><span class="sxs-lookup"><span data-stu-id="ffba2-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffba2-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffba2-170">See also</span></span>

- [<span data-ttu-id="ffba2-171">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="ffba2-171">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="ffba2-172">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ffba2-172">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="ffba2-173">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ffba2-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

