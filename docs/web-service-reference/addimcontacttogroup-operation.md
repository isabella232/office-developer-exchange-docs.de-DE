---
title: AddImContactToGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: Hier finden Sie Informationen über die AddImContactToGroup EWS Vorgang.
ms.openlocfilehash: 669d798b6cabc1cab1fc057a3e18c565467440f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757220"
---
# <a name="addimcontacttogroup-operation"></a><span data-ttu-id="f3328-103">AddImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-103">AddImContactToGroup operation</span></span>

<span data-ttu-id="f3328-104">Hier finden Sie Informationen zum **AddImContactToGroup** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f3328-104">Find information about the **AddImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="f3328-105">Der Vorgang des **AddImContactToGroup** Exchange-Webdienste (EWS) hinzugefügt eine Gruppe einen vorhandenen Kontakt Sofortnachrichten (IM).</span><span class="sxs-lookup"><span data-stu-id="f3328-105">The **AddImContactToGroup** Exchange Web Services (EWS) operation adds an existing instant messaging (IM) contact to a group.</span></span> 
  
<span data-ttu-id="f3328-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f3328-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimcontacttogroup-operation"></a><span data-ttu-id="f3328-107">Verwenden des AddImContactToGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f3328-107">Using the AddImContactToGroup operation</span></span>

<span data-ttu-id="f3328-108">Der Vorgang **AddImContactToGroup** kann nur IM-Kontakten akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="f3328-108">The **AddImContactToGroup** operation can only accept IM contacts.</span></span> <span data-ttu-id="f3328-109">Wenn Sie einen neuen Kontakt Sofortnachrichten der einheitliche Kontaktspeicher hinzufügen möchten, verwenden Sie die [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) -Operation.</span><span class="sxs-lookup"><span data-stu-id="f3328-109">If you want to add a new IM contact to the Unified Contact Store, use the [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) operation.</span></span> 
  
<span data-ttu-id="f3328-110">Der Vorgang **AddImContactToGroup** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f3328-110">The **AddImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="f3328-111">**In Tabelle 1. AddImContactToGroup Vorgang SOAP-Header**</span><span class="sxs-lookup"><span data-stu-id="f3328-111">**Table 1. AddImContactToGroup operation SOAP headers**</span></span>

|<span data-ttu-id="f3328-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="f3328-112">**Header name**</span></span>|<span data-ttu-id="f3328-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3328-113">**Element**</span></span>|<span data-ttu-id="f3328-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3328-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3328-115">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="f3328-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f3328-116">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="f3328-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f3328-117">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="f3328-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f3328-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f3328-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3328-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f3328-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f3328-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f3328-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f3328-121">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3328-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f3328-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f3328-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3328-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f3328-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f3328-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f3328-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f3328-125">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f3328-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f3328-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f3328-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3328-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f3328-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f3328-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f3328-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f3328-129">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f3328-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f3328-130">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f3328-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a><span data-ttu-id="f3328-131">AddImContactToGroup Vorgang-anforderungsbeispiel: hinzufügen eine vorhandene Sofortnachricht wenden Sie sich an eine Gruppe von Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="f3328-131">AddImContactToGroup operation request example: Add an existing IM contact to an IM group</span></span>

<span data-ttu-id="f3328-132">Im folgenden Beispiel wird ein **AddImContactToGroup** Vorgang Anforderung veranschaulicht, wie einen vorhandenen Instant Messaging-Kontakt eine Instant Messaging-Gruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f3328-132">The following example of an **AddImContactToGroup** operation request shows how to add an existing IM contact an IM group.</span></span> 
  
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
      <m:AddImContactToGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTc4Y2AA="
                      ChangeKey="EQAAABYAAABtF8oI7i"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkzzAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f3328-133">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f3328-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3328-134">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="f3328-134">AddImContactToGroup</span></span>](addimcontacttogroup.md)
    
- [<span data-ttu-id="f3328-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="f3328-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="f3328-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="f3328-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a><span data-ttu-id="f3328-137">Erfolgreiche AddImContactToGroup Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="f3328-137">Successful AddImContactToGroup operation response</span></span>

<span data-ttu-id="f3328-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **AddImContactToGroup** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f3328-138">The following example shows a successful response to an **AddImContactToGroup** operation request.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Success" 
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </AddImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f3328-139">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f3328-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3328-140">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f3328-140">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="f3328-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3328-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="f3328-142">AddImContactToGroup Vorgang ErrorInvalidImContactId Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="f3328-142">AddImContactToGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="f3328-143">Das folgende Beispiel zeigt eine Fehlerantwort an eine **AddImContactToGroup** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f3328-143">The following example shows an error response to an **AddImContactToGroup** operation request.</span></span> <span data-ttu-id="f3328-144">Die folgende Fehlerantwort tritt auf, wenn versucht wird, einen Kontakt hinzuzufügen, der nicht auf einen Sofortnachrichten-Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="f3328-144">The following error response occurs when an attempt is made to add a contact that is not an IM contact.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Error" 
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         </AddImContactToGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="f3328-145">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f3328-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3328-146">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f3328-146">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="f3328-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="f3328-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f3328-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3328-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f3328-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f3328-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="f3328-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3328-150">See also</span></span>

- [<span data-ttu-id="f3328-151">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-151">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="f3328-152">AddNewImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-152">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="f3328-153">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-153">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="f3328-154">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="f3328-155">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f3328-155">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="f3328-156">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3328-156">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

