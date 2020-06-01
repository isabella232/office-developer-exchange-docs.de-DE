---
title: GetReminders-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Hier finden Sie Informationen zum reerinnerungs-EWS-Vorgang.
ms.openlocfilehash: dcbe20c674d7524a7776d374fa6964899abf472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458306"
---
# <a name="getreminders-operation"></a><span data-ttu-id="aec8a-103">GetReminders-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aec8a-103">GetReminders operation</span></span>

<span data-ttu-id="aec8a-104">Hier finden Sie Informationen zum **reerinnerungs** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="aec8a-104">Find information about the **GetReminders** EWS operation.</span></span> 
  
<span data-ttu-id="aec8a-105">Mit **dem** Reminder-Exchange-Webdienste Vorgang werden Erinnerungen für Kalender-und Aufgabenelemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aec8a-105">The **GetReminders** Exchange Web Services (EWS) operation retrieves reminders for calendar and task items.</span></span> 
  
<span data-ttu-id="aec8a-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="aec8a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getreminders-operation"></a><span data-ttu-id="aec8a-107">Verwenden der reerinnerungs-Operation</span><span class="sxs-lookup"><span data-stu-id="aec8a-107">Using the GetReminders operation</span></span>

<span data-ttu-id="aec8a-108">Der **geterinnerungs** -Vorgang ruft Erinnerungen für aktuelle und zukünftige Kalender-und Aufgabenelemente im Postfach des Benutzers ab, abhängig von den in der Anforderung übergebenen Elementwerten.</span><span class="sxs-lookup"><span data-stu-id="aec8a-108">The **GetReminders** operation gets reminders for current and future calendar and task items in the user's mailbox, depending on the element values passed in the request.</span></span> <span data-ttu-id="aec8a-109">Mit dem Vorgang können alle aktuellen und zukünftigen Kalenderelemente sowie Aufgaben abgerufen werden, für die eine Erinnerung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="aec8a-109">The operation can retrieve all current and future calendar items as well as tasks that have a reminder set.</span></span> <span data-ttu-id="aec8a-110">Private Kalenderelemente werden in den Antworten eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aec8a-110">Private calendar items are included in responses.</span></span> <span data-ttu-id="aec8a-111">Aufgaben ohne Erinnerungen werden in den Antworten nicht berücksichtigt, und es handelt sich auch nicht um e-Mails mit Erinnerungen oder Nachverfolgungskennzeichen.</span><span class="sxs-lookup"><span data-stu-id="aec8a-111">Tasks without reminders are not included in responses, nor are emails with reminders or follow up flags.</span></span> 
  
<span data-ttu-id="aec8a-112">Zum Abrufen aller aktuellen Erinnerungen empfiehlt es sich, den [Reminder](remindertype.md) auf " **all** " und " [EndTime](endtime-remindermessagedatatype.md) " auf die aktuelle Uhrzeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aec8a-112">To retrieve all current reminders, we recommend setting the [ReminderType](remindertype.md) to **All** and the [EndTime](endtime-remindermessagedatatype.md) to the current time.</span></span> 
  
<span data-ttu-id="aec8a-113">Wenn die [BeginTime](begintime.md) -und **EndTime** -Elemente in der Anforderung enthalten sind, enthält die Antwort Erinnerungen für alle Kalender-und Aufgabenelemente, die zwischen einer Erinnerung zwischen dem **BeginTime** und **EndTime**stattfinden.</span><span class="sxs-lookup"><span data-stu-id="aec8a-113">If the [BeginTime](begintime.md) and **EndTime** elements are included in the request, the response includes reminders for any calendar and task items that occur between have a reminder that occurs between the **BeginTime** and **EndTime**.</span></span>
  
<span data-ttu-id="aec8a-114">In der folgenden Tabelle wird das Verhalten des **Reminder** -Elements beschrieben, wenn die Elemente **BeginTime** und **EndTime** enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aec8a-114">The following table describes the behavior of the **ReminderType** element when the **BeginTime** and **EndTime** elements are included.</span></span> 
  
|<span data-ttu-id="aec8a-115">Reminder \* \*-Elementwert \* \*</span><span class="sxs-lookup"><span data-stu-id="aec8a-115">\*\*\*\*ReminderType\*\* element value\*\*</span></span>|<span data-ttu-id="aec8a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aec8a-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aec8a-117">Alle</span><span class="sxs-lookup"><span data-stu-id="aec8a-117">All</span></span>  <br/> |<span data-ttu-id="aec8a-118">Erinnerungen, die zwischen **BeginTime** und **EndTime**auftreten.</span><span class="sxs-lookup"><span data-stu-id="aec8a-118">Reminders that occur between the **BeginTime** and **EndTime**.</span></span>  <br/> |
|<span data-ttu-id="aec8a-119">Current</span><span class="sxs-lookup"><span data-stu-id="aec8a-119">Current</span></span>  <br/> |<span data-ttu-id="aec8a-120">Erinnerungen, die von **allen**zurückgegeben werden, sowie Erinnerungen, die vor dem angeforderten Zeitfenster liegen, wenn das Ereignis noch nicht abgeschlossen ist, sowie alle Termine unabhängig vom Alter.</span><span class="sxs-lookup"><span data-stu-id="aec8a-120">Reminders returned by **All**, plus reminders that are earlier than the requested time window if the event is still ongoing, plus all appointments regardless of age.</span></span>  <br/> |
|<span data-ttu-id="aec8a-121">Alten</span><span class="sxs-lookup"><span data-stu-id="aec8a-121">Old</span></span>  <br/> |<span data-ttu-id="aec8a-122">Erinnerungen, die von **allen**zurückgegeben werden, minus Ereignisse, die noch nicht abgeschlossen wurden, abzüglich aller Termine.</span><span class="sxs-lookup"><span data-stu-id="aec8a-122">Reminders returned by **All**, minus events that haven't completed yet, minus all appointments.</span></span> <span data-ttu-id="aec8a-123">Die **BeginTime** -und **EndTime** -Elemente müssen festgelegt werden, um den **alten** Wert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aec8a-123">The **BeginTime** and **EndTime** elements must be set to use the **Old** value.</span></span>  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a><span data-ttu-id="aec8a-124">Reerinnerungs-Operation SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="aec8a-124">GetReminders operation SOAP headers</span></span>

<span data-ttu-id="aec8a-125">Der **reerinnerungs** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="aec8a-125">The **GetReminders** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="aec8a-126">**Headername**</span><span class="sxs-lookup"><span data-stu-id="aec8a-126">**Header name**</span></span>|<span data-ttu-id="aec8a-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="aec8a-127">**Element**</span></span>|<span data-ttu-id="aec8a-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aec8a-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aec8a-129">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="aec8a-129">**Impersonation**</span></span> <br/> |[<span data-ttu-id="aec8a-130">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="aec8a-130">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="aec8a-131">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.</span><span class="sxs-lookup"><span data-stu-id="aec8a-131">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="aec8a-132">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aec8a-132">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aec8a-133">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="aec8a-133">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="aec8a-134">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="aec8a-134">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="aec8a-135">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aec8a-135">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="aec8a-136">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aec8a-136">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aec8a-137">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="aec8a-137">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="aec8a-138">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="aec8a-138">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="aec8a-139">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="aec8a-139">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="aec8a-140">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="aec8a-140">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="aec8a-141">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="aec8a-141">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="aec8a-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="aec8a-142">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="aec8a-143">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="aec8a-143">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="aec8a-144">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="aec8a-144">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getreminders-operation-request-example"></a><span data-ttu-id="aec8a-145">Reerinnerungs-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="aec8a-145">GetReminders operation request example</span></span>

<span data-ttu-id="aec8a-146">Das folgende Beispiel einer **reerinnerungs** -Vorgangsanforderung zeigt, wie die ersten fünf Kalenderelemente abgerufen werden, die zwischen **BeginTime** und **EndTime**auftreten.</span><span class="sxs-lookup"><span data-stu-id="aec8a-146">The following example of a **GetReminders** operation request shows how to retrieve the first five calendar items that occur between the **BeginTime** and **EndTime**.</span></span>
  
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
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="aec8a-147">Der SOAP-Beispiel Anforderungstext enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aec8a-147">The example request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aec8a-148">GetReminders</span><span class="sxs-lookup"><span data-stu-id="aec8a-148">GetReminders</span></span>](getreminders.md)
    
- [<span data-ttu-id="aec8a-149">EndTime</span><span class="sxs-lookup"><span data-stu-id="aec8a-149">EndTime</span></span>](endtime-remindermessagedatatype.md)
    
- [<span data-ttu-id="aec8a-150">Reminder</span><span class="sxs-lookup"><span data-stu-id="aec8a-150">ReminderType</span></span>](remindertype.md)
    
<span data-ttu-id="aec8a-151">Der SOAP-Textkörper kann auch die folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="aec8a-151">The SOAP body can also contain the following elements:</span></span>
  
- [<span data-ttu-id="aec8a-152">BeginTime</span><span class="sxs-lookup"><span data-stu-id="aec8a-152">BeginTime</span></span>](begintime.md)
    
- [<span data-ttu-id="aec8a-153">MaxItems wird</span><span class="sxs-lookup"><span data-stu-id="aec8a-153">MaxItems</span></span>](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a><span data-ttu-id="aec8a-154">Erfolgreiche reerinnerungs-Vorgangs Antwort</span><span class="sxs-lookup"><span data-stu-id="aec8a-154">Successful GetReminders operation response</span></span>

<span data-ttu-id="aec8a-155">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Vorgangsanforderung von **reerinnerter** .</span><span class="sxs-lookup"><span data-stu-id="aec8a-155">The following example shows a successful response to a **GetReminders** operation request.</span></span> <span data-ttu-id="aec8a-156">Die Antwort enthält eine Erinnerung für das Kalenderelement "Team Besprechung" und eine Erinnerung an die Aufgabe "Besprechungsnotizen senden".</span><span class="sxs-lookup"><span data-stu-id="aec8a-156">The response contains a reminder for the "Team meeting" calendar item and a reminder for the "Task to send meeting notes" task.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aec8a-157">Die Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aec8a-157">Identifiers have been shortened to preserve readability.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="aec8a-158">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aec8a-158">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aec8a-159">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="aec8a-159">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="aec8a-160">Reminders</span><span class="sxs-lookup"><span data-stu-id="aec8a-160">Reminders</span></span>](reminders.md)
    
- [<span data-ttu-id="aec8a-161">Reminder</span><span class="sxs-lookup"><span data-stu-id="aec8a-161">Reminder</span></span>](reminder.md)
    
- [<span data-ttu-id="aec8a-162">Betreff</span><span class="sxs-lookup"><span data-stu-id="aec8a-162">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="aec8a-163">Standort</span><span class="sxs-lookup"><span data-stu-id="aec8a-163">Location</span></span>](location-remindermessagedatatype.md)
    
- [<span data-ttu-id="aec8a-164">ReminderTime</span><span class="sxs-lookup"><span data-stu-id="aec8a-164">ReminderTime</span></span>](remindertime.md)
    
- [<span data-ttu-id="aec8a-165">StartDate</span><span class="sxs-lookup"><span data-stu-id="aec8a-165">StartDate</span></span>](startdate.md)
    
- [<span data-ttu-id="aec8a-166">EndDate</span><span class="sxs-lookup"><span data-stu-id="aec8a-166">EndDate</span></span>](enddate-remindertype.md)
    
- [<span data-ttu-id="aec8a-167">ItemId</span><span class="sxs-lookup"><span data-stu-id="aec8a-167">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="aec8a-168">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="aec8a-168">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
    
- [<span data-ttu-id="aec8a-169">Reminder</span><span class="sxs-lookup"><span data-stu-id="aec8a-169">ReminderGroup</span></span>](remindergroup.md)
    
- [<span data-ttu-id="aec8a-170">UID</span><span class="sxs-lookup"><span data-stu-id="aec8a-170">UID</span></span>](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a><span data-ttu-id="aec8a-171">Reerinnerungs Operation-Fehlerantwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="aec8a-171">GetReminders operation error response example</span></span>

<span data-ttu-id="aec8a-172">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **reerinnerungs** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="aec8a-172">The following example shows an error response to a **GetReminders** operation request.</span></span> <span data-ttu-id="aec8a-173">Dies ist eine Antwort auf eine Anforderung, bei der das Enddatum vor dem Startdatum lag.</span><span class="sxs-lookup"><span data-stu-id="aec8a-173">This is a response to a request in which the end date was earlier than the start date.</span></span> 
  
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
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="aec8a-174">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="aec8a-174">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="aec8a-175">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="aec8a-175">GetRemindersResponse</span></span>](getremindersresponse.md)
    
- [<span data-ttu-id="aec8a-176">MessageText</span><span class="sxs-lookup"><span data-stu-id="aec8a-176">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="aec8a-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="aec8a-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="aec8a-178">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="aec8a-178">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="aec8a-179">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="aec8a-179">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aec8a-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec8a-180">See also</span></span>


- [<span data-ttu-id="aec8a-181">PerformReminderAction</span><span class="sxs-lookup"><span data-stu-id="aec8a-181">PerformReminderAction</span></span>](performreminderaction.md)
    

