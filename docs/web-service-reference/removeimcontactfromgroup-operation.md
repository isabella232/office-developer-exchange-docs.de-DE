---
title: RemoveImContactFromGroup-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Hier finden Sie Informationen zum RemoveImContactFromGroup-EWS-Vorgang.
ms.openlocfilehash: 4750ef57794c3da540ac36baa8ef6ef093939ea1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466969"
---
# <a name="removeimcontactfromgroup-operation"></a><span data-ttu-id="37fd8-103">RemoveImContactFromGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-103">RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="37fd8-104">Hier finden Sie Informationen zum **RemoveImContactFromGroup** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37fd8-104">Find information about the **RemoveImContactFromGroup** EWS operation.</span></span> 
  
<span data-ttu-id="37fd8-105">Mit dem **RemoveImContactFromGroup** -Vorgang wird ein einzelner Chat Kontakt aus einer Chatgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="37fd8-105">The **RemoveImContactFromGroup** operation removes a single IM contact from an IM group.</span></span> 
  
<span data-ttu-id="37fd8-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="37fd8-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimcontactfromgroup-operation"></a><span data-ttu-id="37fd8-107">Verwenden des RemoveImContactFromGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="37fd8-107">Using the RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="37fd8-108">Für den **RemoveImContactFromGroup** -Vorgang werden zwei Argumente verwendet: eine Kontaktelement-ID und die entsprechende Sofortnachrichten Gruppe, aus der der Kontakt entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="37fd8-108">The **RemoveImContactFromGroup** operation takes two arguments: a contact item identifier, and the corresponding instant messaging (IM) group from which the contact is removed.</span></span> 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a><span data-ttu-id="37fd8-109">SOAP-Header des RemoveImContactFromGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="37fd8-109">RemoveImContactFromGroup operation SOAP headers</span></span>

<span data-ttu-id="37fd8-110">Der **RemoveImContactFromGroup** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="37fd8-110">The **RemoveImContactFromGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="37fd8-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="37fd8-111">**Header name**</span></span>|<span data-ttu-id="37fd8-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="37fd8-112">**Element**</span></span>|<span data-ttu-id="37fd8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37fd8-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37fd8-114">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="37fd8-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="37fd8-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="37fd8-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="37fd8-116">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="37fd8-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="37fd8-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="37fd8-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="37fd8-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="37fd8-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="37fd8-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="37fd8-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="37fd8-120">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37fd8-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="37fd8-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="37fd8-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="37fd8-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="37fd8-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="37fd8-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="37fd8-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="37fd8-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="37fd8-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="37fd8-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="37fd8-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="37fd8-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="37fd8-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="37fd8-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="37fd8-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="37fd8-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="37fd8-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="37fd8-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="37fd8-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a><span data-ttu-id="37fd8-130">RemoveImContactFromGroup-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="37fd8-130">RemoveImContactFromGroup operation request example</span></span>

<span data-ttu-id="37fd8-131">Im folgenden Beispiel einer **RemoveImContactFromGroup** -Vorgangsanforderung wird gezeigt, wie Sie einen sofortnachrichtenkontakt aus einer Chatgruppe entfernen.</span><span class="sxs-lookup"><span data-stu-id="37fd8-131">The following example of a **RemoveImContactFromGroup** operation request shows how to remove an IM contact from an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="37fd8-132">Die Gruppen-und Kontakt-IDs wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="37fd8-132">The group and contact identifiers have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37fd8-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="37fd8-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="37fd8-134">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="37fd8-134">RemoveImContactFromGroup</span></span>](removeimcontactfromgroup.md)
    
- [<span data-ttu-id="37fd8-135">ContactId</span><span class="sxs-lookup"><span data-stu-id="37fd8-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="37fd8-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="37fd8-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a><span data-ttu-id="37fd8-137">Erfolgreiche Reaktion des RemoveImContactFromGroup-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="37fd8-137">Successful RemoveImContactFromGroup operation response</span></span>

<span data-ttu-id="37fd8-138">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveImContactFromGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="37fd8-138">The following example shows a successful response to a **RemoveImContactFromGroup** operation request.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="37fd8-139">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="37fd8-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="37fd8-140">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="37fd8-140">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="37fd8-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="37fd8-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="37fd8-142">RemoveImContactFromGroup-Vorgang ErrorInvalidImContactId-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="37fd8-142">RemoveImContactFromGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="37fd8-143">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveImContactFromGroup** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="37fd8-143">The following example shows an error response to a **RemoveImContactFromGroup** operation request.</span></span> <span data-ttu-id="37fd8-144">Die folgende Fehlermeldung tritt auf, wenn ein Versuch unternommen wird, ein Kontaktelement zu entfernen, das in der Gruppe "Chat" nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37fd8-144">The following error response occurs when an attempt is made to remove a contact item that does not exist in the IM group.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="37fd8-145">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="37fd8-145">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="37fd8-146">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="37fd8-146">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="37fd8-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="37fd8-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="37fd8-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="37fd8-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="37fd8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="37fd8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="37fd8-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fd8-150">See also</span></span>

- [<span data-ttu-id="37fd8-151">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="37fd8-151">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="37fd8-152">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="37fd8-152">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="37fd8-153">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="37fd8-153">AddImContactToGroup</span></span>](addimcontacttogroup-operation.md)
    
- [<span data-ttu-id="37fd8-154">AddImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-154">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="37fd8-155">AddNewImContactToGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-155">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="37fd8-156">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="37fd8-157">GetImItems</span><span class="sxs-lookup"><span data-stu-id="37fd8-157">GetImItems</span></span>](getimitems-operation.md)
    
- [<span data-ttu-id="37fd8-158">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="37fd8-158">RemoveContactFromImList</span></span>](removecontactfromimlist-operation.md)
    
- [<span data-ttu-id="37fd8-159">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="37fd8-159">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist-operation.md)
    
- [<span data-ttu-id="37fd8-160">RemoveImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-160">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="37fd8-161">SetImGroup-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37fd8-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="37fd8-162">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="37fd8-162">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted-operation.md)
    

