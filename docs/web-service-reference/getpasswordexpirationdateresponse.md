---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: Das GetPasswordExpirationDateResponse-Element definiert die Antwort auf eine Anforderung des GetPasswordExpirationDate-Vorgangs Vorgangs.
ms.openlocfilehash: c925b2b37879ba0f8f25b2dd73737ed2f3202555
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530204"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="d3363-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="d3363-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="d3363-104">Das **GetPasswordExpirationDateResponse** -Element definiert die Antwort auf eine Anforderung des [GetPasswordExpirationDate-Vorgangs](getpasswordexpirationdate-operation.md) Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="d3363-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="d3363-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3363-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="d3363-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="d3363-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="d3363-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d3363-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3363-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3363-108">Attributes and elements</span></span>

<span data-ttu-id="d3363-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3363-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3363-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3363-110">Attributes</span></span>

|<span data-ttu-id="d3363-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d3363-111">**Attribute**</span></span>|<span data-ttu-id="d3363-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3363-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3363-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="d3363-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="d3363-114">Beschreibt den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d3363-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="d3363-115">Die folgenden Werte sind für dieses Attribut gültig:</span><span class="sxs-lookup"><span data-stu-id="d3363-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="d3363-116">-Success</span><span class="sxs-lookup"><span data-stu-id="d3363-116">-  Success</span></span>  <br/><span data-ttu-id="d3363-117">-Warnung</span><span class="sxs-lookup"><span data-stu-id="d3363-117">-  Warning</span></span>  <br/><span data-ttu-id="d3363-118">-Error</span><span class="sxs-lookup"><span data-stu-id="d3363-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="d3363-119">ResponseClass-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="d3363-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="d3363-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d3363-120">**Value**</span></span>|<span data-ttu-id="d3363-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3363-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3363-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="d3363-122">**Success**</span></span> <br/> |<span data-ttu-id="d3363-123">Beschreibt eine Anforderung, die erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d3363-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="d3363-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="d3363-124">**Warning**</span></span> <br/> | <span data-ttu-id="d3363-125">Beschreibt eine Anforderung, die nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d3363-125">Describes a request that was not processed.</span></span> <span data-ttu-id="d3363-126">Wenn ein Fehler aufgetreten ist, während ein Element in der Anforderung verarbeitet wurde, kann eine Warnung zurückgegeben werden, und nachfolgende Elemente konnten nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d3363-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="d3363-127">Im folgenden sind Beispiele für Quellen von Warnungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d3363-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="d3363-128">-Der Exchange-Informationsspeicher ist während des Batches offline.</span><span class="sxs-lookup"><span data-stu-id="d3363-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="d3363-129">-Active Directory-Domänendienste (AD DS) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d3363-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="d3363-130">-Postfächer wurden verschoben.</span><span class="sxs-lookup"><span data-stu-id="d3363-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="d3363-131">-Die Nachrichtendatenbank (MDB) ist offline.</span><span class="sxs-lookup"><span data-stu-id="d3363-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="d3363-132">-Ein Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="d3363-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="d3363-133">-Ein Kontingent wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="d3363-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="d3363-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="d3363-134">**Error**</span></span> <br/> | <span data-ttu-id="d3363-135">Beschreibt eine Anforderung, die nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3363-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="d3363-136">Im folgenden finden Sie Beispiele für Fehlerquellen:</span><span class="sxs-lookup"><span data-stu-id="d3363-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="d3363-137">-Ungültige Attribute oder Elemente.</span><span class="sxs-lookup"><span data-stu-id="d3363-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="d3363-138">-Attribute oder Elemente außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="d3363-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="d3363-139">-Ein unbekanntes Tag.</span><span class="sxs-lookup"><span data-stu-id="d3363-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="d3363-140">-Ein Attribut oder Element, das im Kontext nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d3363-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="d3363-141">-Ein nicht autorisierter Zugriff versucht von einem beliebigen Client.</span><span class="sxs-lookup"><span data-stu-id="d3363-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="d3363-142">-Ein serverseitiger Fehler als Reaktion auf einen gültigen clientseitigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="d3363-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="d3363-143">Informationen zum Fehler finden Sie in den Elementen [Response Code](responsecode.md) und [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="d3363-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d3363-144">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3363-144">Child elements</span></span>

|<span data-ttu-id="d3363-145">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="d3363-145">**Element name**</span></span>|<span data-ttu-id="d3363-146">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3363-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3363-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="d3363-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="d3363-148">Gibt das Ablaufdatum für das Kennwort für das in der Anforderung angegebene e-Mail-Konto an.</span><span class="sxs-lookup"><span data-stu-id="d3363-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3363-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3363-149">Parent elements</span></span>

|<span data-ttu-id="d3363-150">**Elementname**</span><span class="sxs-lookup"><span data-stu-id="d3363-150">**Element name**</span></span>|<span data-ttu-id="d3363-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3363-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3363-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d3363-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d3363-153">Enthält die Antwortnachrichten für eine Exchange-Webdienste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d3363-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3363-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3363-154">Remarks</span></span>

<span data-ttu-id="d3363-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d3363-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d3363-156">Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d3363-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3363-157">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d3363-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3363-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3363-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d3363-159">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3363-159">Schema Name</span></span>  <br/> |<span data-ttu-id="d3363-160">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d3363-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d3363-161">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3363-161">Validation File</span></span>  <br/> |<span data-ttu-id="d3363-162">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d3363-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3363-163">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3363-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3363-164">False</span><span class="sxs-lookup"><span data-stu-id="d3363-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3363-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3363-165">See also</span></span>

- [<span data-ttu-id="d3363-166">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d3363-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="d3363-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3363-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

