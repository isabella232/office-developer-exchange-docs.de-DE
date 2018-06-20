---
title: Hinzufügen von Terminen mithilfe der Exchange-Identitätswechsel
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78d5e51b-900f-4302-b9a8-fdc9aa4b65a5
description: Informationen Sie zur Verwendung des Identitätswechsels mit dem EWS Managed API oder EWS in Exchange Benutzerkalendern Termine hinzu.
ms.openlocfilehash: fe737658b88aca66d8b4c2860245db000888ba17
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756881"
---
# <a name="add-appointments-by-using-exchange-impersonation"></a><span data-ttu-id="0b92b-103">Hinzufügen von Terminen mithilfe der Exchange-Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="0b92b-103">Add appointments by using Exchange impersonation</span></span>

<span data-ttu-id="0b92b-104">Informationen Sie zur Verwendung des Identitätswechsels mit dem EWS Managed API oder EWS in Exchange Benutzerkalendern Termine hinzu.</span><span class="sxs-lookup"><span data-stu-id="0b92b-104">Learn how to use impersonation with the EWS Managed API or EWS in Exchange to add appointments to users' calendars.</span></span>
  
<span data-ttu-id="0b92b-105">Sie können eine dienstanwendung erstellen, die Terminen direkt in einen Exchange-Kalender mithilfe eines Dienstkontos, das der **AppplicationImpersonation**[-Rolle aktiviert](how-to-configure-impersonation.md)wurde eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0b92b-105">You can create a service application that inserts appointments directly into an Exchange calendar by using a service account that has the **AppplicationImpersonation**[role enabled](how-to-configure-impersonation.md).</span></span> <span data-ttu-id="0b92b-106">Wenn Sie Identitätswechsel verwenden, fungiert wie der Benutzer die Anwendung; Es ist, als würde der Benutzer den Termin mithilfe eines Clients wie Outlook im Kalender hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b92b-106">When you use impersonation, the application is acting as the user; it's as if the user added the appointment to the calendar by using a client such as Outlook.</span></span> 
  
<span data-ttu-id="0b92b-107">Wenn Sie Identitätswechsel verwenden, beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0b92b-107">When you are using impersonation, keep in mind the following:</span></span>
  
- <span data-ttu-id="0b92b-108">Das Dienstkonto muss Ihre [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) -Objekt gebunden sein.</span><span class="sxs-lookup"><span data-stu-id="0b92b-108">Your [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) object must be bound to the service account.</span></span> <span data-ttu-id="0b92b-109">Das gleiche **ExchangeService** -Objekt können Sie Identitätswechsel für mehrere Konten durch Ändern der [ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) -Eigenschaft für jedes Konto, das Sie imitieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0b92b-109">You can use the same **ExchangeService** object to impersonate multiple accounts by changing the [ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) property for each account that you want to impersonate.</span></span> 
    
- <span data-ttu-id="0b92b-110">Jedes Element, das Sie in einem Konto mit angenommener speichern kann nur einmal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b92b-110">Any item that you save to an impersonated account can only be used once.</span></span> <span data-ttu-id="0b92b-111">Wenn Sie den gleichen Termin in mehrere Konten speichern möchten, müssen Sie beispielsweise ein [Termin](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) -Objekt für jedes Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b92b-111">If you want to save the same appointment in multiple accounts, for example, you have to create an [Appointment](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) object for each account.</span></span> 
    
## <a name="prerequisites"></a><span data-ttu-id="0b92b-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0b92b-112">Prerequisites</span></span>

<span data-ttu-id="0b92b-113">Die Anwendung benötigt ein Konto mit an den Exchange-Server hergestellt werden soll, bevor es Identitätswechsel verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="0b92b-113">Your application needs an account to use to connect to the Exchange server before it can use impersonation.</span></span> <span data-ttu-id="0b92b-114">Es wird empfohlen, dass Sie ein Dienstkonto für die Anwendung verwenden, die Anwendung Identitätswechselrolle für die Konten zugewiesen wurde, die auf sie zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0b92b-114">We suggest that you use a service account for the application that has been granted the Application Impersonation role for the accounts that it will be accessing.</span></span> <span data-ttu-id="0b92b-115">Weitere Informationen finden Sie unter [Configure Identitätswechsel](how-to-configure-impersonation.md)</span><span class="sxs-lookup"><span data-stu-id="0b92b-115">For more information, see [Configure impersonation](how-to-configure-impersonation.md)</span></span>
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a><span data-ttu-id="0b92b-116">Hinzufügen von Terminen durch Verwenden des Identitätswechsels mit der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="0b92b-116">Add appointments by using impersonation with the EWS Managed API</span></span>

<span data-ttu-id="0b92b-117">Im folgende Beispiel werden im Kalender von einem oder mehreren Exchange-Konten eines Termins oder einer Besprechung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0b92b-117">The following example adds an appointment or meeting to the calendar of one or more Exchange accounts.</span></span> <span data-ttu-id="0b92b-118">Die Methode hat drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="0b92b-118">The method takes three parameters.</span></span>
  
-  <span data-ttu-id="0b92b-119">_Dienst_ – ein **ExchangeService** -Objekt gebunden Konto die Service-Anwendung auf dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="0b92b-119">_service_ — An **ExchangeService** object bound to the service application's account on the Exchange server.</span></span> 
    
-  <span data-ttu-id="0b92b-120">_EmailAddresses_ – ein [System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx) -Objekt, das eine Liste der SMTP-e-Mail-Adresszeichenfolgen enthält.</span><span class="sxs-lookup"><span data-stu-id="0b92b-120">_emailAddresses_ — A [System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx) object containing a list of SMTP email address strings.</span></span> 
    
-  <span data-ttu-id="0b92b-121">_Factory_ – ein Objekt, das die **IAppointmentFactory** -Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b92b-121">_factory_ — An object that implements the **IAppointmentFactory** interface.</span></span> <span data-ttu-id="0b92b-122">Diese Schnittstelle verfügt über eine Methode, **GetAppointment** , die ein **ExchangeService** -Objekt als Parameter akzeptiert und gibt ein **Termin** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0b92b-122">This interface has one method, **GetAppointment** that takes an **ExchangeService** object as a parameter and returns an **Appointment** object.</span></span> <span data-ttu-id="0b92b-123">Die **IAppointmentFactory** -Schnittstelle definiert ist [IAppointmentFactory-Schnittstelle](#bk_IAppointmentFactory).</span><span class="sxs-lookup"><span data-stu-id="0b92b-123">The **IAppointmentFactory** interface is defined [IAppointmentFactory interface](#bk_IAppointmentFactory).</span></span>
    
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

<span data-ttu-id="0b92b-124">Beim Speichern des Termins überprüft der Code, um zu bestimmen, ob die Eigenschaft ["RequiredAttendees"](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) alle Teilnehmer hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0b92b-124">When saving the appointment, the code checks to determine whether any attendees have been added to the [RequiredAttendees](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) property.</span></span> <span data-ttu-id="0b92b-125">Wenn sie aufweisen, wird die [Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx) -Methode mit dem [SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, damit die Teilnehmer Besprechungsanfragen empfangen; Andernfalls wird die **Appointment.Save** -Methode mit dem [SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, sodass der Termin in den angenommener Kalender des Benutzers, mit der [Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) -Eigenschaft auf **false**festgelegt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0b92b-125">If they have, the [Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx) method is called with the [SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the attendees receive meeting requests; otherwise, the **Appointment.Save** method is called with the [SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) enumeration value so that the appointment is saved into the impersonated user's calendar with the [Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) property set to **false**.</span></span>
  
### <a name="iappointmentfactory-interface"></a><span data-ttu-id="0b92b-126">IAppointmentFactory-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0b92b-126">IAppointmentFactory interface</span></span>
<span data-ttu-id="0b92b-127"><a name="bk_IAppointmentFactory"> </a></span><span class="sxs-lookup"><span data-stu-id="0b92b-127"></span></span>

<span data-ttu-id="0b92b-128">Da Sie ein neues Objekt **Termin** jedes Mal, die Sie einen Termin im Kalender des Benutzers ein angenommener speichern möchten benötigen, abstrahiert die Schnittstelle **IAppointmentFactory** das Objekt zum Auffüllen der einzelnen **Appointment** -Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b92b-128">Because you need a new **Appointment** object each time that you want to save an appointment on an impersonated user's calendar, the **IAppointmentFactory** interface abstracts the object used to populate each **Appointment** object.</span></span> <span data-ttu-id="0b92b-129">Diese Version ist eine einfache Schnittstelle, die nur eine Methode, **GetAppointment**, enthält, die ein **ExchangeService** -Objekt als Parameter akzeptiert und gibt ein neues **Appointment** -Objekt auf dieses Objekt **ExchangeService** gebunden.</span><span class="sxs-lookup"><span data-stu-id="0b92b-129">This version is a simple interface that contains only one method, **GetAppointment**, that takes an **ExchangeService** object as a parameter and returns a new **Appointment** object bound to that **ExchangeService** object.</span></span> 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

<span data-ttu-id="0b92b-130">Im folgenden Beispiel **AppointmentFactory** -Klasse wird gezeigt, dass eine Implementierung der **IAppointmentFactory** -Schnittstelle, die einem einfachen Termin zurückgibt drei Tage von jetzt auftritt.</span><span class="sxs-lookup"><span data-stu-id="0b92b-130">The following **AppointmentFactory** class example shows an implementation of the **IAppointmentFactory** interface that returns a simple appointment that occurs three days from now.</span></span> <span data-ttu-id="0b92b-131">Auskommentieren der `appointment.RequiredAttendees.Add` Zeile, einer Besprechung und die e-Mail-Adresse angegeben, dass Zeile eine Besprechungsanfrage mit der angenommener als Organisator aufgeführte Benutzer erhält, wird die **GetAppointment** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="0b92b-131">If you uncomment the  `appointment.RequiredAttendees.Add` line, the **GetAppointment** method will return a meeting and the email address specified in that line will receive a meeting request with the impersonated user listed as the organizer.</span></span> 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a><span data-ttu-id="0b92b-132">Hinzufügen von Terminen durch Verwenden des Identitätswechsels mit Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="0b92b-132">Add appointments by using impersonation with EWS</span></span>

<span data-ttu-id="0b92b-133">EWS ermöglicht Anwendung Identitätswechsel verwenden, Hinzufügen von Elementen zu einem Kalender in Auftrag Besitzer des Kalenders.</span><span class="sxs-lookup"><span data-stu-id="0b92b-133">EWS enables you application to use impersonation to add items to a calendar on behalf the calendar's owner.</span></span> <span data-ttu-id="0b92b-134">Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um einen Termin im Kalender ein angenommener Konto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0b92b-134">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to add an appointment to the calendar of an impersonated account.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="0b92b-135">Beachten Sie, dass als das Hinzufügen des Elements **"ExchangeImpersonation"** im SOAP-Header, um das Konto anzugeben, das wir imitiert wird, ist dies der gleichen XML-Anforderung verwendet, um einen Termin ohne Verwenden des Identitätswechsels zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b92b-135">Note that other than the addition of the **ExchangeImpersonation** element in the SOAP header to specify the account that we are impersonating, this is the same XML request used to create an appointment without using impersonation.</span></span> 
  
<span data-ttu-id="0b92b-136">Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0b92b-136">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0b92b-137">Die Attribute **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="0b92b-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="0b92b-138">Dies ist wiederum den gleichen XML-Code, die zurückgegeben wird, wenn Sie die **CreateItem** -Operation verwenden, ohne das Verwenden des Identitätswechsels.</span><span class="sxs-lookup"><span data-stu-id="0b92b-138">Again, this is the same XML that is returned when you use the **CreateItem** operation without using impersonation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b92b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b92b-139">See also</span></span>


- [<span data-ttu-id="0b92b-140">Identitätswechsel und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0b92b-140">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
    
- [<span data-ttu-id="0b92b-141">ApplicationImpersonation-Rolle</span><span class="sxs-lookup"><span data-stu-id="0b92b-141">ApplicationImpersonation role</span></span>](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)
    
- [<span data-ttu-id="0b92b-142">Konfigurieren des Identitätswechsels</span><span class="sxs-lookup"><span data-stu-id="0b92b-142">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="0b92b-143">Identifizieren Sie das Konto Identität</span><span class="sxs-lookup"><span data-stu-id="0b92b-143">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="0b92b-144">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="0b92b-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="0b92b-145">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="0b92b-145">CreateItem operation (calendar item)</span></span>](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)
    
- [<span data-ttu-id="0b92b-146">ExchangeService.ImpersonatedUserId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b92b-146">ExchangeService.ImpersonatedUserId property</span></span>](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx.aspx)
    

