---
title: MarkAsJunk-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1f71f04d-56a9-4fee-a4e7-d1034438329e
description: Hier finden Sie Informationen zum MarkAsJunk-EWS-Vorgang.
ms.openlocfilehash: 25d6b01dfff64c4e45f3382223311219d349c165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468572"
---
# <a name="markasjunk-operation"></a><span data-ttu-id="d10da-103">MarkAsJunk-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d10da-103">MarkAsJunk operation</span></span>

<span data-ttu-id="d10da-104">Hier finden Sie Informationen zum **MarkAsJunk** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d10da-104">Find information about the **MarkAsJunk** EWS operation.</span></span> 
  
<span data-ttu-id="d10da-105">Mit dem **MarkAsJunk** -Vorgang werden Benutzer aus der Liste blockierter e-Mails hinzugefügt und entfernt und e-Mail-Nachrichten in den Ordner Junk-e-Mail verschoben</span><span class="sxs-lookup"><span data-stu-id="d10da-105">The **MarkAsJunk** operation adds and removes users from the blocked email list and moves email messages to the Junk Email folder.</span></span> 
  
<span data-ttu-id="d10da-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d10da-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-markasjunk-operation"></a><span data-ttu-id="d10da-107">Verwenden des MarkAsJunk-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d10da-107">Using the MarkAsJunk operation</span></span>

<span data-ttu-id="d10da-108">Der **MarkAsJunk** -Vorgang enthält zwei boolesche Optionen, um anzugeben, ob ein e-Mail-Absender zur Liste blockierter Absender hinzugefügt werden soll und ob die Ziel-e-Mail in den standardmäßigen Junk-e-Mail-Ordner oder in den Ordner Posteingang verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d10da-108">The **MarkAsJunk** operation contains two Boolean options to indicate whether an email sender should be added to the blocked sender list and whether the target email message should be moved to the default Junk Email folder or the Inbox folder.</span></span> <span data-ttu-id="d10da-109">Die Aktionen werden durch die Werte der Attribute **isjunk** und **MoveItem** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d10da-109">The actions are determined by the values of the **IsJunk** and **MoveItem** attributes.</span></span> <span data-ttu-id="d10da-110">Im folgenden sind die möglichen Aktionen basierend auf den Wertkombinationen für die Attribute **isjunk** und **MoveItem** aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d10da-110">The following are the possible actions based on the value combinations for the **IsJunk** and **MoveItem** attributes:</span></span> 
  
- <span data-ttu-id="d10da-111">Wenn das **isjunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht zur Liste blockierter Absender hinzugefügt, und die e-Mail-Nachricht wird in den Ordner Junk-dmail verschoben.</span><span class="sxs-lookup"><span data-stu-id="d10da-111">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **true**, the sender of the target email message is added to the blocked sender list and the email message is moved to the Junk Dmail folder.</span></span>
    
- <span data-ttu-id="d10da-112">Wenn das **isjunk** -Attribut auf **true**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht zur Liste blockierter Absender hinzugefügt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="d10da-112">If the **IsJunk** attribute is set to **true**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is added to the blocked sender list and the email message is not moved from the folder.</span></span>
    
- <span data-ttu-id="d10da-113">Wenn das **isjunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **true**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht aus der Liste blockierter Absender entfernt, und die e-Mail-Nachricht wird in den Ordner Posteingang verschoben.</span><span class="sxs-lookup"><span data-stu-id="d10da-113">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **true**, the sender of the target email messageis removed from the blocked sender list and the email message is moved to the Inbox folder.</span></span>
    
- <span data-ttu-id="d10da-114">Wenn das **isjunk** -Attribut auf **false**festgelegt ist und das **MoveItem** -Attribut auf **false**festgelegt ist, wird der Absender der Ziel-e-Mail-Nachricht aus der Liste blockierter Absender entfernt, und die e-Mail-Nachricht wird nicht aus dem Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="d10da-114">If the **IsJunk** attribute is set to **false**, and the **MoveItem** attribute is set to **false**, the sender of the target email message is removed from the blocked sender list and the email message is not moved from the folder.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="d10da-115">Der Inhalt der Liste blockierter Absender ist nicht von EWS auffindbar.</span><span class="sxs-lookup"><span data-stu-id="d10da-115">The contents of the blocked sender list are not discoverable from EWS.</span></span> <span data-ttu-id="d10da-116">Wenn der Liste blockierter Absender ein Absender hinzugefügt wird, müssen Sie eine Kopie einer vom blockierten Absender gesendeten e-Mail-Nachricht behalten, um den Absender zukünftig aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="d10da-116">If a sender is added to the blocked sender list, you need to keep a copy of an email message sent by the blocked sender to unblock the sender in the future.</span></span> 
  
### <a name="markasjunk-operation-soap-headers"></a><span data-ttu-id="d10da-117">SOAP-Header des MarkAsJunk-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d10da-117">MarkAsJunk operation SOAP headers</span></span>

<span data-ttu-id="d10da-118">Der **MarkAsJunk** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d10da-118">The **MarkAsJunk** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d10da-119">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d10da-119">**Header name**</span></span>|<span data-ttu-id="d10da-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="d10da-120">**Element**</span></span>|<span data-ttu-id="d10da-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d10da-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d10da-122">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="d10da-122">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d10da-123">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="d10da-123">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d10da-124">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="d10da-124">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="d10da-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d10da-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d10da-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="d10da-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="d10da-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d10da-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="d10da-128">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d10da-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="d10da-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d10da-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d10da-130">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d10da-130">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d10da-131">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d10da-131">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d10da-132">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d10da-132">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d10da-133">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d10da-133">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d10da-134">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d10da-134">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d10da-135">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d10da-135">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d10da-136">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d10da-136">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d10da-137">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d10da-137">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="markasjunk-operation-request-example-add-a-sender-to-the-blocked-sender-list"></a><span data-ttu-id="d10da-138">MarkAsJunk-Vorgangs Anforderungs Beispiel: Hinzufügen eines Absenders zur Liste blockierter Absender</span><span class="sxs-lookup"><span data-stu-id="d10da-138">MarkAsJunk operation request example: Add a sender to the blocked sender list</span></span>

<span data-ttu-id="d10da-139">Im folgenden Beispiel einer **MarkAsJunk** -Vorgangsanforderung wird gezeigt, wie der Absender einer e-Mail zur Liste blockierter Absender hinzugefügt und die e-Mail in den Junk-e-Mail-Ordner verschiebt wird.</span><span class="sxs-lookup"><span data-stu-id="d10da-139">The following example of a **MarkAsJunk** operation request shows how to add the sender of an email to the blocked sender list and move the email to the junk mail folder.</span></span> <span data-ttu-id="d10da-140">Der **MarkAsJunk** -Vorgang akzeptiert die eindeutige ID der e-Mail-Nachricht, um die e-Mail zu identifizieren, die zum Verweisen auf den Absender verwendet wird, der der Liste blockierter Absender hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d10da-140">The **MarkAsJunk** operation accepts the unique email message identifier to identify the email that is used to reference the sender that is added to the blocked sender list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d10da-141">Alle Element-IDs und Änderungsschlüssel in diesem Artikel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d10da-141">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
        <m:MarkAsJunk IsJunk="true" MoveItem="true">
            <m:ItemIds>
                <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYA" />
            </m:ItemIds>
        </m:MarkAsJunk>
    </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="d10da-142">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d10da-142">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d10da-143">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="d10da-143">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="d10da-144">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d10da-144">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d10da-145">ItemId</span><span class="sxs-lookup"><span data-stu-id="d10da-145">ItemId</span></span>](itemid.md)
    
## <a name="successful-markasjunk-operation-response"></a><span data-ttu-id="d10da-146">Erfolgreiche Reaktion des MarkAsJunk-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d10da-146">Successful MarkAsJunk operation response</span></span>

<span data-ttu-id="d10da-147">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MarkAsJunk** -Vorgangsanforderung zum Hinzufügen eines Absenders zur Liste blockierter Absender und zum Verlegen der e-Mail-Nachricht in den Junk-e-Mail-Ordner.</span><span class="sxs-lookup"><span data-stu-id="d10da-147">The following example shows a successful response to a **MarkAsJunk** operation request to add a sender to the blocked sender list and move the email message to the Junk Email folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                             MinorVersion="0" 
                             MajorBuildNumber="545" 
                             MinorBuildNumber="11" 
                             Version="Exchange2013" 
                             xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                             xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d10da-148">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d10da-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d10da-149">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="d10da-149">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="d10da-150">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d10da-150">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d10da-151">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d10da-151">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="d10da-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d10da-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d10da-153">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="d10da-153">MovedItemId</span></span>](moveditemid.md)
    
## <a name="markasjunk-operation-request-example-remove-a-sender-from-the-blocked-sender-list"></a><span data-ttu-id="d10da-154">MarkAsJunk-Vorgangs Anforderungs Beispiel: Entfernen eines Absenders aus der Liste blockierter Absender</span><span class="sxs-lookup"><span data-stu-id="d10da-154">MarkAsJunk operation request example: Remove a sender from the blocked sender list</span></span>

<span data-ttu-id="d10da-155">Im folgenden Beispiel einer **MarkAsJunk** -Vorgangsanforderung wird gezeigt, wie der Absender einer e-Mail-Nachricht aus der Liste blockierter Absender entfernt und die e-Mail-Nachricht in den Ordner Posteingang verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d10da-155">The following example of a **MarkAsJunk** operation request shows how to remove the sender of an email message from the blocked sender list and move the email message to the Inbox folder.</span></span> <span data-ttu-id="d10da-156">Sie müssen eine vom blockierten Absender gesendete e-Mail-Nachricht beibehalten, um den Absender aus der Liste blockierter Absender zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d10da-156">You need to keep an email message sent by the blocked sender to remove the sender from the blocked sender list.</span></span> <span data-ttu-id="d10da-157">Die e-Mail-Adresse des Absenders ist e-Mail-Nachrichten zugeordnet, die vom Absender gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d10da-157">The sender's email address is associated with email messages that have been sent by the sender.</span></span> <span data-ttu-id="d10da-158">Das Entfernen eines Absenders aus der Liste blockierter Absender ist nicht erfolgreich, wenn die Referenz-e-Mail-Nachricht nicht mehr im Postfach des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d10da-158">Removing a sender from the blocked sender list will not succeed if the reference email message no longer exists in the user's mailbox.</span></span> <span data-ttu-id="d10da-159">Die Element-ID, die zum Zuordnen einer e-Mail-Nachricht zu ihrem Absender verwendet wird, muss einem Element zugeordnet sein, das im Exchange-Postfach vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d10da-159">The item identifier used to associate an email message with its sender must be associated with an item that exists in the Exchange mailbox.</span></span> <span data-ttu-id="d10da-160">Es wird empfohlen, einen ausgeblendeten Ordner zum Speichern von Elementen zu erstellen, die von zuvor blockierten Absendern gesendet wurden, sodass die Blockierung der Absender von der Clientanwendung aufgehoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d10da-160">We recommend that you create a hidden folder to store items sent by previously blocked senders so that the senders can be unblocked from the client application.</span></span> <span data-ttu-id="d10da-161">Für den Fall, dass ein Element aus dem Exchange-Postfach entfernt wurde, muss ein Administrator die Exchange-Verwaltungskonsole verwenden, um auf die Liste blockierter Absender zuzugreifen, um einen Absender aus der Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d10da-161">In the event that an item has been removed from the Exchange mailbox, an administrator has to use the Exchange Management Console to access the blocked sender list to remove a sender from the list.</span></span> <span data-ttu-id="d10da-162">Informationen zum Aufheben der Blockierung eines Benutzers mithilfe der Exchange-Verwaltungskonsole finden Sie unter [Konfigurieren der Einstellungen für sichere Absender und blockierte Absender in Office 365](https://support.microsoft.com/kb/2545137).</span><span class="sxs-lookup"><span data-stu-id="d10da-162">For information about how to unblock a user by using the Exchange Management Console, see [How to configure the safe senders and blocked senders settings in Office 365](https://support.microsoft.com/kb/2545137).</span></span>
  
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
      <m:MarkAsJunk IsJunk="false" MoveItem="true">
        <m:ItemIds>
          <t:ItemId Id="AAMkAD=" ChangeKey="CQAAABYu" />
        </m:ItemIds>
      </m:MarkAsJunk>
    </soap:Body>
 </soap:Envelope>

```

<span data-ttu-id="d10da-163">Eine erfolgreiche Antwort zum Entfernen eines Absenders aus der Liste blockierter Absender ist identisch mit der Antwort zum Hinzufügen eines Absenders zur Liste blockierter Absender.</span><span class="sxs-lookup"><span data-stu-id="d10da-163">A successful response for removing a sender from the blocked sender list is the same as the response for adding a sender to the blocked sender list.</span></span>
  
<span data-ttu-id="d10da-164">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d10da-164">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d10da-165">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="d10da-165">MarkAsJunk</span></span>](markasjunk.md)
    
- [<span data-ttu-id="d10da-166">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d10da-166">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="d10da-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="d10da-167">ItemId</span></span>](itemid.md)
    
## <a name="markasjunk-operation-error-response"></a><span data-ttu-id="d10da-168">Fehlerantwort des MarkAsJunk-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d10da-168">MarkAsJunk operation error response</span></span>

<span data-ttu-id="d10da-169">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **MarkAsJunk** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d10da-169">The following example shows an error response to a **MarkAsJunk** operation request.</span></span> <span data-ttu-id="d10da-170">Dies ist eine Antwort auf eine Anforderung zum Hinzufügen oder Entfernen eines Absenders aus der Liste blockierter Absender, wenn die durch die Element-ID angegebene e-Mail-Nachricht nicht mehr im Postfach vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d10da-170">This is a response to a request to add or remove a sender from the blocked sender list when the email message specified by the item identifier no longer exists in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="545" 
                         MinorBuildNumber="11" 
                         Version="Exchange2013" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:MarkAsJunkResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d10da-171">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d10da-171">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d10da-172">MarkAsJunkResponse</span><span class="sxs-lookup"><span data-stu-id="d10da-172">MarkAsJunkResponse</span></span>](markasjunkresponse.md)
    
- [<span data-ttu-id="d10da-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d10da-173">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="d10da-174">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d10da-174">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
    
- [<span data-ttu-id="d10da-175">MessageText</span><span class="sxs-lookup"><span data-stu-id="d10da-175">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d10da-176">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d10da-176">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d10da-177">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d10da-177">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="d10da-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d10da-178">See also</span></span>

- [<span data-ttu-id="d10da-179">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="d10da-179">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- <span data-ttu-id="d10da-180">[GetItem-Vorgang](getitem-operation.md) GetItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d10da-180">[GetItem operation](getitem-operation.md) GetItem operation</span></span> 
    
- [<span data-ttu-id="d10da-181">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d10da-181">FindItem operation</span></span>](finditem-operation.md)
    

