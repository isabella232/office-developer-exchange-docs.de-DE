---
title: Hinzufügen von Terminen mit Exchange-Identitätswechsel
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: In diesem Artikel erfahren Sie, wie Sie den Identitätswechsel mit dem verwaltete EWS-API oder EWS in Exchange verwenden, um Kalendern von Benutzern Termine hinzuzufügen.
localization_priority: Priority
ms.openlocfilehash: b1473d72113f8cc07d05364a4d87fedf23c7351d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455331"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a><span data-ttu-id="9f78b-103">Hinzufügen von Terminen mit Exchange-Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="9f78b-103">Add appointments by using Exchange impersonation</span></span>

<span data-ttu-id="9f78b-104">In diesem Artikel erfahren Sie, wie Sie den Identitätswechsel mit dem verwaltete EWS-API oder EWS in Exchange verwenden, um Kalendern von Benutzern Termine hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f78b-104">Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.</span></span>
  
<span data-ttu-id="9f78b-105">Sie können eine Dienstanwendung erstellen, die Termine direkt in einen Exchange-Kalender einfügt, indem Sie ein Dienstkonto verwenden, für das die Rolle **ApplicationImpersonation** [aktiviert](how-to-configure-impersonation.md)ist.</span><span class="sxs-lookup"><span data-stu-id="9f78b-105">You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **ApplicationImpersonation** [role enabled](how-to-configure-impersonation.md).</span></span> <span data-ttu-id="9f78b-106">Wenn Sie den Identitätswechsel verwenden, fungiert die Anwendung als Benutzer; Es ist, als ob der Benutzer den Termin mithilfe eines Clients wie Outlook zum Kalender hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="9f78b-106">When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.</span></span> 
  
<span data-ttu-id="9f78b-107">Beachten Sie beim Verwenden eines Identitätswechsels Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f78b-107">When you are using impersonation, keep in mind the following:</span></span>
  
- <span data-ttu-id="9f78b-108">Das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) -Objekt muss an das Dienstkonto gebunden sein.</span><span class="sxs-lookup"><span data-stu-id="9f78b-108">Your [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account.</span></span> <span data-ttu-id="9f78b-109">Sie können das gleiche **Datei "ExchangeService** -Objekt verwenden, um die Identität mehrerer Konten zu imitieren, indem Sie die [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) -Eigenschaft für jedes Konto ändern, für das Sie den Identitätswechsel durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="9f78b-109">You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.</span></span> 
    
- <span data-ttu-id="9f78b-110">Jedes Element, das Sie in einem imitierten Konto speichern, kann nur einmal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f78b-110">Any item that you save to an impersonated account can only be used once.</span></span> <span data-ttu-id="9f78b-111">Wenn Sie beispielsweise den gleichen Termin in mehreren Konten speichern möchten, müssen Sie für jedes Konto ein [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f78b-111">If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.</span></span> 
    
## <a name="prerequisites"></a><span data-ttu-id="9f78b-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9f78b-112">Prerequisites</span></span>

<span data-ttu-id="9f78b-113">Ihre Anwendung benötigt ein Konto, das zum Herstellen einer Verbindung mit dem Exchange-Server verwendet wird, bevor der Identitätswechsel verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9f78b-113">Your application needs an account to use to connect to the Exchange server before it can use impersonation.</span></span> <span data-ttu-id="9f78b-114">Es wird empfohlen, ein Dienstkonto für die Anwendung zu verwenden, der die Rolle "Anwendungsidentitätswechsel" für die Konten erteilt wurde, auf die Sie zugreift.</span><span class="sxs-lookup"><span data-stu-id="9f78b-114">We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing.</span></span> <span data-ttu-id="9f78b-115">Weitere Informationen finden Sie unter [Konfigurieren eines Identitätswechsels](how-to-configure-impersonation.md) .</span><span class="sxs-lookup"><span data-stu-id="9f78b-115">For more information, see [Configure impersonation](how-to-configure-impersonation.md)</span></span>
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a><span data-ttu-id="9f78b-116">Hinzufügen von Terminen mithilfe des Identitätswechsels mit dem verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="9f78b-116">Add appointments by using impersonation with the EWS Managed API</span></span>

<span data-ttu-id="9f78b-117">Im folgenden Beispiel wird dem Kalender eines oder mehrerer Exchange-Konten ein Termin oder eine Besprechung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9f78b-117">The following example adds an appointment or meeting to the calendar of one or more Exchange accounts.</span></span> <span data-ttu-id="9f78b-118">Die-Methode benötigt drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f78b-118">The method takes three parameters.</span></span>
  
-  <span data-ttu-id="9f78b-119">_Dienst_ – ein **Datei "ExchangeService** -Objekt, das an das Konto der Dienstanwendung auf dem Exchange-Server gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="9f78b-119">_service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.</span></span> 
    
-  <span data-ttu-id="9f78b-120">e _-Mail-Adressen – ein_ [System. List](https://msdn.microsoft.com/library/6sh2ey19.aspx) -Objekt, das eine Liste von SMTP-e-Mail-Adress Zeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="9f78b-120">_emailAddresses_ — A [System.List](https://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.</span></span> 
    
-  <span data-ttu-id="9f78b-121">_Factory_ – ein Objekt, das die **IAppointmentFactory** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="9f78b-121">_factory_ — An object that implements the **IAppointmentFactory** interface.</span></span> <span data-ttu-id="9f78b-122">Diese Schnittstelle hat eine Methode, **gettermination** , die ein **Datei "ExchangeService** -Objekt als Parameter akzeptiert und ein **Termin** Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9f78b-122">This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object.</span></span> <span data-ttu-id="9f78b-123">Die **IAppointmentFactory** -Schnittstelle ist [IAppointmentFactory-Schnittstelle](#bk_IAppointmentFactory)definiert.</span><span class="sxs-lookup"><span data-stu-id="9f78b-123">The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).</span></span>
    
```cs
private static void CreateAppointments(ExchangeService service, List<string> emailAddresses, IAppointmentFactory factory)
{
  // Loop through the list of email addresses to add the appointment.
  foreach (var emailAddress in emailAddresses)
  {
    Console.WriteLine(string.Format("  Placing appointment in calendar for {0}.", emailAddress));
    // Set the email address of the account to get the appointment.
    service.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, emailAddress);
    // Get the appointment to add.
    Appointment appointment = factory.GetAppointment(service);
    // Save the appointment.
    try
    {
      if (appointment.RequiredAttendees.Count > 0)
      {
        // The appointment has attendees so send them the meeting request.
        appointment.Save(SendInvitationsMode.SendToAllAndSaveCopy);
      }
      else
      {
        // The appointment does not have attendees, so just save to calendar.
        appointment.Save(SendInvitationsMode.SendToNone);
      }
    }
    catch (ServiceResponseException ex)
    {
      Console.WriteLine(string.Format("Could not create appointment for {0}", emailAddress));
      Console.WriteLine(ex.Message);
    }
  }
}
```

<span data-ttu-id="9f78b-124">Beim Speichern des Termins überprüft der Code, um zu bestimmen, ob Teilnehmer der [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) -Eigenschaft hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f78b-124">When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property.</span></span> <span data-ttu-id="9f78b-125">Wenn dies der Fall ist, wird die [Termin. Save](https://msdn.microsoft.com/library/dd635394.aspx) -Methode mit dem [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, sodass die Teilnehmer Besprechungsanfragen erhalten; Andernfalls wird die **Termin. Save** -Methode mit dem [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Aufzählungswert aufgerufen, sodass der Termin im Kalender des imitierten Benutzers gespeichert wird, wobei die Eigenschaft [Termin. ismeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) auf **false**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f78b-125">If they have, the [Appointment.Save](https://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.</span></span>
  
### <a name="iappointmentfactory-interface"></a><span data-ttu-id="9f78b-126">IAppointmentFactory-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9f78b-126">IAppointmentFactory interface</span></span>
<span data-ttu-id="9f78b-127"><a name="bk_IAppointmentFactory"> </a></span><span class="sxs-lookup"><span data-stu-id="9f78b-127"><a name="bk_IAppointmentFactory"> </a></span></span>

<span data-ttu-id="9f78b-128">Da Sie jedes Mal ein neues **Termin** Objekt benötigen, wenn Sie einen Termin für den Kalender eines imitierten Benutzers speichern möchten, abstrahiert die **IAppointmentFactory** -Schnittstelle das Objekt, mit dem jedes **Termin** Objekt aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="9f78b-128">Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object.</span></span> <span data-ttu-id="9f78b-129">Diese Version ist eine einfache Schnittstelle, die nur eine Methode, **gettermine**, enthält, die ein **Datei "ExchangeService** -Objekt als Parameter verwendet und ein neues **Termin** Objekt zurückgibt, das an dieses **Datei" ExchangeService** -Objekt gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="9f78b-129">This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.</span></span> 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

<span data-ttu-id="9f78b-130">Das folgende **AppointmentFactory** -Klassen Beispiel zeigt eine Implementierung der **IAppointmentFactory** -Schnittstelle, die einen einfachen Termin zurückgibt, der drei Tage ab jetzt auftritt.</span><span class="sxs-lookup"><span data-stu-id="9f78b-130">The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now.</span></span> <span data-ttu-id="9f78b-131">Wenn Sie die Kommentar `appointment.RequiredAttendees.Add` Zeilen entfernen, gibt die **gettermine** -Methode eine Besprechung zurück, und die in dieser Verbindung angegebene e-Mail-Adresse erhält eine Besprechungsanfrage, wobei der imitierte Benutzer als Organisator aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f78b-131">If you uncomment the  `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.</span></span> 
  
```cs
class AppointmentFactory : IAppointmentFactory
{
  public Appointment GetAppointment(ExchangeService service)
  {
    // First create the appointment to add.
    Appointment appointment = new Appointment(service);
    // Set the properties on the appointment.
    appointment.Subject = "Tennis lesson";
    appointment.Body = "Focus on backhand this week.";
    appointment.Start = DateTime.Now.AddDays(3);
    appointment.End = appointment.Start.AddHours(1);
    appointment.Location = "Tennis club";
    // appointment.RequiredAttendees.Add(new Attendee("sonyaf@contoso1000.onmicrosoft.com"));
    return appointment;
  }
}

```

## <a name="add-appointments-by-using-impersonation-with-ews"></a><span data-ttu-id="9f78b-132">Hinzufügen von Terminen mithilfe des Identitätswechsels mit EWS</span><span class="sxs-lookup"><span data-stu-id="9f78b-132">Add appointments by using impersonation with EWS</span></span>

<span data-ttu-id="9f78b-133">Mit EWS können Sie die Anwendung verwenden, um einem Kalender im Auftrag des Besitzers des Kalenders Elemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f78b-133">EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner.</span></span> <span data-ttu-id="9f78b-134">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs einen Termin zum Kalender eines imitierten Kontos hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f78b-134">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="9f78b-135">Beachten Sie, dass es sich nicht um das Hinzufügen des **ExchangeImpersonation** -Elements im SOAP-Header handelt, um das Konto anzugeben, von dem die Identität angenommen wird, sondern dieselbe XML-Anforderung, die zum Erstellen eines Termins verwendet wird, ohne den Identitätswechsel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f78b-135">Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.</span></span> 
  
<span data-ttu-id="9f78b-136">Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f78b-136">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f78b-137">Die Attribute **ItemID** und **ChangeKey** werden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="9f78b-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="9f78b-138">Auch dies ist derselbe XML-Code, der zurückgegeben wird, wenn Sie den **CreateItem** -Vorgang ohne Verwendung des Identitätswechsels verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f78b-138">Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f78b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f78b-139">See also</span></span>


- [<span data-ttu-id="9f78b-140">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9f78b-140">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="9f78b-141">ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="9f78b-141">ApplicationImpersonation role</span></span>](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="9f78b-142">Konfigurieren eines Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="9f78b-142">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="9f78b-143">Identifizieren des Kontos für Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="9f78b-143">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="9f78b-144">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9f78b-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="9f78b-145">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="9f78b-145">CreateItem operation (calendar item)</span></span>](../web-service-reference/createitem-operation-calendar-item.md)
    
- [<span data-ttu-id="9f78b-146">Datei "ExchangeService. ImpersonatedUserId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f78b-146">ExchangeService.ImpersonatedUserId property</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

