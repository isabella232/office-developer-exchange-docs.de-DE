---
title: PerformReminderAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Hier finden Sie Informationen zum PerformReminderAction-EWS-Vorgang.
ms.openlocfilehash: 4c069d541e9a42167c447a50c405399958d3608d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462290"
---
# <a name="performreminderaction-operation"></a><span data-ttu-id="764ab-103">PerformReminderAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="764ab-103">PerformReminderAction operation</span></span>

<span data-ttu-id="764ab-104">Hier finden Sie Informationen zum **PerformReminderAction** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="764ab-104">Find information about the **PerformReminderAction** EWS operation.</span></span> 
  
<span data-ttu-id="764ab-105">Die **PerformReminderAction** -Exchange-Webdienste Operation initiiert eine Kündigungs-oder Snooze-Aktion für eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="764ab-105">The **PerformReminderAction** Exchange Web Services (EWS) operation initiates a dismiss or snooze action on a reminder.</span></span> 
  
<span data-ttu-id="764ab-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="764ab-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-performreminderaction-operation"></a><span data-ttu-id="764ab-107">Verwenden des PerformReminderAction-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="764ab-107">Using the PerformReminderAction operation</span></span>

<span data-ttu-id="764ab-108">Sie können den **PerformReminderAction** -Vorgang verwenden, um Erinnerungen, die von der [geterinnerungs](getreminders-operation.md) -Operation zurückgegeben werden, zu schließen oder zu Snooze (Delay).</span><span class="sxs-lookup"><span data-stu-id="764ab-108">You can use the **PerformReminderAction** operation to dismiss or snooze (delay) reminders returned by the [GetReminders](getreminders-operation.md) operation.</span></span> <span data-ttu-id="764ab-109">Um eine Erinnerung zu snoozen, legen Sie den [Action](actiontype-reminderactiontype.md) Type auf **Snooze**fest, und legen Sie den Wert für die [neumahnung](newremindertime.md) auf einen Zeitpunkt nach der aktuellen [Erinnerungs](remindertime.md)Zeit fest, andernfalls wird die **neuerinnerung** vom Server ignoriert.</span><span class="sxs-lookup"><span data-stu-id="764ab-109">To snooze a reminder, set the [ActionType](actiontype-reminderactiontype.md) to **Snooze**, and set the [NewReminderTime](newremindertime.md) value to a time later than the current [ReminderTime](remindertime.md), otherwise the **NewReminderTime** is ignored by the server.</span></span> <span data-ttu-id="764ab-110">Wenn es sich bei der Erinnerung um ein Auftreten einer Besprechungsserie handelt und die **Snooze** -Aktion in der Erinnerung mit einer Erinnerungszeit angezeigt **wird, die** über die Erinnerung an das nächste Vorkommen verfügt, wird die Erinnerung effektiv zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="764ab-110">If the reminder is for an occurrence of a recurring meeting, and the **Snooze** action is taken on the reminder with a **NewReminderTime** that is past the reminder of the next occurrence, the reminder is effectively dismissed.</span></span> 
  
<span data-ttu-id="764ab-111">Um eine Erinnerung zu schließen, legen Sie den **Action** Type auf **entlassen**fest.</span><span class="sxs-lookup"><span data-stu-id="764ab-111">To dismiss a reminder, set the **ActionType** to **Dismiss**.</span></span> <span data-ttu-id="764ab-112">Wenn der Server die Anforderung verarbeitet, ändert der Server den [Reminder](isreminderset.md) -Wert für das Element von **true** in **false**.</span><span class="sxs-lookup"><span data-stu-id="764ab-112">When the server processes the request, the server changes the [IsReminderSet](isreminderset.md) value for the item from **True** to **False**.</span></span>
  
### <a name="performreminderaction-operation-soap-headers"></a><span data-ttu-id="764ab-113">SOAP-Header des PerformReminderAction-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="764ab-113">PerformReminderAction operation SOAP headers</span></span>

<span data-ttu-id="764ab-114">Der **PerformReminderAction** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="764ab-114">The **PerformReminderAction** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="764ab-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="764ab-115">**Header name**</span></span>|<span data-ttu-id="764ab-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="764ab-116">**Element**</span></span>|<span data-ttu-id="764ab-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="764ab-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="764ab-118">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="764ab-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="764ab-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="764ab-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="764ab-120">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="764ab-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="764ab-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="764ab-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="764ab-122">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="764ab-122">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="764ab-123">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="764ab-123">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="764ab-124">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="764ab-124">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="764ab-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="764ab-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="764ab-126">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="764ab-126">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="764ab-127">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="764ab-127">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="764ab-128">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="764ab-128">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="764ab-129">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="764ab-129">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="764ab-130">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="764ab-130">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="764ab-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="764ab-131">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="764ab-132">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="764ab-132">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="764ab-133">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="764ab-133">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a><span data-ttu-id="764ab-134">PerformReminderAction-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="764ab-134">PerformReminderAction operation request example</span></span>

<span data-ttu-id="764ab-135">Im folgenden Beispiel einer **PerformReminderAction** -Vorgangsanforderung wird gezeigt, wie eine aktuelle Erinnerung eingeschlummert und eine neue Erinnerungszeit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="764ab-135">The following example of a **PerformReminderAction** operation request shows how to snooze a current reminder and set a new reminder time.</span></span> <span data-ttu-id="764ab-136">Beachten Sie, dass Sie das **ChangeKey** -Objekt für [das Itemid](itemid.md) -Objekt einschließen müssen und die **Reminder** -Uhrzeit auf eine Zeitspanne festgelegt sein muss, die von der **Reminders** [-Operation zurück](getreminders-operation.md) gegeben wird.</span><span class="sxs-lookup"><span data-stu-id="764ab-136">Note that you need to include the **ChangeKey** for the [ItemId](itemid.md) and the **NewReminderTime** must be set to a time later than the **ReminderTime** returned by the [GetReminders](getreminders-operation.md) operation.</span></span> 
  
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
> <span data-ttu-id="764ab-137">Der **ItemID** -Wert wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="764ab-137">The **ItemId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="764ab-138">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="764ab-138">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="764ab-139">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="764ab-139">PerformReminderAction</span></span>](performreminderaction.md)
    
- [<span data-ttu-id="764ab-140">ReminderItemActions</span><span class="sxs-lookup"><span data-stu-id="764ab-140">ReminderItemActions</span></span>](reminderitemactions.md)
    
- [<span data-ttu-id="764ab-141">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="764ab-141">ReminderItemAction</span></span>](reminderitemaction.md)
    
- [<span data-ttu-id="764ab-142">ActionType</span><span class="sxs-lookup"><span data-stu-id="764ab-142">ActionType</span></span>](actiontype-reminderactiontype.md)
    
- [<span data-ttu-id="764ab-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="764ab-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="764ab-144">Neuerinnerung</span><span class="sxs-lookup"><span data-stu-id="764ab-144">NewReminderTime</span></span>](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a><span data-ttu-id="764ab-145">Erfolgreiche Reaktion des PerformReminderAction-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="764ab-145">Successful PerformReminderAction operation response</span></span>

<span data-ttu-id="764ab-146">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **PerformReminderAction** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="764ab-146">The following example shows a successful response to a **PerformReminderAction** operation request.</span></span> <span data-ttu-id="764ab-147">Das **UpdatedItemIds** -Element enthält die **itemids** des aktualisierten Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="764ab-147">The **UpdatedItemIds** element contains the **ItemIds** of the updated calendar item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="764ab-148">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="764ab-148">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="764ab-149">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="764ab-149">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="764ab-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="764ab-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="764ab-151">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="764ab-151">UpdatedItemIds</span></span>](updateditemids.md)
    
- [<span data-ttu-id="764ab-152">ItemId</span><span class="sxs-lookup"><span data-stu-id="764ab-152">ItemId</span></span>](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a><span data-ttu-id="764ab-153">PerformReminderAction-Operation-Fehlerantwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="764ab-153">PerformReminderAction operation error response example</span></span>

<span data-ttu-id="764ab-154">Das folgende Beispiel zeigt eine Antwort auf eine **PerformReminderAction** -Vorgangsanforderung, wenn keine Änderung auf dem Server vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="764ab-154">The following example shows a response to a **PerformReminderAction** operation request when no change was made on the server.</span></span> <span data-ttu-id="764ab-155">Dies ist eine Antwort, bei der eine Anforderung gesendet wurde, aber keine **UpdatedItemIds** zurückgegeben wurden, was bedeutet, dass keine Erinnerungen geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="764ab-155">This is a response in which a request was sent, but no **UpdatedItemIds** were returned, meaning no reminders were changed.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="764ab-156">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="764ab-156">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="764ab-157">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="764ab-157">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
    
- [<span data-ttu-id="764ab-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="764ab-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="764ab-159">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="764ab-159">UpdatedItemIds</span></span>](updateditemids.md)
    
<span data-ttu-id="764ab-160">Weitere Fehlercodes, die für EWS allgemein sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="764ab-160">For additional error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="764ab-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="764ab-161">See also</span></span>


- [<span data-ttu-id="764ab-162">GetReminders-Vorgang</span><span class="sxs-lookup"><span data-stu-id="764ab-162">GetReminders operation</span></span>](getreminders-operation.md)
    

