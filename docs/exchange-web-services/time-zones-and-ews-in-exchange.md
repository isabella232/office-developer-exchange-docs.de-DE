---
title: Zeitzonen und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: Erfahren Sie, wie Zeitzonen mit dem verwaltete EWS-API und EWS in Exchange funktionieren.
localization_priority: Priority
ms.openlocfilehash: 8435087d7709b77e7562e2b9d50ece58377dd8db
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463748"
---
# <a name="time-zones-and-ews-in-exchange"></a>Zeitzonen und EWS in Exchange

Erfahren Sie, wie Zeitzonen mit dem verwaltete EWS-API und EWS in Exchange funktionieren.
  
Zeitzonen sind nicht etwas, das die meisten Menschen viel zu denken geben. Sie sind jedoch ein wichtiges Konzept beim Angeben von Datums-und Uhrzeitangaben mithilfe der verwaltete EWS-API oder EWS. Zeitzonen in einer verwaltete EWS-API-oder EWS-Anwendung können unerwartet Ergebnisse liefern. Das ordnungsgemäße behandeln von Zeitzonen ist einfach, solange Sie wissen, wie.
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>Behandeln von Zeitzonen im verwaltete EWS-API

Wenn Sie die verwaltete EWS-API verwenden, werden die Zeitzonen größtenteils automatisch für Sie verarbeitet. Ohne explizite Aktion Ihrerseits verwendet die API die lokale Zeitzone des Clientcomputers und verarbeitet alle erforderlichen Konvertierungen hinter den Kulissen. Dies ist besonders wichtig, wenn es sich um den gewünschten Effekt handelt, Sie jedoch über andere Optionen verfügen.
  
Eine Option ist das Festlegen der [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft. Diese Eigenschaft steuert die Zeitzone für alle Anforderungen, die von der verwaltete EWS-API ausgeführt werden. Diese Eigenschaft ist schreibgeschützt; die einzige Möglichkeit, dies festzulegen, erfolgt über den Klassenkonstruktor. Wenn Sie entweder den [Datei "ExchangeService (System. TimeZoneInfo)](https://msdn.microsoft.com/library/dd635875%28v=exchg.80%29.aspx) -oder den [Datei" ExchangeService (ExchangeVersion, System. TimeZoneInfo)](https://msdn.microsoft.com/library/dd636248%28v=exchg.80%29.aspx) -Konstruktor verwenden, können Sie eine bestimmte Zeitzone als [System. TimeZoneInfo](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx) -Objekt angeben. Wenn Sie einen der anderen Konstruktoren verwenden, die kein **TimeZoneInfo** -Objekt als Parameter verwenden, legt die **Datei "ExchangeService** -Klasse die **TimeZone** -Eigenschaft auf die aktuelle Zeitzone des Clientcomputers fest. 
  
Unabhängig davon, ob Sie eine bestimmte Zeitzone festlegen oder als Zeitzone des Clientcomputers belassen, werden alle Datums-und Uhrzeitangaben in der Zeitzone ausgedrückt, die durch die **TimeZone** -Eigenschaft dargestellt wird. Das verwaltete EWS-API macht alle Date/Time-Eigenschaften als [System. DateTime](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx) -Strukturen verfügbar. Wenn Sie also Eigenschaften vom Typ Datum/Uhrzeit festlegen, sollten Sie beachten, dass die von Ihnen angegebene Zeit gemäß dem [DateTime. Kind](https://msdn.microsoft.com/library/system.datetime.kind%28v=vs.110%29.aspx) -Eigenschaftswert des **DateTime** -Objekts interpretiert wird. Wenn der Wert der **Kind** -Eigenschaft auf **Unspecified**festgelegt ist, wird der Wert des **DateTime** -Werts in der Zeitzone interpretiert, die von der **TimeZone** -Eigenschaft angegeben wird. Wenn Sie die Eigenschaften Datum/Uhrzeit lesen, werden alle **DateTime** -Eigenschaften in dieser Zeitzone ausgedrückt. 
  
Wenn Sie [neue Termine oder Besprechungen erstellen](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md) oder [vorhandene Termine oder Besprechungen aktualisieren](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md), können Sie die Zeitzone außer Kraft setzen, die in der **Zeitzone** für neue [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekte angegeben ist. Was Sie jedoch außer Kraft setzen können, hängt von der [EWS-Schemaversion](ews-schema-versions-in-exchange.md) ab, auf die Sie Zielen. Für alle Werte der [Datei "ExchangeService. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft können Sie den [Termin. StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) so festlegen, dass eine bestimmte Zeitzone für diesen Termin oder eine Besprechung verwendet wird. Wenn Sie einen Wert für die **Datei "ExchangeService. RequestedServerVersion** -Eigenschaft größer als **Exchange2007_SP1**verwenden, können Sie auch die [Termin. EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) -Eigenschaft festlegen, sodass Sie eine Zeitzone für die [Termin. End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) -Eigenschaft angeben können. Beachten Sie jedoch, dass sich diese Eigenschaften nur auf die Interpretation von Datum/Uhrzeit für die CREATE-Anforderung auswirken. Wenn Sie den Termin abrufen, werden die Anfangs-und Endzeiten weiterhin in der Zeitzone ausgedrückt, die von der **TimeZone** -Eigenschaft angegeben wird. 
  
Wenn Sie vorhandene Termine oder Besprechungen aktualisieren, können Sie die Zeitzone für ein **Termin** Objekt ändern, indem Sie die **StartTimeZone** -Eigenschaft und/oder die **EndTimeZone** -Eigenschaft festlegen. Dies führt dazu, dass die entsprechenden Zeiten entsprechend verschoben werden. Wenn Sie **Datei "ExchangeService. RequestedServerVersion** auf **Exchange2007_SP1**festgelegt haben, können Sie die **EndTimeZone** -Eigenschaft nicht festlegen; der Wert der **StartTimeZone** -Eigenschaft wird an seiner Stelle verwendet. 
  
**Tabelle 1. Zeitzoneneigenschaften in der verwaltete EWS-API**

|**Time Zone-Eigenschaft**|**Minimale Server Anforderungs Version**|**Beschreibung**|
|:-----|:-----|:-----|
|[TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Wenn Sie nicht über den Konstruktor für die **Datei "ExchangeService** -Klasse festgelegt wird, wird diese Eigenschaft auf die Zeitzone des Clientcomputers festgelegt. Alle **DateTime** -Eigenschaften beim Erstellen von Elementen und beim Abrufen vorhandener Elemente werden in dieser Zeitzone ausgedrückt. Diese Zeitzone kann in Erstellen von Anforderungen für Termine und Besprechungen durch Festlegen der **Termin. StartTimeZone** und/oder der **Termin. EndTimeZone** -Eigenschaft außer Kraft gesetzt werden. Wenn die Eigenschaft **Termin. StartTimeZone** nicht außer Kraft gesetzt wird, wird diese Zeitzone als Erstellungs Zeitzone für Termine und Besprechungen betrachtet.  <br/> |
|[StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Wenn diese Zeitzone für neue **Termin** Objekte festgelegt wird, werden die Eigenschaften [Termin. Start](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) und [Termin. ReminderDueBy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) interpretiert. Diese Zeitzone wird auch als Erstellungs Zeitzone für das **Termin** Objekt betrachtet.  <br/> Beim Abrufen vorhandener Elemente ist diese Eigenschaft nur Informations bereit. Die Werte der **DateTime** -Eigenschaften für einen vorhandenen Termin werden immer in der Zeitzone ausgedrückt, die durch die **Datei "ExchangeService. TimeZone** -Eigenschaft angegeben wird.  <br/> |
|[EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |Bei Festlegung für neue **Termin** Objekte wird diese Zeitzone verwendet, um die Eigenschaft [Termin. End](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) zu interpretieren.  <br/> Beim Abrufen vorhandener Elemente ist diese Eigenschaft nur Informations bereit. Die Werte der **DateTime** -Eigenschaften für einen vorhandenen Termin werden immer in der Zeitzone ausgedrückt, die durch die **Datei "ExchangeService. TimeZone** -Eigenschaft angegeben wird.  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>Behandeln von Zeitzonen in EWS

Wenn Sie EWS verwenden, werden Zeitzonen nicht automatisch für Sie verarbeitet, und die Dinge sind etwas komplizierter. Wie sich Zeitzonen auf EWS-Anforderungen und-Antworten auswirken, hängt von einer Reihe von Faktoren ab:
  
- Die im [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) -Element angegebene Exchange-Version 
    
- Die im [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegebene Zeitzone (sofern vorhanden) 
    
- Die in den Elementen [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx), [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)oder [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) angegebene Zeitzone (sofern in Terminen oder Besprechungen vorhanden) 
    
- Die in den XML- **DateTime** -Elementen angegebene Zeitzone (falls vorhanden) 
    
Die im Wert von **DateTime** -Elementen angegebene Zeitzone kann drei Formen annehmen. Sie können alle Details in [XML Schema Part 2: Datatypes Second Edition](http://www.w3.org/TR/xmlschema-2/#dateTime)lesen, jedoch in Paraphrase:
  
- **UTC (Universal Coordinated Time):** Angegeben durch "Z". Zum Beispiel  `2014-06-06T19:00:00.000Z`.
    
- **Bestimmte Zeitzone:** Durch "+" oder "-" gefolgt von Stunden und Minuten angegeben. Zum Beispiel  `2014-06-06T19:00:00.000-08:00`.
    
- **Keine Zeitzone:** Durch das Fehlen einer beliebigen Zeitzone angegeben. Zum Beispiel  `2014-06-06T19:00:00.000`.
    
Wenn eine Zeitzone in einem **DateTime** -Wert vorhanden ist (entweder UTC oder eine bestimmte Zeitzone), wird dieser Wert immer als diese Zeitzone interpretiert. Wenn keine Zeitzone vorhanden ist, hängt die Interpretation des Werts von der spezifischen Kombination der anderen Zeit Zonen bezogenen Elemente ab. 
  
**Tabelle 2. Zeitzonenelemente in EWS und ihre Auswirkungen**

|**RequestServerVersion**|**Zeitzonecontext vorhanden?**|**MeetingTimeZone, StartTimeZone oder EndTimeZone vorhanden (nur CalendarItem und MeetingRequest)?**|**DateTime in UTC**|**DateTime in der angegebenen Zeitzone**|**DateTime ohne Zeitzone**|**Zeitzone für Termin-und Besprechungs Erstellung**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |Ja  <br/> |Ja ( **MeetingTimeZone** )  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Elemente innerhalb des [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) -oder [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) -Elements, das das **MeetingTimeZone** -Element enthält, werden als Zeitzone im **MeetingTimeZone** -Element interpretiert, alle anderen als UTC interpretiert.  <br/> |Zeitzone im **MeetingTimeZone** -Element  <br/> |
|**Exchange2007_SP1** <br/> |Ja  <br/> |Nein  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Interpretiert als UTC  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |Nein  <br/> |Ja ( **MeetingTimeZone** )  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Elemente innerhalb des [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) -oder [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) -Elements, das das **MeetingTimeZone** -Element enthält, werden als Zeitzone im **MeetingTimeZone** -Element interpretiert, alle anderen als UTC interpretiert.  <br/> |Zeitzone im **MeetingTimeZone** -Element  <br/> |
|**Exchange2007_SP1** <br/> |Nein  <br/> |Nein  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Interpretiert als UTC  <br/> |UTC  <br/> |
|**Exchange2010** und höher  <br/> |Ja  <br/> |Ja ( **StartTimeZone** und/oder **EndTimeZone** )  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Wenn das **StartTimeZone** -Element vorhanden ist, wird der Wert der Elemente [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) als Zeitzone im **StartTimeZone** -Element interpretiert. Andernfalls wird der Wert dieser Elemente als Zeitzone im **timezonecontext** -Element interpretiert.  <br/> Wenn das **EndTimeZone** -Element vorhanden ist, wird der Wert des [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) -Elements als Zeitzone im **EndTimeZone** -Element interpretiert. Andernfalls wird der Wert des **End** -Elements als Zeitzone im **timezonecontext** -Element interpretiert.  <br/> Elemente außerhalb der [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) werden als Zeitzone im **timezonecontext** -Element interpretiert.  <br/> |Zeitzone im **StartTimeZone** -Element, falls vorhanden, Zeitzone im **timezonecontext** -Element, wenn nicht  <br/> |
|**Exchange2010** und höher  <br/> |Ja  <br/> |Nein  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Interpretiert als Zeitzone im **timezonecontext** -Element  <br/> |Zeitzone im **timezonecontext** -Element  <br/> |
|**Exchange2010** und höher  <br/> |Nein  <br/> |Ja ( **StartTimeZone** und/oder **EndTimeZone** )  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Wenn das **StartTimeZone** -Element vorhanden ist, wird der Wert der Elemente [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [ReminderDueBy](https://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) als Zeitzone im **StartTimeZone** -Element interpretiert. Andernfalls wird der Wert dieser Elemente als UTC interpretiert.  <br/> Wenn das **EndTimeZone** -Element vorhanden ist, wird der Wert des [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) -Elements als Zeitzone im **EndTimeZone** -Element interpretiert. Andernfalls wird der Wert des **End** -Elements als UTC interpretiert.  <br/> Elemente außerhalb der [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) werden als UTC interpretiert.  <br/> |Zeitzone im **StartTimeZone** -Element, falls vorhanden, UTC, wenn nicht  <br/> |
|**Exchange2010** und höher  <br/> |Nein  <br/> |Nein  <br/> |Interpretiert als UTC  <br/> |Wird als die im Wert angegebene Zeitzone interpretiert.  <br/> |Interpretiert als UTC  <br/> |UTC  <br/> |
   
Wenn Sie Antworten vom Server interpretieren, sollten Sie immer den Wert jedes Elements überprüfen und den Wert entsprechend interpretieren. Exchange wird immer eine Zeitzone (entweder UTC oder eine bestimmte Zeitzone) in den Wert einschließen.
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>Zusätzliche Zeit Zonen Überlegungen beim Erstellen von Terminen und Besprechungen

Wenn Sie einen Termin oder eine Besprechung erstellen, wird die Zeitzone, die für die Startzeit gilt, als Erstellungs Zeitzone für den Termin betrachtet. Zusätzlich zur Steuerung, wie die Datums-und Uhrzeitangaben beim Erstellen eines Termins oder einer Besprechung interpretiert werden, hat die Erstellungs Zeitzone folgende Auswirkungen auf das Element:
  
- Wenn das Element ein ganztägiges Ereignis ist, wird es möglicherweise auf unerwartete Weise angezeigt, wenn es von einem Client angezeigt wird, der eine andere Zeitzone als die Erstellungs Zeitzone verwendet. Dies liegt daran, dass [beim Erstellen eines ganztägigen Ereignisses](how-to-create-all-day-events-by-using-ews-in-exchange.md)die Anfangs-und Endzeit der ganztägigen Ereignisse auf Mitternacht der Erstellungs Zeitzone angepasst werden. Diese Zeit wird als eine andere Zeit als Mitternacht in einer anderen Zeitzone angezeigt, sodass das Element möglicherweise zusätzliche Tage umfasst. Aus diesem Grund wird empfohlen, dass Sie die Zeitzone verwenden, die für den primären Kalender Client des Benutzers konfiguriert ist, um nach Möglichkeit ganztägige Ereignisse zu erstellen.
    
- Wenn es sich bei dem Element um eine Besprechung handelt, wird die Erstellungs Zeitzone in der Outlook-Informationsleiste für die Besprechungsanfragen angezeigt, die von den Teilnehmern empfangen werden, wenn sich diese Zeitzone von der Zeitzone Ihres Clients unterscheidet.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [DateTime-Struktur](https://msdn.microsoft.com/library/system.datetime%28v=vs.110%29.aspx)
    
- [TimeZoneInfo-Klasse](https://msdn.microsoft.com/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

