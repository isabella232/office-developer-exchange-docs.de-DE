---
title: AddImContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: Hier finden Sie Informationen zum AddImContactToGroup-EWS-Vorgang.
ms.openlocfilehash: a69ee0b355e78e1249383cab612a75bcda8d9e8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458411"
---
# <a name="addimcontacttogroup-operation"></a><span data-ttu-id="1563e-103">AddImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-103">AddImContactToGroup operation</span></span>

<span data-ttu-id="1563e-104">Hier finden Sie Informationen zum **AddImContactToGroup** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1563e-104">Find information about the **AddImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="1563e-105">Mit dem **AddImContactToGroup** -Exchange-Webdienste Vorgang wird einer Gruppe ein vorhandener Chat Kontakt (Instant Messaging) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1563e-105">The **AddImContactToGroup** Exchange Web Services (EWS) operation adds an existing instant messaging (IM) contact to a group.</span></span> 
  
<span data-ttu-id="1563e-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1563e-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimcontacttogroup-operation"></a><span data-ttu-id="1563e-107">Verwenden des AddImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="1563e-107">Using the AddImContactToGroup operation</span></span>

<span data-ttu-id="1563e-108">Der **AddImContactToGroup** -Vorgang kann nur Chatkontakte akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="1563e-108">The **AddImContactToGroup** operation can only accept IM contacts.</span></span> <span data-ttu-id="1563e-109">Wenn Sie einen neuen Chat Kontakt zum einheitlichen Kontaktspeicher hinzufügen möchten, verwenden Sie den [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1563e-109">If you want to add a new IM contact to the Unified Contact Store, use the [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) operation.</span></span> 
  
<span data-ttu-id="1563e-110">Der **AddImContactToGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1563e-110">The **AddImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="1563e-111">**Tabelle 1. SOAP-Header des AddImContactToGroup-Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="1563e-111">**Table 1. AddImContactToGroup operation SOAP headers**</span></span>

|<span data-ttu-id="1563e-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="1563e-112">**Header name**</span></span>|<span data-ttu-id="1563e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1563e-113">**Element**</span></span>|<span data-ttu-id="1563e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1563e-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1563e-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="1563e-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="1563e-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="1563e-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="1563e-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="1563e-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="1563e-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1563e-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1563e-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="1563e-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="1563e-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="1563e-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="1563e-121">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1563e-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="1563e-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1563e-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1563e-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="1563e-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="1563e-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="1563e-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="1563e-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="1563e-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="1563e-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1563e-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1563e-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="1563e-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="1563e-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1563e-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="1563e-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="1563e-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="1563e-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="1563e-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a><span data-ttu-id="1563e-131">AddImContactToGroup-Vorgangs Anforderungs Beispiel: Hinzufügen eines vorhandenen Chat Kontakts zu einer Chatgruppe</span><span class="sxs-lookup"><span data-stu-id="1563e-131">AddImContactToGroup operation request example: Add an existing IM contact to an IM group</span></span>

<span data-ttu-id="1563e-132">Im folgenden Beispiel einer **AddImContactToGroup** -Vorgangsanforderung wird das Hinzufügen eines vorhandenen sofortnachrichtenkontakts zu einer Chatgruppe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1563e-132">The following example of an **AddImContactToGroup** operation request shows how to add an existing IM contact an IM group.</span></span> 
  
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
      <m:AddImContactToGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTc4Y2AA="
                      ChangeKey="EQAAABYAAABtF8oI7i"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkzzAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="1563e-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="1563e-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="1563e-134">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1563e-134">AddImContactToGroup</span></span>](addimcontacttogroup.md)
    
- [<span data-ttu-id="1563e-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="1563e-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="1563e-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="1563e-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a><span data-ttu-id="1563e-137">Erfolgreiche Reaktion des AddImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="1563e-137">Successful AddImContactToGroup operation response</span></span>

<span data-ttu-id="1563e-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **AddImContactToGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="1563e-138">The following example shows a successful response to an **AddImContactToGroup** operation request.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Success" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </AddImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="1563e-139">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="1563e-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="1563e-140">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="1563e-140">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="1563e-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1563e-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="1563e-142">AddImContactToGroup-Vorgang ErrorInvalidImContactId-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="1563e-142">AddImContactToGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="1563e-143">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **AddImContactToGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="1563e-143">The following example shows an error response to an **AddImContactToGroup** operation request.</span></span> <span data-ttu-id="1563e-144">Die folgende Fehlermeldung tritt auf, wenn ein Versuch unternommen wird, einen Kontakt hinzuzufügen, der kein Chat Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="1563e-144">The following error response occurs when an attempt is made to add a contact that is not an IM contact.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Error" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         </AddImContactToGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="1563e-145">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="1563e-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="1563e-146">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="1563e-146">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="1563e-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="1563e-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="1563e-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1563e-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1563e-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1563e-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="1563e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1563e-150">See also</span></span>

- [<span data-ttu-id="1563e-151">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-151">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="1563e-152">AddNewImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-152">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="1563e-153">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-153">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="1563e-154">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="1563e-155">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1563e-155">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="1563e-156">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1563e-156">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

