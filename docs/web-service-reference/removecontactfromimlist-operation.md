---
title: RemoveContactFromImList-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Hier finden Sie Informationen über die RemoveContactFromImList EWS Vorgang.
ms.openlocfilehash: 036b295a84e86ad74c467572cc52fdf6bbae5191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831080"
---
# <a name="removecontactfromimlist-operation"></a><span data-ttu-id="2c09a-103">RemoveContactFromImList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c09a-103">RemoveContactFromImList operation</span></span>

<span data-ttu-id="2c09a-104">Hier finden Sie Informationen zum **RemoveContactFromImList** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2c09a-104">Find information about the **RemoveContactFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="2c09a-105">Der Vorgang **RemoveContactFromImList** entfernt Kontakte aus der Liste für die Lync-Sofortnachrichten (IM), bei der Lync Exchange für den Kontaktspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c09a-105">The **RemoveContactFromImList** operation removes contacts from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="2c09a-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2c09a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removecontactfromimlist-operation"></a><span data-ttu-id="2c09a-107">Verwenden des RemoveContactFromImList-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2c09a-107">Using the RemoveContactFromImList operation</span></span>

<span data-ttu-id="2c09a-108">Der **RemoveContactFromImList** -Vorgang akzeptiert ein einzelnes Argument, das einen Kontakt aus der Lync-Kontaktliste auf einem Exchange-Server gespeicherten entfernen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2c09a-108">The **RemoveContactFromImList** operation accepts a single argument that identifies a contact to remove from the Lync contact list stored on an Exchange server.</span></span> <span data-ttu-id="2c09a-109">Die Liste der Kontakte, dass dieser Vorgang Ziele **Lync-Kontakte** in Outlook 2013 aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2c09a-109">The list of contacts that this operation targets is called **Lync Contacts** in Outlook 2013.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="2c09a-110">Verwenden Sie die [DeleteItem Vorgang](deleteitem-operation.md) nicht um Kontakte aus einer Kontaktliste entfernen.</span><span class="sxs-lookup"><span data-stu-id="2c09a-110">Do not use the [DeleteItem operation](deleteitem-operation.md) to remove contacts from a contact list.</span></span> <span data-ttu-id="2c09a-111">Zusätzliche serverseitige Verarbeitung möglicherweise zur Unterstützung der Entfernen eines Kontakts aus der Liste **Kontakte Lync** auftreten.</span><span class="sxs-lookup"><span data-stu-id="2c09a-111">Additional server-side processing might have to occur to support removing a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="2c09a-112">Beachten Sie, dass die **Lync** -Kontaktliste konzeptionelle Standardordner **Kontakte Lync** Postfach entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c09a-112">Note that the **Lync Contacts** list is the conceptual equivalent of the default **Lync Contacts** mailbox folder.</span></span> 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a><span data-ttu-id="2c09a-113">RemoveContactFromImList Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="2c09a-113">RemoveContactFromImList operation SOAP headers</span></span>

<span data-ttu-id="2c09a-114">Der Vorgang **RemoveContactFromImList** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2c09a-114">The **RemoveContactFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2c09a-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="2c09a-115">**Header name**</span></span>|<span data-ttu-id="2c09a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c09a-116">**Element**</span></span>|<span data-ttu-id="2c09a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c09a-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c09a-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="2c09a-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="2c09a-119">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="2c09a-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2c09a-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="2c09a-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="2c09a-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c09a-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2c09a-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="2c09a-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="2c09a-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2c09a-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2c09a-124">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c09a-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="2c09a-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c09a-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2c09a-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2c09a-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2c09a-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2c09a-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2c09a-128">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2c09a-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2c09a-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c09a-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2c09a-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2c09a-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2c09a-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2c09a-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2c09a-132">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="2c09a-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2c09a-133">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="2c09a-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a><span data-ttu-id="2c09a-134">RemoveContactFromImList Vorgang-anforderungsbeispiel: Entfernen eines Kontakts aus der Liste Lync-Kontakte</span><span class="sxs-lookup"><span data-stu-id="2c09a-134">RemoveContactFromImList operation request example: Remove a contact from the Lync Contacts list</span></span>

<span data-ttu-id="2c09a-135">Im folgenden Beispiel wird eine **RemoveContactFromImList** Vorgang Anforderung Entfernen eines Kontakts aus der Liste **Kontakte Lync** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2c09a-135">The following example of a **RemoveContactFromImList** operation request shows how to remove a contact from the **Lync Contacts** list.</span></span> <span data-ttu-id="2c09a-136">Der **RemoveContactFromImList** -Vorgang akzeptiert einen einzelnen Kontakten, eindeutigen Bezeichner, um den Kontakt zu ermitteln, der von der **Lync** -Kontaktliste entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2c09a-136">The **RemoveContactFromImList** operation accepts a single unique contact identifier to identify the contact that is removed from the **Lync Contacts** list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c09a-137">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2c09a-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

<span data-ttu-id="2c09a-138">Die folgenden Elemente werden in der Anforderung SOAP-Body verwendet:</span><span class="sxs-lookup"><span data-stu-id="2c09a-138">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="2c09a-139">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="2c09a-139">RemoveContactFromImList</span></span>](removecontactfromimlist.md)
    
- [<span data-ttu-id="2c09a-140">ContactId</span><span class="sxs-lookup"><span data-stu-id="2c09a-140">ContactId</span></span>](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a><span data-ttu-id="2c09a-141">Erfolgreiche RemoveContactFromImList Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="2c09a-141">Successful RemoveContactFromImList operation response</span></span>

<span data-ttu-id="2c09a-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RemoveContactFromImList** Vorgang Anforderung zum Entfernen eines Kontakts aus der **Lync** -Kontaktliste.</span><span class="sxs-lookup"><span data-stu-id="2c09a-142">The following example shows a successful response to a **RemoveContactFromImList** operation request to remove a contact from the **Lync Contacts** list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="2c09a-143">Die folgenden Elemente werden in der Antwort SOAP-Body verwendet:</span><span class="sxs-lookup"><span data-stu-id="2c09a-143">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="2c09a-144">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="2c09a-144">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="2c09a-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c09a-145">ResponseCode</span></span>](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a><span data-ttu-id="2c09a-146">RemoveContactFromImList Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="2c09a-146">RemoveContactFromImList operation error response</span></span>

<span data-ttu-id="2c09a-147">Das folgende Beispiel zeigt eine Fehlerantwort an eine **RemoveContactFromImList** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2c09a-147">The following example shows an error response to a **RemoveContactFromImList** operation request.</span></span> <span data-ttu-id="2c09a-148">Dies ist eine Antwort auf eine Anforderung an einen Kontakt aus der **Lync** -Kontaktliste entfernen, wenn der Kontakt nicht mehr in der Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2c09a-148">This is a response to a request to remove a contact from the **Lync Contacts** list when the contact no longer exists in the list.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2c09a-149">Die folgenden Elemente werden in die SOAP-Body-Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="2c09a-149">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="2c09a-150">RemoveContactFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="2c09a-150">RemoveContactFromImListResponse</span></span>](removecontactfromimlistresponse.md)
    
- [<span data-ttu-id="2c09a-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="2c09a-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2c09a-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c09a-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2c09a-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2c09a-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="2c09a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c09a-154">See also</span></span>

- [<span data-ttu-id="2c09a-155">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c09a-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2c09a-156">GetImItemList-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2c09a-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

