---
title: Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Informationen zum Erstellen von ganztägigen Ereignissen mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 6be638c17cc0e0c86fa6b4217169aa7259dfd4aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456864"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange

Informationen zum Erstellen von ganztägigen Ereignissen mithilfe der verwaltete EWS-API oder EWS in Exchange.
  
Ganztägige Ereignisse bieten eine Möglichkeit, etwas darzustellen, das für einen ganzen Tag oder mehrere Tage stattfindet (beispielsweise einen Feiertag oder Urlaubstage). Das Erstellen von ganztägigen Ereignissen mit dem verwaltete EWS-API oder EWS ist ein Kinderspiel. Es ist genau wie das [Erstellen von Terminen](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), aber mit ein paar kleinen Änderungen.
  
## <a name="setting-start-and-end-times"></a>Festlegen der Anfangs-und Endzeiten

Per Definition beginnen ganztägige Ereignisse an einem bestimmten Tag um Mitternacht und enden später 24 Stunden (oder ein Vielfaches von 24 Stunden). Mit dem verwaltete EWS-API und EWS können Sie jedoch beim Erstellen aller Day-Ereignisse andere Zeiten als Mitternacht angeben. Dies kann zu unerwünschtem Verhalten führen, wenn Sie nicht wissen, wie diese Zeiten auf dem Server übersetzt werden.
  
Wenn eine Anforderung empfangen wird, um ein Neues ganztägiges Ereignis zu erstellen, das nicht Mitternacht (in der Zeitzone der [Anforderung oder des Termins](time-zones-and-ews-in-exchange.md)) beginnt und/oder endet, werden diese Zeiten entsprechend den folgenden Regeln auf Mitternacht in der entsprechenden Zeitzone angepasst:
  
- Startzeiten außerhalb der Mitternachtszeit werden vor der angegebenen Uhrzeit auf Mitternacht angepasst. Beispielsweise wird 1:00 Uhr am 6. Juni auf 12:00 Uhr am 6. Juni angepasst.
    
- Endzeiten von nicht-Mitternacht werden nach der angegebenen Uhrzeit auf Mitternacht angepasst. Beispielsweise wird 1:00 Uhr am 6. Juni auf 12:00 Uhr am 7. Juni angepasst.
    
Das ganztägige Ereignis, das Sie erstellen, ist also immer die Start-und Endzeit, die Sie angeben, aber möglicherweise zusätzliche Zeit im Kalender des Benutzers aufgrund der Verschiebung bis Mitternacht beansprucht. Da der Server die Start-und Endzeit auf Mitternacht anpassen wird, wird empfohlen, dass Sie die Start-und Endzeit um Mitternacht angeben, um unbeabsichtigte Änderungen an den Zeiten zu vermeiden.
  
Bei der Erstellung von ganztägigen Ereignissen ist es auch wichtig, Zeitzonen zu berücksichtigen. Da der Exchange-Server eine Mitternachts Start-und-Endzeit in der Zeitzone der Anforderung oder des Termins erzwingt, kann das Anzeigen dieses ganztägigen Ereignisses in einem für eine andere Zeitzone konfigurierten Client unerwartete Ergebnisse liefern. Je nach Client kann es als ganztägiges Ereignis mit zusätzlichen Tagen angezeigt werden, die Sie nicht einschließen wollten, oder es wird möglicherweise nicht als ganztägiges Ereignis insgesamt angezeigt. Aus diesem Grund wird empfohlen, die bevorzugte Zeitzone des Benutzers zu verwenden, wenn immer möglich, wenn Sie ganztägige Ereignisse erstellen.
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>Erstellen Sie ein ganztägiges Ereignis mithilfe der verwaltete EWS-API

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der verwaltete EWS-API ein ganztägiges Ereignis erstellen, beginnend mit dem durch den Parameter _StartDate_ angegebenen Datum und einer dauerhaften Anzahl von Tagen, die durch den _numDays_ -Parameter angegeben werden. Beachten Sie, dass der Termin in der Zeitzone erstellt wird, die durch die [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegeben wird. In diesem Beispiel wird davon ausgegangen, dass das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, das im Parameter _Service_ übergeben wurde, mit gültigen Werten für die Eigenschaften [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) initialisiert wurde. 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a>Erstellen eines ganztägigen Ereignisses mithilfe von EWS

Das folgende Beispiel zeigt eine EWS- [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung zum Erstellen eines ganztägigen Ereignisses. Der Termin wird in der östlichen Zeitzone erstellt, wie vom [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegeben. Beachten Sie, dass der Zeitbereich der Werte für [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) das Start [-und](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) Endelement sowohl "04:00Z" ist, das in der östlichen Zeitzone während der Sommerzeit in Mitternacht konvertiert wird. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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
    

