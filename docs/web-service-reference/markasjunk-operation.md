---
title: MarkAsJunk Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Hier finden Sie Informationen über die MarkAsJunk EWS Vorgang.
ms.openlocfilehash: b9d79e6fbec87ce41030b4981f3c16f2f9ce9507
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830353"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="0b6fd-103">MarkAsJunk Operation</span><span class="sxs-lookup"><span data-stu-id="0b6fd-103">MarkAsJunk operation</span></span>

<span data-ttu-id="0b6fd-104">Hier finden Sie Informationen zum **MarkAsJunk** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="0b6fd-105">Der Vorgang **MarkAsJunk** hinzugefügt und entfernt aus der Liste blockierter e-Mail-Benutzer und e-Mail-Nachrichten in den Junk-e-Mail-Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="0b6fd-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="0b6fd-107">Verwenden des MarkAsJunk-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="0b6fd-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="0b6fd-108">Der Vorgang **MarkAsJunk** enthält zwei boolesche Optionen, um anzugeben, ob ein e-Mail-Absender zur Liste blockierter Absender hinzugefügt werden soll, und gibt an, ob die Ziel-e-Mail-Nachricht in den Junk-e-Mail-Standardordner oder den Ordner Posteingang verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="0b6fd-109">Die Aktionen werden durch die Werte der Attribute **IsJunk** und **MoveItem** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="0b6fd-110">Im folgenden sind die möglichen Aktionen basierend auf den Wertkombinationen für die Attribute **IsJunk** und **MoveItem** :</span><span class="sxs-lookup"><span data-stu-id="0b6fd-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="0b6fd-111">Wenn das **IsJunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, der Absender der e-Mail-Zielnachricht wird die Liste der blockierten Absender hinzugefügt, und die e-Mail-Nachricht in den Junk-e-Dmail Ordner verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="0b6fd-112">Wenn das **IsJunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der e-Mail-Zielnachricht die Liste der blockierten Absender hinzugefügt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="0b6fd-113">Wenn das Attribut **IsJunk** festgelegt ist auf **false**und der **MoveItem** -Attribut auf **true fest,** den Absender der Ziel-e-Mail-Messageis aus der Liste blockierter Absender entfernt festgelegt ist und die e-Mail-Nachricht wird in den Ordner Posteingang verschoben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="0b6fd-114">Wenn das **IsJunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der e-Mail-Zielnachricht aus der Liste blockierter Absender entfernt und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="0b6fd-115">Der Inhalt der Liste blockierter Absender sind nicht von EWS sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="0b6fd-116">Wenn ein Absender zur Liste blockierter Absender hinzugefügt wird, müssen Sie eine Kopie einer e-Mail-Nachricht, die von der blockierten Absender gesendet, um den Absender in der Zukunft Aufheben der Blockierung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="0b6fd-117">MarkAsJunk Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="0b6fd-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="0b6fd-118">Der Vorgang **MarkAsJunk** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="0b6fd-119">**Headername**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-119">**Header name**</span></span>|<span data-ttu-id="0b6fd-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-120">**Element**</span></span>|<span data-ttu-id="0b6fd-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b6fd-122">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="0b6fd-123">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="0b6fd-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="0b6fd-124">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="0b6fd-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b6fd-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="0b6fd-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="0b6fd-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="0b6fd-128">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="0b6fd-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b6fd-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="0b6fd-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="0b6fd-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="0b6fd-132">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="0b6fd-133">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="0b6fd-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="0b6fd-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="0b6fd-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0b6fd-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="0b6fd-136">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="0b6fd-137">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="0b6fd-138">MarkAsJunk Vorgang-anforderungsbeispiel: einen Absender zur Liste blockierter Absender hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0b6fd-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="0b6fd-139">Im folgenden Beispiel wird eine **MarkAsJunk** Vorgang Anforderung veranschaulicht den Absender einer e-Mail aus der Liste blockierter Absender hinzufügen und die e-Mail-Nachricht in den Junk-e-Mailordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="0b6fd-140">Der **MarkAsJunk** -Vorgang akzeptiert den eigenen e-Mail-Nachrichtenbezeichner, um die e-Mail-Nachricht zu ermitteln, die verwendet wird, um den Absender verweisen, der die die Liste der blockierten Absender hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0b6fd-141">Bezeichner für alle Elemente aus, und Ändern von Schlüsseln in diesem Artikel wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="0b6fd-142">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="0b6fd-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b6fd-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0b6fd-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="0b6fd-144">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0b6fd-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b6fd-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="0b6fd-146">Erfolgreiche MarkAsJunk Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="0b6fd-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="0b6fd-147">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAsJunk** Vorgang an einen Absender zur Liste blockierter Absender hinzufügen und die e-Mail-Nachricht in den Junk-e-Mail-Ordner verschieben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
           <m:ResponseMessages>
               <m:MarkAsJunkResponseMessage ResponseClass="Success">
                  <m:ResponseCode>NoError</m:ResponseCode>
                 <m:MovedItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
               </m:MarkAsJunkResponseMessage>
           </m:ResponseMessages>
        </m:MarkAsJunkResponse>
    </s:Body>
</s:Envelope>
```

<span data-ttu-id="0b6fd-148">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="0b6fd-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b6fd-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="0b6fd-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="0b6fd-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b6fd-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0b6fd-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b6fd-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="0b6fd-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b6fd-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b6fd-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="0b6fd-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="0b6fd-154">MarkAsJunk Vorgang-anforderungsbeispiel: Entfernen von einem Absender aus der Liste blockierter Absender</span><span class="sxs-lookup"><span data-stu-id="0b6fd-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="0b6fd-155">Im folgenden Beispiel wird eine **MarkAsJunk** Vorgang Anforderung veranschaulicht den Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernen und die e-Mail-Nachricht in den Ordner Posteingang zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="0b6fd-156">Sie müssen eine e-Mail-Nachricht, die von der blockierten Absender gesendet, um den Absender aus der Liste der blockierten Absender zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="0b6fd-157">Die e-Mail-Adresse des Absenders ist zugeordnet, mit der e-Mail-Nachrichten, die vom Absender gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="0b6fd-158">Entfernen von einem Absender aus der Liste blockierter Absender erfolgreich nicht, wenn die Verweis e-Mail-Nachricht in das Postfach des Benutzers nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="0b6fd-159">Die Element-ID verwendet, um den Absender eine e-Mail-Nachricht zuordnen muss ein Element zugeordnet werden, die in der Exchange-Postfach vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="0b6fd-160">Es wird empfohlen, dass Sie Erstellen eines ausgeblendeten Ordners zum Speichern von Elementen, die von zuvor blockierten Absendern gesendet werden, sodass die Absender in der Clientanwendung aufgehoben werden können.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="0b6fd-161">Wenn ein Element aus dem Exchange-Postfach entfernt wurde, muss ein Administrator die Exchange-Verwaltungskonsole verwenden, um Zugriff auf die Liste der blockierten Absender, um einem Absender aus der Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="0b6fd-162">Informationen zum Aufheben der Blockierung ein Benutzers mithilfe der Exchange-Verwaltungskonsole finden Sie unter [Gewusst wie: Konfigurieren des sicherer Absender und blockierter Absender Settings in Office 365](http://support.microsoft.com/kb/2545137).</span><span class="sxs-lookup"><span data-stu-id="0b6fd-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](http://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="0b6fd-163">Eine erfolgreiche Antwort für das Entfernen von eines Absenders aus der Liste der blockierten Absender ist identisch mit der Antwort für das einen Absender zur Liste blockierter Absender hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="0b6fd-164">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="0b6fd-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b6fd-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="0b6fd-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="0b6fd-166">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0b6fd-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="0b6fd-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="0b6fd-168">MarkAsJunk Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="0b6fd-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="0b6fd-169">Das folgende Beispiel zeigt eine Fehlerantwort an eine **MarkAsJunk** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="0b6fd-170">Dies ist eine Antwort auf eine Anforderung zum Hinzufügen oder Entfernen von einem Absender aus der Liste blockierter Absender bei die e-Mail-Nachricht durch den Bezeichner des Elements angegeben nicht mehr im Postfach vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b6fd-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:MarkAsJunkResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:MarkAsJunkResponseMessage>
      </m:ResponseMessages>
    </m:MarkAsJunkResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="0b6fd-171">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="0b6fd-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="0b6fd-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="0b6fd-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="0b6fd-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0b6fd-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0b6fd-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0b6fd-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="0b6fd-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="0b6fd-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0b6fd-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0b6fd-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0b6fd-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0b6fd-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="0b6fd-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b6fd-178">See also</span></span>

- [<span data-ttu-id="0b6fd-179">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="0b6fd-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="0b6fd-180">[GetItem-Vorgang](getitem-operation.md) GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0b6fd-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="0b6fd-181">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0b6fd-181">FindItem operation</span></span>](finditem-operation.md)
    

