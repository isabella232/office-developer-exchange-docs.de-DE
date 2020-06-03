---
title: RemoveContactFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Hier finden Sie Informationen zum RemoveContactFromImList-EWS-Vorgang.
ms.openlocfilehash: 8b3d83a0b53bad169d9f3478540e5087901f3a12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458467"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="5c324-103">RemoveContactFromImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5c324-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="5c324-104">Hier finden Sie Informationen zum **RemoveContactFromImList** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5c324-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="5c324-105">Der **RemoveContactFromImList** -Vorgang entfernt Kontakte aus der lync-Chat-Liste (Instant Messaging), wenn lync Exchange für den Kontaktspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c324-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="5c324-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5c324-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="5c324-107">Verwenden des RemoveContactFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5c324-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="5c324-108">Der **RemoveContactFromImList** -Vorgang akzeptiert ein einzelnes Argument, das einen Kontakt identifiziert, der aus der auf einem Exchange-Server gespeicherten lync-Kontaktliste entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c324-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="5c324-109">Die Liste der Kontakte, die dieser Vorgang als Ziel hat, wird in Outlook 2013 als **lync-Kontakte** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5c324-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="5c324-110">Verwenden Sie nicht den [DeleteItem-Vorgang](deleteitem-operation.md) , um Kontakte aus einer Kontaktliste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5c324-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="5c324-111">Möglicherweise muss eine weitere serverseitige Verarbeitung durchgeführt werden, um das Entfernen eines Kontakts aus der **lync-Kontakt** Liste zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c324-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="5c324-112">Beachten Sie, dass die **lync-Kontakt** Liste die konzeptionelle Entsprechung des Standardordners für **lync-Kontakte** ist.</span><span class="sxs-lookup"><span data-stu-id="5c324-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="5c324-113">SOAP-Header des RemoveContactFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5c324-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="5c324-114">Der **RemoveContactFromImList** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5c324-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="5c324-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="5c324-115">**Header name**</span></span>|<span data-ttu-id="5c324-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c324-116">**Element**</span></span>|<span data-ttu-id="5c324-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c324-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c324-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="5c324-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="5c324-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="5c324-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="5c324-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="5c324-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="5c324-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5c324-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5c324-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="5c324-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="5c324-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="5c324-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="5c324-124">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c324-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="5c324-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5c324-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5c324-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="5c324-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="5c324-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5c324-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5c324-128">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="5c324-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="5c324-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5c324-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5c324-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="5c324-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="5c324-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5c324-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5c324-132">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="5c324-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="5c324-133">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="5c324-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="5c324-134">RemoveContactFromImList-Vorgangs Anforderungs Beispiel: Entfernen eines Kontakts aus der lync-Kontaktliste</span><span class="sxs-lookup"><span data-stu-id="5c324-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="5c324-135">Im folgenden Beispiel einer **RemoveContactFromImList** -Vorgangsanforderung wird gezeigt, wie ein Kontakt aus der **lync-Kontakt** Liste entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5c324-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="5c324-136">Der **RemoveContactFromImList** -Vorgang akzeptiert eine einzelne eindeutige Kontakt-ID, um den Kontakt zu identifizieren, der aus der **lync-Kontakt** Liste entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c324-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5c324-137">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c324-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="5c324-138">Die folgenden Elemente werden im SOAP-Anforderungstext Körper verwendet:</span><span class="sxs-lookup"><span data-stu-id="5c324-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="5c324-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="5c324-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="5c324-140">ContactId</span><span class="sxs-lookup"><span data-stu-id="5c324-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="5c324-141">Erfolgreiche Reaktion des RemoveContactFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5c324-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="5c324-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveContactFromImList** -Vorgangsanforderung, um einen Kontakt aus der **lync-Kontakt** Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5c324-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="5c324-143">Die folgenden Elemente werden im SOAP-Antworttext Körper verwendet:</span><span class="sxs-lookup"><span data-stu-id="5c324-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="5c324-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="5c324-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="5c324-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5c324-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="5c324-146">Fehlerantwort des RemoveContactFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5c324-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="5c324-147">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RemoveContactFromImList** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="5c324-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="5c324-148">Dies ist eine Antwort auf eine Anforderung zum Entfernen eines Kontakts aus der **lync** -Kontaktliste, wenn der Kontakt nicht mehr in der Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5c324-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="5c324-149">Die folgenden Elemente werden im SOAP-Textkörper der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="5c324-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="5c324-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="5c324-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="5c324-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="5c324-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5c324-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5c324-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5c324-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5c324-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5c324-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c324-154">See also</span></span>

- [<span data-ttu-id="5c324-155">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="5c324-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="5c324-156">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5c324-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

