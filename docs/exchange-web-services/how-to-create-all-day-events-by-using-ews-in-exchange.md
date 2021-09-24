---
title: Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Erfahren Sie, wie Sie ganztägige Ereignisse mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
ms.openlocfilehash: 8769999907df46f519355a36fdf409f9ad347330
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521221"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie ganztägige Ereignisse mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
  
Ganztägige Ereignisse bieten eine Möglichkeit, etwas darzustellen, das für einen ganzen Tag oder mehrere Tage geschieht , z. B. einen Feiertag oder Feiertagstage. Das Erstellen von ganztägigen Ereignissen mit der verwalteten EWS-API oder EWS ist ein Snap. Es ist wie [beim Erstellen von Terminen,](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)aber mit ein paar kleinen Änderungen.
  
## <a name="setting-start-and-end-times"></a>Festlegen der Start- und Endzeiten

Per Definition beginnen ganztägige Ereignisse um Mitternacht an einem bestimmten Tag und enden 24 Stunden (oder ein Vielfaches von 24 Stunden) später. Mit der verwalteten EWS-API und EWS können Sie jedoch andere Zeiten als Mitternacht angeben, wenn Sie ganztägige Ereignisse erstellen. Dies kann zu unerwünschtem Verhalten führen, wenn Sie nicht wissen, wie diese Zeiten auf dem Server übersetzt werden.
  
Wenn eine Anforderung zum Erstellen eines neuen ganztägigen Ereignisses mit nicht mitternachts (in der [Zeitzone der Anforderung oder des Termins)](time-zones-and-ews-in-exchange.md)Anfangs- und/oder Endzeiten empfangen wird, werden diese Zeiten gemäß den folgenden Regeln an Mitternacht in der entsprechenden Zeitzone angepasst:
  
- Startzeiten, die nicht Mitternacht sind, werden vor der angegebenen Zeit an Mitternacht angepasst. Beispielsweise wird am 6. Juni um 13:00 Uhr an 12:00 Uhr am 6. Juni angepasst.
    
- Endzeiten, die nicht Mitternacht sind, werden nach der angegebenen Zeit an Mitternacht angepasst. Beispielsweise wird am 6. Juni um 13:00 Uhr an 12:00 Uhr am 7. Juni angepasst.
    
Das von Ihnen erstellte ganztägige Ereignis enthält also immer die von Ihnen angegebene Start- und Endzeit, kann jedoch aufgrund der Verschiebung zu Mitternacht zusätzliche Zeit im Kalender des Benutzers beanspruchen. Da der Server die Start- und Endzeit auf Mitternacht anpasst, wird empfohlen, die Start- und Endzeit um Mitternacht anzugeben, um unbeabsichtigte Änderungen an den Zeiten zu vermeiden.
  
Es ist auch wichtig, Zeitzonen beim Erstellen von ganztägigen Ereignissen zu berücksichtigen. Da der Exchange Server eine Mitternachtsanfangs- und Endzeit in der Zeitzone der Anforderung oder des Termins erzwingt, kann das Anzeigen dieses ganztägigen Ereignisses in einem Client, der für eine andere Zeitzone konfiguriert ist, zu unerwarteten Ergebnissen führen. Je nach Client kann es als ganztägiges Ereignis mit zusätzlichen Tagen erscheinen, die Sie nicht einschließen wollten, oder es wird möglicherweise nicht als ganztägiges Ereignis angezeigt. Aus diesem Grund wird empfohlen, wann immer möglich die bevorzugte Zeitzone des Benutzers zu verwenden, wenn Sie ganztägige Ereignisse erstellen.
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>Erstellen eines ganztägigen Ereignisses mithilfe der verwalteten EWS-API

Das folgende Beispiel zeigt, wie Sie die verwaltete EWS-API verwenden, um ein ganztägiges Ereignis zu erstellen, beginnend mit dem durch den  _Parameter "startDate"_ angegebenen Datum und dauerhaft für die Anzahl der Tage, die durch den  _numDays-Parameter_ angegeben werden. Beachten Sie, dass der Termin in der durch die [ExchangeService.TimeZone-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) angegebenen Zeitzone erstellt wird. In diesem Beispiel wird davon ausgegangen, dass das im _Dienstparameter_ übergebene [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) mit gültigen Werten für die [Eigenschaften Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) initialisiert wurde. 
  
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

Das folgende Beispiel zeigt eine EWS [CreateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) zum Erstellen eines ganztägigen Ereignisses. Der Termin wird in der Eastern-Zeitzone erstellt, wie durch das [TimeZoneContext-Element](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) angegeben. Beachten Sie, dass der Zeitteil der Werte der [Start-](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [End-Elemente](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) 04:00Z ist, was während der Sommerzeit in Mitternacht in die Zeitzone "Ost" konvertiert wird. 
  
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
    

