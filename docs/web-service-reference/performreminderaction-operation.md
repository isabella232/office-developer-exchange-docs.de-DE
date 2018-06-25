---
title: PerformReminderAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Hier finden Sie Informationen über die PerformReminderAction EWS Vorgang.
ms.openlocfilehash: 778fbb508413721f58cfcf9143a5296874e6cd1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830722"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="bdab7-103">PerformReminderAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bdab7-103">PerformReminderAction operation</span></span>

<span data-ttu-id="bdab7-104">Hier finden Sie Informationen zum **PerformReminderAction** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bdab7-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="bdab7-105">Der Vorgang des **PerformReminderAction** Exchange-Webdienste (EWS) initiiert eine Aktion schließen oder erneut erinnern auf eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="bdab7-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="bdab7-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bdab7-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="bdab7-107">Verwenden des PerformReminderAction-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="bdab7-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="bdab7-108">Den Vorgang **PerformReminderAction** können Sie schließen oder erneut erinnern (Verzögerung) Erinnerungen durch den Vorgang [GetReminders](getreminders-operation.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdab7-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="bdab7-109">Um eine Erinnerung snooze, die [ActionType](actiontype-reminderactiontype.md) auf **erneut erinnern**, und legen Sie den [NewReminderTime](newremindertime.md) Wert auf einen Zeitpunkt höher als die aktuelle [ReminderTime](remindertime.md)andernfalls die **NewReminderTime** wird vom Server ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bdab7-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="bdab7-110">Wenn die Erinnerung für ein Vorkommen einer Besprechungsserie wird und der **erneut erinnern** Aktionen auf die Erinnerung mit einer **NewReminderTime** , die die Erinnerung an das nächste Vorkommen überschreitet, wird die Erinnerung effektiv geschlossen.</span><span class="sxs-lookup"><span data-stu-id="bdab7-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="bdab7-111">Um eine Erinnerung zu schließen, legen Sie die **ActionType** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="bdab7-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="bdab7-112">Wenn der Server die Anforderung verarbeitet, ändert der Server den [IsReminderSet](isreminderset.md) Wert für das Element von **True** auf **false festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="bdab7-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="bdab7-113">PerformReminderAction Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="bdab7-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="bdab7-114">Der Vorgang **PerformReminderAction** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bdab7-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="bdab7-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="bdab7-115">**Header name**</span></span>|<span data-ttu-id="bdab7-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdab7-116">**Element**</span></span>|<span data-ttu-id="bdab7-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdab7-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bdab7-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="bdab7-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="bdab7-119">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="bdab7-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="bdab7-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="bdab7-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="bdab7-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bdab7-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bdab7-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="bdab7-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="bdab7-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="bdab7-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="bdab7-124">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdab7-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="bdab7-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bdab7-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bdab7-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="bdab7-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="bdab7-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="bdab7-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="bdab7-128">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="bdab7-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="bdab7-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="bdab7-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="bdab7-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="bdab7-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="bdab7-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bdab7-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="bdab7-132">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="bdab7-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="bdab7-133">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="bdab7-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="bdab7-134">PerformReminderAction Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="bdab7-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="bdab7-135">Im folgenden Beispiel wird eine **PerformReminderAction** Vorgang Anforderung veranschaulicht eine aktuelle Erinnerung snooze, und legen Sie eine neue Erinnerungszeit.</span><span class="sxs-lookup"><span data-stu-id="bdab7-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="bdab7-136">Beachten Sie, dass Sie die **ChangeKey** für die [ItemId](itemid.md) schließen müssen und die **NewReminderTime** auf einen Zeitpunkt höher als die durch den Vorgang [GetReminders](getreminders-operation.md) zurückgegebenen **ReminderTime** festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="bdab7-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
    <m:PerformReminderAction>
      <m:ReminderItemActions>
        <t:ReminderItemAction>
          <t:ActionType>Snooze</t:ActionType>
          <t:ItemId Id="vwAAAA=="
           ChangeKey="DwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAUDA=="/>
          <t:NewReminderTime>2014-04-16T17:00:00Z</t:NewReminderTime>
        </t:ReminderItemAction>
      </m:ReminderItemActions>
    </m:PerformReminderAction>
  </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> <span data-ttu-id="bdab7-137">Der **ItemId** -Wert wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdab7-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="bdab7-138">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bdab7-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bdab7-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="bdab7-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="bdab7-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="bdab7-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="bdab7-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="bdab7-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="bdab7-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="bdab7-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="bdab7-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="bdab7-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="bdab7-144">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="bdab7-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="bdab7-145">Erfolgreiche PerformReminderAction Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="bdab7-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="bdab7-146">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **PerformReminderAction** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="bdab7-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="bdab7-147">Das **UpdatedItemIds** -Element enthält die **Artikelnummern ein.** des aktualisierten Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="bdab7-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="bdab7-148">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bdab7-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bdab7-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="bdab7-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="bdab7-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bdab7-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bdab7-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="bdab7-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="bdab7-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="bdab7-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="bdab7-153">PerformReminderAction Vorgang Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="bdab7-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="bdab7-154">Das folgende Beispiel zeigt eine Antwort auf eine **PerformReminderAction** Vorgang an, wenn auf dem Server keine Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="bdab7-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="bdab7-155">Dies ist eine Antwort, in denen eine Anforderung gesendet wurde, aber keine **UpdatedItemIds** wurden zurückgegeben, was bedeutet, dass keine Erinnerungen geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="bdab7-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="bdab7-156">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="bdab7-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="bdab7-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="bdab7-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="bdab7-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bdab7-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bdab7-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="bdab7-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="bdab7-160">Zusätzliche Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="bdab7-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bdab7-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdab7-161">See also</span></span>


- [<span data-ttu-id="bdab7-162">GetReminders-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bdab7-162">GetReminders operation</span></span>](getreminders-operation.md)
    

