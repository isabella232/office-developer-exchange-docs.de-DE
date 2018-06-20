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
# <a name="add-appointments-by-using-exchange-impersonation"></a>Hinzufügen von Terminen mithilfe der Exchange-Identitätswechsel

Informationen Sie zur Verwendung des Identitätswechsels mit dem EWS Managed API oder EWS in Exchange Benutzerkalendern Termine hinzu.
  
Sie können eine dienstanwendung erstellen, die Terminen direkt in einen Exchange-Kalender mithilfe eines Dienstkontos, das der **AppplicationImpersonation**[-Rolle aktiviert](how-to-configure-impersonation.md)wurde eingefügt. Wenn Sie Identitätswechsel verwenden, fungiert wie der Benutzer die Anwendung; Es ist, als würde der Benutzer den Termin mithilfe eines Clients wie Outlook im Kalender hinzugefügt. 
  
Wenn Sie Identitätswechsel verwenden, beachten Sie Folgendes:
  
- Das Dienstkonto muss Ihre [ExchangeService](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) -Objekt gebunden sein. Das gleiche **ExchangeService** -Objekt können Sie Identitätswechsel für mehrere Konten durch Ändern der [ImpersonatedUserId](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) -Eigenschaft für jedes Konto, das Sie imitieren möchten. 
    
- Jedes Element, das Sie in einem Konto mit angenommener speichern kann nur einmal verwendet werden. Wenn Sie den gleichen Termin in mehrere Konten speichern möchten, müssen Sie beispielsweise ein [Termin](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) -Objekt für jedes Konto erstellen. 
    
## <a name="prerequisites"></a>Voraussetzungen

Die Anwendung benötigt ein Konto mit an den Exchange-Server hergestellt werden soll, bevor es Identitätswechsel verwenden kann. Es wird empfohlen, dass Sie ein Dienstkonto für die Anwendung verwenden, die Anwendung Identitätswechselrolle für die Konten zugewiesen wurde, die auf sie zugreifen. Weitere Informationen finden Sie unter [Configure Identitätswechsel](how-to-configure-impersonation.md)
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>Hinzufügen von Terminen durch Verwenden des Identitätswechsels mit der EWS Managed API

Im folgende Beispiel werden im Kalender von einem oder mehreren Exchange-Konten eines Termins oder einer Besprechung hinzugefügt. Die Methode hat drei Parameter.
  
-  _Dienst_ – ein **ExchangeService** -Objekt gebunden Konto die Service-Anwendung auf dem Exchange-Server. 
    
-  _EmailAddresses_ – ein [System.List](http://msdn.microsoft.com/library/6sh2ey19.aspx) -Objekt, das eine Liste der SMTP-e-Mail-Adresszeichenfolgen enthält. 
    
-  _Factory_ – ein Objekt, das die **IAppointmentFactory** -Schnittstelle implementiert wird. Diese Schnittstelle verfügt über eine Methode, **GetAppointment** , die ein **ExchangeService** -Objekt als Parameter akzeptiert und gibt ein **Termin** -Objekt zurück. Die **IAppointmentFactory** -Schnittstelle definiert ist [IAppointmentFactory-Schnittstelle](#bk_IAppointmentFactory).
    
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

Beim Speichern des Termins überprüft der Code, um zu bestimmen, ob die Eigenschaft ["RequiredAttendees"](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) alle Teilnehmer hinzugefügt wurden. Wenn sie aufweisen, wird die [Appointment.Save](http://msdn.microsoft.com/library/dd635394.aspx) -Methode mit dem [SendToAllAndSaveCopy](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, damit die Teilnehmer Besprechungsanfragen empfangen; Andernfalls wird die **Appointment.Save** -Methode mit dem [SendToNone](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, sodass der Termin in den angenommener Kalender des Benutzers, mit der [Appointment.IsMeeting](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) -Eigenschaft auf **false**festgelegt gespeichert wird.
  
### <a name="iappointmentfactory-interface"></a>IAppointmentFactory-Schnittstelle
<a name="bk_IAppointmentFactory"> </a>

Da Sie ein neues Objekt **Termin** jedes Mal, die Sie einen Termin im Kalender des Benutzers ein angenommener speichern möchten benötigen, abstrahiert die Schnittstelle **IAppointmentFactory** das Objekt zum Auffüllen der einzelnen **Appointment** -Objekts verwendet wird. Diese Version ist eine einfache Schnittstelle, die nur eine Methode, **GetAppointment**, enthält, die ein **ExchangeService** -Objekt als Parameter akzeptiert und gibt ein neues **Appointment** -Objekt auf dieses Objekt **ExchangeService** gebunden. 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

Im folgenden Beispiel **AppointmentFactory** -Klasse wird gezeigt, dass eine Implementierung der **IAppointmentFactory** -Schnittstelle, die einem einfachen Termin zurückgibt drei Tage von jetzt auftritt. Auskommentieren der `appointment.RequiredAttendees.Add` Zeile, einer Besprechung und die e-Mail-Adresse angegeben, dass Zeile eine Besprechungsanfrage mit der angenommener als Organisator aufgeführte Benutzer erhält, wird die **GetAppointment** -Methode zurück. 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a>Hinzufügen von Terminen durch Verwenden des Identitätswechsels mit Exchange-Webdienste

EWS ermöglicht Anwendung Identitätswechsel verwenden, Hinzufügen von Elementen zu einem Kalender in Auftrag Besitzer des Kalenders. Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um einen Termin im Kalender ein angenommener Konto hinzufügen. 
  
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

Beachten Sie, dass als das Hinzufügen des Elements **"ExchangeImpersonation"** im SOAP-Header, um das Konto anzugeben, das wir imitiert wird, ist dies der gleichen XML-Anforderung verwendet, um einen Termin ohne Verwenden des Identitätswechsels zu erstellen. 
  
Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemId** und **ChangeKey** werden zur besseren Lesbarkeit gekürzt. 
  
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

Dies ist wiederum den gleichen XML-Code, die zurückgegeben wird, wenn Sie die **CreateItem** -Operation verwenden, ohne das Verwenden des Identitätswechsels. 
  
## <a name="see-also"></a>Siehe auch


- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [ApplicationImpersonation-Rolle](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)
    
- [Konfigurieren des Identitätswechsels](how-to-configure-impersonation.md)
    
- [Identifizieren Sie das Konto Identität](how-to-identify-the-account-to-impersonate.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [CreateItem-Vorgang (Kalenderelement)](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)
    
- [ExchangeService.ImpersonatedUserId-Eigenschaft](http://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx.aspx)
    

