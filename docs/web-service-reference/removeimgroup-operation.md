---
title: RemoveImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e788016-68e0-4a3f-9243-03f6b6c6b389
description: Hier finden Sie Informationen über die RemoveImGroup EWS Vorgang.
ms.openlocfilehash: 85b312f0b156125a2d5395658ccea06d831abdde
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831097"
---
# <a name="removeimgroup-operation"></a><span data-ttu-id="16f98-103">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16f98-103">RemoveImGroup operation</span></span>

<span data-ttu-id="16f98-104">Hier finden Sie Informationen zum **RemoveImGroup** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="16f98-104">Find information about the **RemoveImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="16f98-105">Der Vorgang **RemoveImGroup** entfernt eine einzelne instant messaging (IM) Gruppe aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="16f98-105">The **RemoveImGroup** operation removes a single instant messaging (IM) group from a mailbox.</span></span> 
  
<span data-ttu-id="16f98-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="16f98-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimgroup-operation"></a><span data-ttu-id="16f98-107">Verwenden des RemoveImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="16f98-107">Using the RemoveImGroup operation</span></span>

<span data-ttu-id="16f98-108">Die **RemoveImGroup** Operation hat nur eine einzige Gruppe Identifier-Argument.</span><span class="sxs-lookup"><span data-stu-id="16f98-108">The **RemoveImGroup** operation only takes a single group identifier argument.</span></span> 
  
### <a name="removeimgroup-operation-soap-headers"></a><span data-ttu-id="16f98-109">RemoveImGroup Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="16f98-109">RemoveImGroup operation SOAP headers</span></span>

<span data-ttu-id="16f98-110">Der Vorgang **RemoveImGroup** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="16f98-110">The **RemoveImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="16f98-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="16f98-111">**Header name**</span></span>|<span data-ttu-id="16f98-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="16f98-112">**Element**</span></span>|<span data-ttu-id="16f98-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16f98-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16f98-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="16f98-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="16f98-115">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="16f98-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="16f98-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="16f98-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="16f98-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16f98-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16f98-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="16f98-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="16f98-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="16f98-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="16f98-120">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16f98-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="16f98-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16f98-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16f98-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="16f98-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="16f98-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="16f98-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="16f98-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="16f98-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="16f98-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16f98-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16f98-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="16f98-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="16f98-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="16f98-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="16f98-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="16f98-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="16f98-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="16f98-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimgroup-operation-request-example"></a><span data-ttu-id="16f98-130">RemoveImGroup Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="16f98-130">RemoveImGroup operation request example</span></span>

<span data-ttu-id="16f98-131">Im folgenden Beispiel wird eine **RemoveImGroup** Vorgang Anforderung veranschaulicht eine Instant Messaging-Gruppe zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="16f98-131">The following example of a **RemoveImGroup** operation request shows how to remove an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16f98-132">Die Gruppen-ID wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16f98-132">The group ID has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5hQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="16f98-133">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16f98-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16f98-134">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="16f98-134">RemoveImGroup</span></span>](removeimgroup.md)
    
- [<span data-ttu-id="16f98-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="16f98-135">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimgroup-operation-response"></a><span data-ttu-id="16f98-136">Erfolgreiche RemoveImGroup Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="16f98-136">Successful RemoveImGroup operation response</span></span>

<span data-ttu-id="16f98-137">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveImGroup** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="16f98-137">The following example shows a successful response to a **RemoveImGroup** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Success" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="16f98-138">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16f98-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16f98-139">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="16f98-139">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="16f98-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16f98-140">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimgroup-operation-errorinvalidimgroupid-error-response"></a><span data-ttu-id="16f98-141">RemoveImGroup Vorgang ErrorInvalidImGroupId Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="16f98-141">RemoveImGroup operation ErrorInvalidImGroupId error response</span></span>

<span data-ttu-id="16f98-142">Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveImGroup** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16f98-142">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="16f98-143">Die folgende Fehlerantwort tritt auf, wenn versucht wird, eine Gruppe zu entfernen, die im Postfach nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="16f98-143">The following error response occurs when an attempt is made to remove a group that does not exist in the mailbox.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Group Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImGroupId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="16f98-144">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16f98-144">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16f98-145">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="16f98-145">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="16f98-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="16f98-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="16f98-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16f98-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="16f98-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="16f98-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="16f98-149">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="16f98-149">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="removeimgroup-operation-errorinvalididmalformed-error-response"></a><span data-ttu-id="16f98-150">RemoveImGroup Vorgang ErrorInvalidIdMalformed Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="16f98-150">RemoveImGroup operation ErrorInvalidIdMalformed error response</span></span>

<span data-ttu-id="16f98-151">Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveImGroup** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16f98-151">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="16f98-152">Die folgende Fehlerantwort tritt auf, wenn versucht wird, eine Gruppe mit einem Gruppenbezeichner falsch formatierte zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="16f98-152">The following error response occurs when an attempt is made to remove a group with an incorrectly formatted group identifier.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="16f98-153">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16f98-153">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16f98-154">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="16f98-154">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="16f98-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="16f98-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="16f98-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16f98-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="16f98-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="16f98-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="16f98-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f98-158">See also</span></span>

- [<span data-ttu-id="16f98-159">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="16f98-159">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="16f98-160">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16f98-160">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="16f98-161">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16f98-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    

