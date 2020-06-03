---
title: AddImGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Hier finden Sie Informationen zum AddImGroup-EWS-Vorgang.
ms.openlocfilehash: 38ed12a741d46fe998dc0079ed13973ce9edf5ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462815"
---
# <a name="addimgroup-operation"></a><span data-ttu-id="d1168-103">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d1168-103">AddImGroup operation</span></span>

<span data-ttu-id="d1168-104">Hier finden Sie Informationen zum **AddImGroup** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d1168-104">Find information about the **AddImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="d1168-105">Mit dem **AddImGroup** -Exchange-Webdienste Vorgang wird einem Postfach eine neue Sofortnachrichten Gruppe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d1168-105">The **AddImGroup** Exchange Web Services (EWS) operation adds a new instant messaging (IM) group to a mailbox.</span></span> 
  
<span data-ttu-id="d1168-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d1168-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimgroup-operation"></a><span data-ttu-id="d1168-107">Verwenden des AddImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d1168-107">Using the AddImGroup operation</span></span>

<span data-ttu-id="d1168-108">Für den **AddImGroup** -Vorgang wird nur ein einzelnes Anzeigename-Argument verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1168-108">The **AddImGroup** operation only takes a single display name argument.</span></span> 
  
<span data-ttu-id="d1168-109">Dieser Vorgang gibt den Anzeigenamen, den Gruppentyp und Exchange-Informationsspeicher Bezeichner der neuen Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="d1168-109">This operation returns the display name, group type, and Exchange store identifier of the new group.</span></span>
  
<span data-ttu-id="d1168-110">Der **AddImGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d1168-110">The **AddImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="d1168-111">**Tabelle 1. SOAP-Header des AddImGroup-Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="d1168-111">**Table 1. AddImGroup operation SOAP headers**</span></span>

|<span data-ttu-id="d1168-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d1168-112">**Header name**</span></span>|<span data-ttu-id="d1168-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1168-113">**Element**</span></span>|<span data-ttu-id="d1168-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1168-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1168-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="d1168-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d1168-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d1168-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d1168-p101">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d1168-p101">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d1168-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d1168-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d1168-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d1168-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d1168-121">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1168-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d1168-122">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d1168-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d1168-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d1168-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d1168-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d1168-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d1168-p103">Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d1168-p103">Identifies the schema version for the operation request. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d1168-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d1168-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d1168-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d1168-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d1168-p104">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d1168-p104">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a><span data-ttu-id="d1168-131">AddImGroup-Vorgangs Anforderungs Beispiel: Erstellen einer neuen Chatgruppe</span><span class="sxs-lookup"><span data-stu-id="d1168-131">AddImGroup operation request example: Create a new IM group</span></span>

<span data-ttu-id="d1168-132">Im folgenden Beispiel einer **AddImGroup** -Vorgangsanforderung wird gezeigt, wie Sie eine Chatgruppe mit dem Namen mykundengroup erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1168-132">The following example of an **AddImGroup** operation request shows how to create an IM group named MyCustomerGroup.</span></span> 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d1168-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d1168-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d1168-134">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="d1168-134">AddImGroup</span></span>](addimgroup.md)
    
- [<span data-ttu-id="d1168-135">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d1168-135">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a><span data-ttu-id="d1168-136">Erfolgreiche Reaktion des AddImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d1168-136">Successful AddImGroup operation response</span></span>

<span data-ttu-id="d1168-137">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddImGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d1168-137">The following example shows a successful response to an **AddImGroup** operation request.</span></span> 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d1168-138">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d1168-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d1168-139">AddImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="d1168-139">AddImGroupResponse</span></span>](addimgroupresponse.md)
    
- [<span data-ttu-id="d1168-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d1168-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d1168-141">Imgroup</span><span class="sxs-lookup"><span data-stu-id="d1168-141">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="d1168-142">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d1168-142">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="d1168-143">GroupType</span><span class="sxs-lookup"><span data-stu-id="d1168-143">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="d1168-144">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="d1168-144">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a><span data-ttu-id="d1168-145">Fehlerantwort des AddImGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d1168-145">AddImGroup operation error response</span></span>

<span data-ttu-id="d1168-146">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddImGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d1168-146">The following example shows an error response to an **AddImGroup** operation request.</span></span> <span data-ttu-id="d1168-147">Dies ist eine Antwort auf eine Anforderung, die ein Zeichen enthält, das nicht in einem Anzeigenamen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1168-147">This is a response to a request that contains a character that cannot be used in a display name.</span></span> <span data-ttu-id="d1168-148">Beachten Sie, dass dies ein SOAP-Fehler und keine schemabasierte Fehlermeldung ist.</span><span class="sxs-lookup"><span data-stu-id="d1168-148">Note that this is a SOAP fault and not a schema-based error message.</span></span> <span data-ttu-id="d1168-149">Der in der Anforderung übermittelte Anzeigename lautet ~! @ # $% ^ &amp; , und der Fehler tritt auf dem &amp; Zeichen auf.</span><span class="sxs-lookup"><span data-stu-id="d1168-149">The display name submitted in the request is ~!@#$%^&amp;, and the error occurs on the &amp; character.</span></span> <span data-ttu-id="d1168-150">Das &amp; Zeichen ist in der elften und 33. Zeichen in der Anforderungsnutzlast aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d1168-150">The &amp; character occurred on the 11th line and 33rd character in the request payload.</span></span> <span data-ttu-id="d1168-151">Die Antwort wurde mit einem HTTP 500-Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1168-151">The response was returned with an HTTP 500 code.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d1168-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1168-152">See also</span></span>

- [<span data-ttu-id="d1168-153">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d1168-153">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="d1168-154">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d1168-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="d1168-155">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="d1168-155">SetImGroup</span></span>](setimgroup.md)
    

