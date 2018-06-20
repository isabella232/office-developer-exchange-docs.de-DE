---
title: GetReminders-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Hier finden Sie Informationen über die GetReminders EWS Vorgang.
ms.openlocfilehash: 803dabf51b94dbd8fb01f2709a42ff59a597bfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758785"
---
# <a name="getreminders-operation"></a><span data-ttu-id="aaa2a-103">GetReminders-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aaa2a-103">GetReminders operation</span></span>

<span data-ttu-id="aaa2a-104">Hier finden Sie Informationen zum **GetReminders** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="aaa2a-105">Der Vorgang des **GetReminders** Exchange-Webdienste (EWS) werden für Kalender und Erinnerungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="aaa2a-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="aaa2a-107">Verwenden des GetReminders-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="aaa2a-107">Using the GetReminders operation</span></span>

<span data-ttu-id="aaa2a-108">Der Vorgang **GetReminders** ruft Erinnerungen für aktuellen und zukünftigen Kalender und Aufgabenelementen im Postfach des Benutzers, je nach der Elementwerte in der Anforderung übergeben.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="aaa2a-109">Alle aktuellen und zukünftigen Kalenderelemente sowie Aufgaben, bei die eine Erinnerung festgelegt haben, kann die Operation abrufen.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="aaa2a-110">Privaten Kalenderelementen sind in Antworten enthalten.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="aaa2a-111">Aufgaben ohne Erinnerungen sind nicht in Antworten, noch werden e-Mails mit Erinnerungen oder Flags nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="aaa2a-112">Rufen Sie alle aktuelle Erinnerungen wird empfohlen, die [ReminderType](remindertype.md) an **Alle** und die [EndTime](endtime-remindermessagedatatype.md) auf die aktuelle Zeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="aaa2a-113">Wenn die [BeginTime](begintime.md) und **EndTime für** Elemente in der Anforderung enthalten sind, die Antwort enthält Erinnerungen für alle Kalender und Aufgabenelementen, die zwischen auftreten haben eine Erinnerung, die zwischen den **BeginTime** und **EndTime**liegt.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="aaa2a-114">In der folgenden Tabelle wird das Verhalten des **ReminderType** -Elements beschrieben, wenn die Elemente **BeginTime** und **EndTime** enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="aaa2a-115">ReminderType ** Element Wert **</span><span class="sxs-lookup"><span data-stu-id="aaa2a-115">****ReminderType** element value**</span></span>|<span data-ttu-id="aaa2a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aaa2a-117">Alle</span><span class="sxs-lookup"><span data-stu-id="aaa2a-117">All</span></span>  <br/> |<span data-ttu-id="aaa2a-118">Erinnerungen, die zwischen dem **BeginTime** und **EndTime**auftreten.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="aaa2a-119">Aktuelle</span><span class="sxs-lookup"><span data-stu-id="aaa2a-119">Current</span></span>  <br/> |<span data-ttu-id="aaa2a-120">Erinnerungen zurückgegebene **Alle**, plus Erinnerungen, die älter als die angeforderte Zeitfenster sind Wenn das Ereignis noch laufende plus alle Termine unabhängig von Alter.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="aaa2a-121">Alte</span><span class="sxs-lookup"><span data-stu-id="aaa2a-121">Old</span></span>  <br/> |<span data-ttu-id="aaa2a-122">Erinnerungen zurückgegebene **Alle**, minus Ereignisse, die noch nicht minus alle Termine abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="aaa2a-123">Die Elemente **BeginTime** und **EndTime** müssen den **alten** Wert verwenden, festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="aaa2a-124">GetReminders Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="aaa2a-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="aaa2a-125">Der Vorgang **GetReminders** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="aaa2a-126">**Headername**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-126">**Header name**</span></span>|<span data-ttu-id="aaa2a-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-127">**Element**</span></span>|<span data-ttu-id="aaa2a-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aaa2a-129">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="aaa2a-130">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="aaa2a-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="aaa2a-131">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="aaa2a-132">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aaa2a-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="aaa2a-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="aaa2a-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="aaa2a-135">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="aaa2a-136">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aaa2a-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="aaa2a-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="aaa2a-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="aaa2a-139">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="aaa2a-140">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aaa2a-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="aaa2a-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="aaa2a-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="aaa2a-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="aaa2a-143">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="aaa2a-144">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="aaa2a-145">GetReminders Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="aaa2a-145">GetReminders operation request example</span></span>

<span data-ttu-id="aaa2a-146">Im folgenden Beispiel wird eine **GetReminders** Vorgang Anforderung veranschaulicht, wie die ersten fünf Kalenderelemente abgerufen, die zwischen dem **BeginTime** und **EndTime**auftreten.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
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
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="aaa2a-147">Die Beispiel für eine Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aaa2a-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="aaa2a-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="aaa2a-149">EndTime</span><span class="sxs-lookup"><span data-stu-id="aaa2a-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="aaa2a-150">ReminderType</span><span class="sxs-lookup"><span data-stu-id="aaa2a-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="aaa2a-151">Der SOAP-Text kann auch die folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="aaa2a-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="aaa2a-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="aaa2a-153">MaxItems wird</span><span class="sxs-lookup"><span data-stu-id="aaa2a-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="aaa2a-154">Erfolgreiche GetReminders Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="aaa2a-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="aaa2a-155">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetReminders** Vorgang an.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="aaa2a-156">Die Antwort enthält eine Erinnerung für das Kalenderelement "Team-Meeting" und eine Erinnerung für die Aufgabe "Vorgang zum Senden von Besprechungsnotizen".</span><span class="sxs-lookup"><span data-stu-id="aaa2a-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aaa2a-157">Bezeichner wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-157">Identifiers have been shortened to preserve readability.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Team meeting</Subject>
          <Location />
          <ReminderTime>2014-04-15T21:00:00Z</ReminderTime>
          <StartDate>2014-04-15T21:00:00Z</StartDate>
          <EndDate>2014-04-15T21:30:00Z</EndDate>
          <ItemId Id="vQAAAA=="
                  ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV4" />
          <RecurringMasterItemId Id="K7u5AAA=" ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV0" />
          <ReminderGroup>Calendar</ReminderGroup>
          <UID>6CF2FA62</UID>
        </Reminder>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Task to send meeting notes</Subject>
          <Location />
          <ReminderTime>2014-04-16T14:00:00Z</ReminderTime>
          <StartDate>0001-01-02T00:00:00Z</StartDate>
          <EndDate>0001-01-02T00:00:00Z</EndDate>
          <ItemId Id="vAAAAA=="
                  ChangeKey="EwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAIDg==" />
          <ReminderGroup>Task</ReminderGroup>
          <UID>vAAAAA==</UID>
        </Reminder>
      </Reminders>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aaa2a-158">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aaa2a-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="aaa2a-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="aaa2a-160">Reminders</span><span class="sxs-lookup"><span data-stu-id="aaa2a-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="aaa2a-161">Reminder</span><span class="sxs-lookup"><span data-stu-id="aaa2a-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="aaa2a-162">Betreff</span><span class="sxs-lookup"><span data-stu-id="aaa2a-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="aaa2a-163">Ort</span><span class="sxs-lookup"><span data-stu-id="aaa2a-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="aaa2a-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="aaa2a-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="aaa2a-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="aaa2a-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="aaa2a-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="aaa2a-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="aaa2a-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="aaa2a-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="aaa2a-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="aaa2a-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="aaa2a-169">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="aaa2a-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="aaa2a-170">UID</span><span class="sxs-lookup"><span data-stu-id="aaa2a-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="aaa2a-171">GetReminders Vorgang Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="aaa2a-171">GetReminders operation error response example</span></span>

<span data-ttu-id="aaa2a-172">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetReminders** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="aaa2a-173">Dies ist eine Antwort auf eine Anforderung, in der das Enddatum einer älteren Version als der Anfangstermin war.</span><span class="sxs-lookup"><span data-stu-id="aaa2a-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aaa2a-174">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aaa2a-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aaa2a-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="aaa2a-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="aaa2a-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="aaa2a-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="aaa2a-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="aaa2a-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="aaa2a-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="aaa2a-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="aaa2a-179">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="aaa2a-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aaa2a-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaa2a-180">See also</span></span>


- [<span data-ttu-id="aaa2a-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="aaa2a-181">PerformReminderAction</span></span>](performreminderaction.md)
    

