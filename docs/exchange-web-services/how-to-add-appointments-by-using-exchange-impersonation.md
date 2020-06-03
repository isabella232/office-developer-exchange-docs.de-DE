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
# <a name="add-appointments-by-using-exchange-impersonation"></a>Hinzufügen von Terminen mit Exchange-Identitätswechsel

In diesem Artikel erfahren Sie, wie Sie den Identitätswechsel mit dem verwaltete EWS-API oder EWS in Exchange verwenden, um Kalendern von Benutzern Termine hinzuzufügen.
  
Sie können eine Dienstanwendung erstellen, die Termine direkt in einen Exchange-Kalender einfügt, indem Sie ein Dienstkonto verwenden, für das die Rolle **ApplicationImpersonation** [aktiviert](how-to-configure-impersonation.md)ist. Wenn Sie den Identitätswechsel verwenden, fungiert die Anwendung als Benutzer; Es ist, als ob der Benutzer den Termin mithilfe eines Clients wie Outlook zum Kalender hinzugefügt hat. 
  
Beachten Sie beim Verwenden eines Identitätswechsels Folgendes:
  
- Das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.aspx) -Objekt muss an das Dienstkonto gebunden sein. Sie können das gleiche **Datei "ExchangeService** -Objekt verwenden, um die Identität mehrerer Konten zu imitieren, indem Sie die [ImpersonatedUserId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid.aspx) -Eigenschaft für jedes Konto ändern, für das Sie den Identitätswechsel durchführen möchten. 
    
- Jedes Element, das Sie in einem imitierten Konto speichern, kann nur einmal verwendet werden. Wenn Sie beispielsweise den gleichen Termin in mehreren Konten speichern möchten, müssen Sie für jedes Konto ein [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.aspx) Objekt erstellen. 
    
## <a name="prerequisites"></a>Voraussetzungen

Ihre Anwendung benötigt ein Konto, das zum Herstellen einer Verbindung mit dem Exchange-Server verwendet wird, bevor der Identitätswechsel verwendet werden kann. Es wird empfohlen, ein Dienstkonto für die Anwendung zu verwenden, der die Rolle "Anwendungsidentitätswechsel" für die Konten erteilt wurde, auf die Sie zugreift. Weitere Informationen finden Sie unter [Konfigurieren eines Identitätswechsels](how-to-configure-impersonation.md) .
  
## <a name="add-appointments-by-using-impersonation-with-the-ews-managed-api"></a>Hinzufügen von Terminen mithilfe des Identitätswechsels mit dem verwaltete EWS-API

Im folgenden Beispiel wird dem Kalender eines oder mehrerer Exchange-Konten ein Termin oder eine Besprechung hinzugefügt. Die-Methode benötigt drei Parameter.
  
-  _Dienst_ – ein **Datei "ExchangeService** -Objekt, das an das Konto der Dienstanwendung auf dem Exchange-Server gebunden ist. 
    
-  e _-Mail-Adressen – ein_ [System. List](https://msdn.microsoft.com/library/6sh2ey19.aspx) -Objekt, das eine Liste von SMTP-e-Mail-Adress Zeichenfolgen enthält. 
    
-  _Factory_ – ein Objekt, das die **IAppointmentFactory** -Schnittstelle implementiert. Diese Schnittstelle hat eine Methode, **gettermination** , die ein **Datei "ExchangeService** -Objekt als Parameter akzeptiert und ein **Termin** Objekt zurückgibt. Die **IAppointmentFactory** -Schnittstelle ist [IAppointmentFactory-Schnittstelle](#bk_IAppointmentFactory)definiert.
    
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

Beim Speichern des Termins überprüft der Code, um zu bestimmen, ob Teilnehmer der [RequiredAttendees](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.requiredattendees.aspx) -Eigenschaft hinzugefügt wurden. Wenn dies der Fall ist, wird die [Termin. Save](https://msdn.microsoft.com/library/dd635394.aspx) -Methode mit dem [SendToAllAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Enumerationswert aufgerufen, sodass die Teilnehmer Besprechungsanfragen erhalten; Andernfalls wird die **Termin. Save** -Methode mit dem [SendToNone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode.aspx) -Aufzählungswert aufgerufen, sodass der Termin im Kalender des imitierten Benutzers gespeichert wird, wobei die Eigenschaft [Termin. ismeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.ismeeting.aspx) auf **false**festgelegt ist.
  
### <a name="iappointmentfactory-interface"></a>IAppointmentFactory-Schnittstelle
<a name="bk_IAppointmentFactory"> </a>

Da Sie jedes Mal ein neues **Termin** Objekt benötigen, wenn Sie einen Termin für den Kalender eines imitierten Benutzers speichern möchten, abstrahiert die **IAppointmentFactory** -Schnittstelle das Objekt, mit dem jedes **Termin** Objekt aufgefüllt wird. Diese Version ist eine einfache Schnittstelle, die nur eine Methode, **gettermine**, enthält, die ein **Datei "ExchangeService** -Objekt als Parameter verwendet und ein neues **Termin** Objekt zurückgibt, das an dieses **Datei" ExchangeService** -Objekt gebunden ist. 
  
```cs
interface IAppointmentFactory
{
  Appointment GetAppointment(ExchangeService service);
}
```

Das folgende **AppointmentFactory** -Klassen Beispiel zeigt eine Implementierung der **IAppointmentFactory** -Schnittstelle, die einen einfachen Termin zurückgibt, der drei Tage ab jetzt auftritt. Wenn Sie die Kommentar `appointment.RequiredAttendees.Add` Zeilen entfernen, gibt die **gettermine** -Methode eine Besprechung zurück, und die in dieser Verbindung angegebene e-Mail-Adresse erhält eine Besprechungsanfrage, wobei der imitierte Benutzer als Organisator aufgeführt wird. 
  
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

## <a name="add-appointments-by-using-impersonation-with-ews"></a>Hinzufügen von Terminen mithilfe des Identitätswechsels mit EWS

Mit EWS können Sie die Anwendung verwenden, um einem Kalender im Auftrag des Besitzers des Kalenders Elemente hinzuzufügen. In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs einen Termin zum Kalender eines imitierten Kontos hinzufügen. 
  
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

Beachten Sie, dass es sich nicht um das Hinzufügen des **ExchangeImpersonation** -Elements im SOAP-Header handelt, um das Konto anzugeben, von dem die Identität angenommen wird, sondern dieselbe XML-Anforderung, die zum Erstellen eines Termins verwendet wird, ohne den Identitätswechsel zu verwenden. 
  
Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird. 
  
> [!NOTE]
> Die Attribute **ItemID** und **ChangeKey** werden zur Lesbarkeit gekürzt. 
  
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

Auch dies ist derselbe XML-Code, der zurückgegeben wird, wenn Sie den **CreateItem** -Vorgang ohne Verwendung des Identitätswechsels verwenden. 
  
## <a name="see-also"></a>Siehe auch


- [Identitätswechsel und EWS in Exchange](impersonation-and-ews-in-exchange.md)
    
- [ApplicationImpersonation-Rolle](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)
    
- [Konfigurieren eines Identitätswechsels](how-to-configure-impersonation.md)
    
- [Identifizieren des Kontos für Identitätswechsel](how-to-identify-the-account-to-impersonate.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [CreateItem-Vorgang (Kalenderelement)](../web-service-reference/createitem-operation-calendar-item.md)
    
- [Datei "ExchangeService. ImpersonatedUserId-Eigenschaft](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice.impersonateduserid?view=exchange-ews-api)
    

