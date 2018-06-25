---
title: Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Erfahren Sie, wie ganztägige Ereignisse zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 0547fdf0ca92ba0648caeb5de6940d90d2a8ff46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756873"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse

Erfahren Sie, wie ganztägige Ereignisse zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Ganztägige Ereignisse bieten die Möglichkeit, etwas darstellen, die für einen ganzen Tag oder mehrere Tage geschieht – beispielsweise einen Feiertag oder Urlaubstage. Ganztägige Ereignisse mit dem EWS Managed API oder EWS erstellen, ist ein Kinderspiel. [Erstellen von Terminen](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), vergleichbar mit ein paar geringfügige Änderungen ist.
  
## <a name="setting-start-and-end-times"></a>Festlegen der Start- und Endzeiten

Per Definition ganztägige Ereignisse Mitternacht für einen bestimmten Tag, und die End 24 Stunden (oder ein Vielfaches von 24 Stunden) weiter unten. Jedoch die EWS Managed API und EWS können Sie angeben, wie oft als Mitternacht beim ganztägige Ereignisse erstellen. Dies kann zu unbeabsichtigten Verhalten führen, wenn Sie nicht wissen, wie diese Zeiten auf dem Server übersetzt werden.
  
Wenn eine Anforderung empfangen wird, erstellen Sie ein neues ganztägiges Ereignis mit Mitternacht (in der [Zeitzone des Anforderung oder Termin](time-zones-and-ews-in-exchange.md)) Anfangs- und/oder Endzeit, erhalten diese Zeiten Mitternacht in der entsprechenden Zeitzone nach den folgenden Regeln angepasst:
  
- Nicht-Mitternacht Anfangszeiten werden die Mitternacht vor der angegebenen Zeit angepasst. Beispielsweise ruft 1:00 PM 6. Juni auf 00:00 Uhr am 6. Juni korrigiert.
    
- Endzeit nicht Mitternacht werden die Mitternacht nach dem angegebenen Zeitpunkt angepasst. Beispielsweise ruft 1:00 PM 6. Juni auf 00:00:00 Uhr 7. Juni korrigiert.
    
Damit das ganztägige Ereignis, das Sie erstellen immer einschließlich Start- und Endzeit Zeitpunkt steht, die Sie angeben, aber möglicherweise zusätzliche Zeit in Anspruch der Benutzer angezeigt werden sollen, die die UMSCHALTTASTE gedrückt, um Mitternacht. Da der Server die Start- und Endzeit Zeit vor Mitternacht angepasst wird, wird empfohlen, dass Sie Ihre Zeit Start- und Endzeit Mitternacht zur Vermeidung von unbeabsichtigten Änderungen an die Zeiten angeben.
  
Es ist außerdem unbedingt Zeitzonen berücksichtigt ganztägige Ereignisse erstellen. Da der Exchange Server ein Mitternacht erzwingt Start- und Endzeit in der Zeitzone des Anforderung oder einem Termin, kann das anzeigen, ganztägigen Ereignis in einem Client konfiguriert für eine andere Zeitzone unerwarteten Ergebnissen führen. Je nach den Client kann es so aussehen als ganztägiges Ereignis mit zusätzlichen Tage, die Sie wollten nicht einschließen, oder nicht angezeigt werden als ein ganztägiges Ereignis vollständig. Aus diesem Grund wird empfohlen, dass Sie bei der Erstellung von ganztägige Ereignisse des Benutzers bevorzugte Zeitzone nach Möglichkeit verwenden.
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>Erstellen Sie ein ganztägiges Ereignis mithilfe der EWS Managed API

Im folgenden Beispiel wird veranschaulicht, wie die EWS Managed API verwenden, erstellen Sie ein ganztägiges Ereignis, ab dem Datum angegeben wird, indem der Parameter _StartDate_ und, jedoch nur für die Anzahl der Tage, die durch den Parameter _NumDays_ angegeben. Beachten Sie, dass der Termin in die Zeitzone, die durch die [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegebenen erstellt wird. In diesem Beispiel wird davon ausgegangen, dass das im _Dienst_ -Parameter übergebene [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt durch gültige Werte für die [Anmeldeinformationen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) -Eigenschaften initialisiert wurde. 
  
```cs
static void CreateAllDayAppointment(ExchangeService service, DateTime startDate, int numDays)
{
    // Best practice is to set the start date to midnight
    // on the first day of the all-day event.
    DateTime startDateMidnight = startDate.Date;
    // The end date should be midnight on the first day
    // after the event.
    DateTime endDateMidnight = startDateMidnight.AddDays(numDays);
    Appointment allDayEvent = new Appointment(service);
    // Set IsAllDayEvent to true.
    allDayEvent.IsAllDayEvent = true;
    // Set other properties.
    allDayEvent.Subject = "Vacation";
    allDayEvent.LegacyFreeBusyStatus = LegacyFreeBusyStatus.OOF;
    allDayEvent.Start = startDateMidnight;
    allDayEvent.End = endDateMidnight;
    // Save the appointment.
    try
    {
        allDayEvent.Save(WellKnownFolderName.Calendar, SendInvitationsMode.SendToNone);
        Console.WriteLine("All day event created.");
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving all day event: {0}", ex.Message);
    }
}
```

## <a name="create-an-all-day-event-by-using-ews"></a>Erstellen Sie ein ganztägiges Ereignis mithilfe der Exchange-Webdienste

Das folgende Beispiel zeigt eine Anforderung EWS [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) ein ganztägiges Ereignis erstellen. Der Termin wird in der Eastern Time-Zone erstellt, wie das [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegeben. Beachten Sie, dass der Zeitteil der Werte der Elemente [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [End](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) sind beide 04:00Z, die in der Eastern Time-Zone während der Sommerzeit Mitternacht konvertiert. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Vacation</t:Subject>
          <t:Start>2014-06-09T04:00:00.000Z</t:Start>
          <t:End>2014-06-10T04:00:00.000Z</t:End>
          <t:IsAllDayEvent>true</t:IsAllDayEvent>
          <t:LegacyFreeBusyStatus>OOF</t:LegacyFreeBusyStatus>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)
    

