---
title: SetImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d48aa07-8152-4c3d-a519-061253e80174
description: Hier finden Sie Informationen zum SetImGroup-EWS-Vorgang.
ms.openlocfilehash: 37b290559fff0b2de57669741547ba4b1b56c28c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44438075"
---
# <a name="setimgroup-operation"></a><span data-ttu-id="f262c-103">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f262c-103">SetImGroup operation</span></span>

<span data-ttu-id="f262c-104">Hier finden Sie Informationen zum **SetImGroup** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f262c-104">Find information about the **SetImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="f262c-105">Der **SetImGroup** -Vorgang ändert den Anzeigenamen einer Chatgruppe (Instant Messaging).</span><span class="sxs-lookup"><span data-stu-id="f262c-105">The **SetImGroup** operation changes the display name of an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="f262c-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f262c-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setimgroup-operation"></a><span data-ttu-id="f262c-107">Verwenden des SetImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f262c-107">Using the SetImGroup operation</span></span>

<span data-ttu-id="f262c-108">Für den **SetImGroup** -Vorgang wird nur ein einzelnes Anzeigename-Argument verwendet.</span><span class="sxs-lookup"><span data-stu-id="f262c-108">The **SetImGroup** operation only takes a single display name argument.</span></span> 
  
### <a name="setimgroup-operation-soap-headers"></a><span data-ttu-id="f262c-109">SOAP-Header des SetImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f262c-109">SetImGroup operation SOAP headers</span></span>

<span data-ttu-id="f262c-110">Der **SetImGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f262c-110">The **SetImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f262c-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="f262c-111">**Header name**</span></span>|<span data-ttu-id="f262c-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f262c-112">**Element**</span></span>|<span data-ttu-id="f262c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f262c-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f262c-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="f262c-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f262c-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f262c-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f262c-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="f262c-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f262c-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f262c-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f262c-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f262c-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f262c-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f262c-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f262c-120">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f262c-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f262c-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f262c-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f262c-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f262c-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f262c-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f262c-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f262c-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f262c-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f262c-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f262c-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f262c-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f262c-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f262c-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f262c-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f262c-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f262c-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f262c-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f262c-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setimgroup-operation-request-example"></a><span data-ttu-id="f262c-130">SetImGroup-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="f262c-130">SetImGroup operation request example</span></span>

<span data-ttu-id="f262c-131">Im folgenden Beispiel einer **SetImGroup** -Vorgangsanforderung wird gezeigt, wie ein Anzeigename einer Chatgruppe in "MyNewGroupName" geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f262c-131">The following example of a **SetImGroup** operation request shows how to change an IM group display name to "MyNewGroupName".</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f262c-132">Die Exchange-Informationsspeicher-ID wurde verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f262c-132">The Exchange store identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:SetImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
         <m:NewDisplayName>MyNewGroupName</m:NewDisplayName>
      </m:SetImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f262c-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f262c-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f262c-134">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="f262c-134">SetImGroup</span></span>](setimgroup.md)
    
- [<span data-ttu-id="f262c-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="f262c-135">GroupId</span></span>](groupid.md)
    
- [<span data-ttu-id="f262c-136">Neuanzeigename</span><span class="sxs-lookup"><span data-stu-id="f262c-136">NewDisplayName</span></span>](newdisplayname.md)
    
## <a name="successful-setimgroup-operation-response"></a><span data-ttu-id="f262c-137">Erfolgreiche Reaktion des SetImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f262c-137">Successful SetImGroup operation response</span></span>

<span data-ttu-id="f262c-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SetImGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="f262c-138">The following example shows a successful response to a **SetImGroup** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetImGroupResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         </SetImGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="f262c-139">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f262c-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f262c-140">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f262c-140">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="f262c-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f262c-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="setimgroup-operation-error-response"></a><span data-ttu-id="f262c-142">Fehlerantwort des SetImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f262c-142">SetImGroup operation error response</span></span>

<span data-ttu-id="f262c-143">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SetImGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="f262c-143">The following example shows an error response to a **SetImGroup** operation request.</span></span> <span data-ttu-id="f262c-144">Die folgende Fehlermeldung tritt auf, wenn versucht wird, den Anzeigenamen der Gruppe in den vorhandenen Gruppen Anzeigenamen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f262c-144">The following error response occurs when an attempt is made to change the group display name to the existing group display name.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15"
                           MinorVersion="0"
                           MajorBuildNumber="349"
                           MinorBuildNumber="0"
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <SetImGroupResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>An IM group with the specified display name already exists.</MessageText>
         <ResponseCode>ErrorImGroupDisplayNameAlreadyExists</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f262c-145">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f262c-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f262c-146">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f262c-146">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="f262c-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="f262c-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f262c-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f262c-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f262c-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f262c-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f262c-150">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f262c-150">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f262c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f262c-151">See also</span></span>

- [<span data-ttu-id="f262c-152">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f262c-152">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="f262c-153">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f262c-153">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="f262c-154">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f262c-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    

