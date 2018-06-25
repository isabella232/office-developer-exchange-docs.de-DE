---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: Das GetPasswordExpirationDateResponse-Element definiert die Antwort auf eine GetPasswordExpirationDate Vorgang Vorgang an.
ms.openlocfilehash: 3754a53da53c12479f11c2e32cd15a08cba665fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758772"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="86866-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="86866-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="86866-104">Das **GetPasswordExpirationDateResponse** -Element definiert die Antwort auf eine [GetPasswordExpirationDate Vorgang](getpasswordexpirationdate-operation.md) Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="86866-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="86866-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86866-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="86866-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="86866-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="86866-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="86866-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86866-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-108">Attributes and elements</span></span>

<span data-ttu-id="86866-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="86866-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86866-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="86866-110">Attributes</span></span>

|<span data-ttu-id="86866-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="86866-111">**Attribute**</span></span>|<span data-ttu-id="86866-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86866-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86866-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="86866-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="86866-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="86866-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="86866-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="86866-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="86866-116">-Success</span><span class="sxs-lookup"><span data-stu-id="86866-116">-  Success</span></span>  <br/><span data-ttu-id="86866-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="86866-117">-  Warning</span></span>  <br/><span data-ttu-id="86866-118">-Fehler</span><span class="sxs-lookup"><span data-stu-id="86866-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="86866-119">Attributwerte ResponseClass</span><span class="sxs-lookup"><span data-stu-id="86866-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="86866-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="86866-120">**Value**</span></span>|<span data-ttu-id="86866-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86866-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86866-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="86866-122">**Success**</span></span> <br/> |<span data-ttu-id="86866-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="86866-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="86866-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="86866-124">**Warning**</span></span> <br/> | <span data-ttu-id="86866-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="86866-125">Describes a request that was not processed.</span></span> <span data-ttu-id="86866-126">Eine Warnung kann zurückgegeben werden, wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet hat, und die nachfolgenden Elemente nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="86866-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="86866-127">Es folgen Beispiele für die Quellen der Warnungen:</span><span class="sxs-lookup"><span data-stu-id="86866-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="86866-128">-Der Exchange-Speicher ist während der Batchaktualisierung offline.</span><span class="sxs-lookup"><span data-stu-id="86866-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="86866-129">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="86866-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="86866-130">-Postfächern verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="86866-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="86866-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="86866-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="86866-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="86866-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="86866-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="86866-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="86866-134">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="86866-134">**Error**</span></span> <br/> | <span data-ttu-id="86866-135">Beschreibt eine Anforderung, die nicht gewährleistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="86866-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="86866-136">Es folgen Beispiele für Datenquellen von Fehlern:</span><span class="sxs-lookup"><span data-stu-id="86866-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="86866-137">-Ungültige Attribute oder Elemente.</span><span class="sxs-lookup"><span data-stu-id="86866-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="86866-138">-Attribute oder Elemente, die sich außerhalb des gültigen Bereichs befinden.</span><span class="sxs-lookup"><span data-stu-id="86866-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="86866-139">-Eine unbekannte Marke.</span><span class="sxs-lookup"><span data-stu-id="86866-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="86866-140">-Ein Attribut oder ein Element, das nicht im Kontext gültig ist.</span><span class="sxs-lookup"><span data-stu-id="86866-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="86866-141">-Eine Versuch nicht autorisierten Zugriff von jedem Client.</span><span class="sxs-lookup"><span data-stu-id="86866-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="86866-142">-Eine serverseitige Fehler als Reaktion auf einen gültigen mithilfe der clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="86866-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="86866-143">Informationen zu dem Fehler kann in den Elementen [ResponseCode](responsecode.md) und [MessageText](messagetext.md) gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="86866-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86866-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-144">Child elements</span></span>

|<span data-ttu-id="86866-145">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="86866-145">**Element name**</span></span>|<span data-ttu-id="86866-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86866-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86866-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="86866-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="86866-148">Stellt das Ablaufdatum Kennwort für das e-Mail-Konto in der Anforderung angegeben.</span><span class="sxs-lookup"><span data-stu-id="86866-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86866-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86866-149">Parent elements</span></span>

|<span data-ttu-id="86866-150">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="86866-150">**Element name**</span></span>|<span data-ttu-id="86866-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86866-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86866-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="86866-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="86866-153">Enthält die Antwortnachrichten für eine Exchange-Webdienste (EWS)-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="86866-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86866-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86866-154">Remarks</span></span>

<span data-ttu-id="86866-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="86866-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="86866-156">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="86866-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86866-157">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="86866-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86866-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="86866-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86866-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="86866-159">Schema Name</span></span>  <br/> |<span data-ttu-id="86866-160">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="86866-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86866-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="86866-161">Validation File</span></span>  <br/> |<span data-ttu-id="86866-162">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86866-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86866-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="86866-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="86866-164">False</span><span class="sxs-lookup"><span data-stu-id="86866-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86866-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86866-165">See also</span></span>

- [<span data-ttu-id="86866-166">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="86866-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="86866-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="86866-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

