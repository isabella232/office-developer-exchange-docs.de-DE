---
title: Zeitzonen und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0e0a666c-0541-414b-a7fb-297d94f692e6
description: Erfahren Sie, wie Zeitzonen die EWS Managed API und EWS in Exchange entwickelt.
ms.openlocfilehash: fcc8b00acf2b63de04718e13b82191de95bbf2b7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757137"
---
# <a name="time-zones-and-ews-in-exchange"></a>Zeitzonen und EWS in Exchange

Erfahren Sie, wie Zeitzonen die EWS Managed API und EWS in Exchange entwickelt.
  
Zeitzonen sind nicht etwas, mit denen meisten Benutzer erhalten, die viel betrachtet. Jedoch können sie beim Angeben von Datumsangaben und Uhrzeiten mithilfe des EWS Managed API oder EWS ein wichtiges Konzept. Handhabung von Zeitzonen in einer EWS Managed API oder EWS kann Anwendung unerwartete Ergebnisse ergeben. Behandeln von Zeitzonen ordnungsgemäß ist einfach, solange Sie wissen, wie.
  
## <a name="handling-time-zones-in-the-ews-managed-api"></a>Behandeln von Zeitzonen in die EWS Managed API

Wenn Sie die EWS Managed API verwenden, werden, Zeitzonen in den meisten Fällen automatisch für Sie behandelt. Ohne explizite Aktion des Benutzers die API verwendet die lokale Zeitzone des Clientcomputers und alle erforderliche Konvertierungen im Hintergrund behandelt. Dies ist nützlich, wenn, die den gewünschten Effekt, jedoch stehen Ihnen weitere Optionen.
  
Eine Option wird durch die [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft festlegen. Diese Eigenschaft steuert die Zeitzone für alle Anfragen, die durch die EWS Managed API ausgeführt. Diese Eigenschaft ist schreibgeschützt. über den Klassenkonstruktor ist die einzige Möglichkeit festgelegt. Wenn Sie die [ExchangeService(System.TimeZoneInfo)](http://msdn.microsoft.com/en-us/library/dd635875%28v=exchg.80%29.aspx) oder den Konstruktor [ExchangeService (ExchangeVersion, System.TimeZoneInfo)](http://msdn.microsoft.com/en-us/library/dd636248%28v=exchg.80%29.aspx) verwenden, können Sie eine bestimmte Zeitzone als [System.TimeZoneInfo](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx) -Objekt angeben. Wenn Sie einen der anderen Konstruktoren, die kein **TimeZoneInfo** -Objekt als Parameter akzeptieren verwenden, wird die **ExchangeService** -Klasse die Eigenschaft **"TimeZone"** auf die aktuelle Zeitzone des Clientcomputers. 
  
Gibt an, ob eine bestimmte Zeitzone festlegen oder behalten sie die Zeitzone des Clients Computer alle Datums- und Zeitangaben werden in die Zeitzone, dargestellt durch die Eigenschaft **"TimeZone"** ausgedrückt. Die EWS Managed API stellt alle Eigenschaften von Datum/Uhrzeit als [System.DateTime](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx) -Strukturen. Wenn Sie keine Datum/Uhrzeit-Eigenschaften festlegen, werden Sie also Beachten Sie, dass die Zeit, die von die Ihnen angegebenen entsprechend der [DateTime.Kind](http://msdn.microsoft.com/en-us/library/system.datetime.kind%28v=vs.110%29.aspx) -Eigenschaftswert auf **DateTime** -Objekts interpretiert wird. Wenn der Wert der Eigenschaft **Art** auf **Unspecified**festgelegt ist, wird der Wert der **DateTime** interpretiert, wie in der Zeitzone, die von der **TimeZone** -Eigenschaft angegeben wird. Wenn Sie Eigenschaften von Datum/Uhrzeit lesen, werden alle **DateTime** -Eigenschaften in dieser Zeitzone angegeben. 
  
Wenn Sie [neue Termine oder Besprechungen erstellen](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md) oder [Aktualisieren Sie vorhandene Termine oder Besprechungen](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)sind, müssen Sie die Möglichkeit zum Überschreiben der Zeitzone in die **Zeitzone** für neue [Termin](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekte angegeben. Genau wie Sie außer Kraft setzen können hängt jedoch die [EWS-Schemaversion](ews-schema-versions-in-exchange.md) , die Sie verwenden möchten. Für alle Werte der [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft können Sie die [Appointment.StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) mit einer bestimmten Zeitzone, Termin oder eine Besprechung festlegen. Wenn Sie einen Wert für die **ExchangeService.RequestedServerVersion** -Eigenschaft größer als **Exchange2007_SP1**verwenden, können Sie auch die [Appointment.EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) -Eigenschaft festlegen ermöglicht es Ihnen, eine Zeitzone für den [angeben Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) Eigenschaft. Beachten Sie, dass diese Eigenschaften nur die Interpretation der Datum/Uhrzeit für die Anforderung erstellen beeinflussen jedoch tragen. Wenn Sie den Termin abrufen, werden die Anfangs- und Endzeiten weiterhin in der Zeitzone, die durch die Eigenschaft **"TimeZone"** angegebene vermittelt werden. 
  
Wenn Sie vorhandene Termine oder Besprechungen aktualisieren, können Sie die Zeitzone für ein Objekt " **Appointment** " durch Festlegen der **StartTimeZone** -Eigenschaft und/oder **EndTimeZone** -Eigenschaft ändern. Dadurch verursacht, dass die entsprechenden Zeiten entsprechend verschoben. Wenn Sie die **ExchangeService.RequestedServerVersion** **Exchange2007_SP1**festgelegt haben, können Sie die **EndTimeZone** -Eigenschaft nicht festlegen; Stattdessen wird der Wert der **StartTimeZone** -Eigenschaft verwendet werden. 
  
**In Tabelle 1. Zeitzone Eigenschaften in die EWS Managed API**

|**Zeitzone-Eigenschaft**|**Minimale Anforderung Serverversion**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeitzone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Falls nicht über den Konstruktor für die **ExchangeService** -Klasse festgelegt, wird diese Eigenschaft auf die Zeitzone des Clientcomputers festgelegt. Alle **DateTime** -Eigenschaften beim Erstellen von Elementen und beim Abrufen von einer vorhandenen Elemente werden in dieser Zeitzone angegeben. Erstellen Sie dieses Mal Zone in außer Kraft gesetzt werden kann Anforderungen für Termine und Besprechungen, indem Sie die **Appointment.StartTimeZone** und/oder die **Appointment.EndTimeZone** -Eigenschaft. Wenn von der **Appointment.StartTimeZone** -Eigenschaft nicht überschrieben wird, gilt diese Zeitzone die Zeitzone Erstellung für Termine und Besprechungen.  <br/> |
|[StartTimeZone-Zeitzone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2007_SP1** <br/> |Wenn Sie auf neuer **Termin** Objekte festgelegt, die diese Zeitzone verwendet wird, die Eigenschaften [Appointment.Start](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.start%28v=exchg.80%29.aspx) und [Appointment.ReminderDueBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) interpretiert werden. Diese Zeitzone gilt auch die Erstellung Zeitzone für **Appointment** -Objekts.  <br/> Wenn Sie vorhandene Elemente abrufen möchten, ist diese Eigenschaft nur Informationszwecken. Die Werte der Eigenschaften auf vorhandenen Termin **DateTime** werden immer in der Zeitzone angegeben, die von der **ExchangeService.TimeZone** -Eigenschaft angegeben.  <br/> |
|[EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) <br/> |**Exchange2010** <br/> |Wenn für neue **Termin** -Objekte festgelegt, die diese Zeitzone verwendet wird, die [Appointment.End](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.end%28v=exchg.80%29.aspx) -Eigenschaft interpretiert werden.  <br/> Wenn Sie vorhandene Elemente abrufen möchten, ist diese Eigenschaft nur Informationszwecken. Die Werte der Eigenschaften auf vorhandenen Termin **DateTime** werden immer in der Zeitzone angegeben, die von der **ExchangeService.TimeZone** -Eigenschaft angegeben.  <br/> |
   
## <a name="handling-time-zones-in-ews"></a>Behandeln von Zeitzonen in der Exchange-Webdienste

Wenn Sie Exchange-Webdienste verwenden, Zeitzonen werden nicht automatisch für Sie behandelt und Dinge sind etwas komplizierter. Wie Zeitzonen EWS-Anforderungen und-Antworten beeinflussen, hängt von einer Reihe von Faktoren ab:
  
- Die Exchange-Version im [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) -Element 
    
- Die Zeitzone, die im [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegeben (falls vorhanden) 
    
- Der Zeitzone angegeben in den [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx), [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)oder [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elementen (falls vorhanden, auf der Termine oder Besprechungen) 
    
- Die Zeitzone in der XML-Schemaelemente **DateTime** angegeben wird (falls vorhanden) 
    
Die Zeitzone, die den Wert der **DateTime** -Elemente angegeben können drei Arten erfolgen. Sie können die Details im Lesen [XML-Schema, Teil 2: Datentypen Second Edition](http://www.w3.org/TR/xmlschema-2/#dateTime), jedoch für umschreiben:
  
- **Koordinierte Weltzeit (UTC):** Von "Z" angegeben wird. Zum Beispiel`2014-06-06T19:00:00.000Z`
    
- **Bestimmten Zeitzone:** Vom angegebenen '+' oder '-' gefolgt von Stunden und Minuten. Zum Beispiel`2014-06-06T19:00:00.000-08:00`
    
- **Ohne Angabe einer Zeitzone:** Durch das Fehlen einer Zeitzone angegeben. Zum Beispiel`2014-06-06T19:00:00.000`
    
Wenn eine Zeitzone in ein **DateTime** -Wert (UTC oder einer bestimmten Zeitzone) vorhanden ist, wird dieser Wert immer als diese Zeitzone interpretiert. Wenn keine Zeitzone vorhanden ist, hängt die Interpretation des Werts auf bestimmte Kombination der anderen Zeitzone verwandte Elemente ab. 
  
**In Tabelle 2. Zeitzone Elemente EWS und deren Effekte**

|**RequestServerVersion**|**TimeZoneContext vorhanden?**|**MeetingTimeZone, StartTimeZone oder EndTimeZone vorhanden (CalendarItem und nur MeetingRequest)?**|**DateTime in UTC**|**DateTime in bestimmten Zeitzone**|**DateTime keine Angabe einer Zeitzone**|**Termin und Besprechung erstellen Zeitzone**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|**Exchange2007_SP1** <br/> |Ja  <br/> |Ja ( **MeetingTimeZone** )  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Elemente im [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) -Element mit dem **MeetingTimeZone** Element werden als die Zeitzone in das **MeetingTimeZone** -Element, alle anderen als UTC interpretiert interpretiert.  <br/> |Zeitzone in **MeetingTimeZone** -element  <br/> |
|**Exchange2007_SP1** <br/> |Ja  <br/> |Nein  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Als UTC interpretiert  <br/> |UTC  <br/> |
|**Exchange2007_SP1** <br/> |Nein  <br/> |Ja ( **MeetingTimeZone** )  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Elemente im [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) -Element mit dem **MeetingTimeZone** Element werden als die Zeitzone in das **MeetingTimeZone** -Element, alle anderen als UTC interpretiert interpretiert.  <br/> |Zeitzone in **MeetingTimeZone** -element  <br/> |
|**Exchange2007_SP1** <br/> |Nein  <br/> |Nein  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Als UTC interpretiert  <br/> |UTC  <br/> |
|**Exchange2010** und höher  <br/> |Ja  <br/> |Ja ( **StartTimeZone** und/oder **EndTimeZone** )  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Wenn das **StartTimeZone** -Element vorhanden ist, wird der Wert der [Starten](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) Elemente als die Zeitzone in der **StartTimeZone** -Element interpretiert. Andernfalls werden der Wert dieser Elemente als die Zeitzone in das Element **TimeZoneContext** interpretiert.  <br/> Wenn das **EndTimeZone** -Element vorhanden ist, wird der Wert des [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) -Elements als Zeitzone im **EndTimeZone** -Element interpretiert. Andernfalls wird der Wert des **End** -Elements als Zeitzone im Element **TimeZoneContext** interpretiert.  <br/> Elemente außerhalb der [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) sind als die Zeitzone in das Element **TimeZoneContext** interpretiert.  <br/> |Zeitzone in der **StartTimeZone** -Element, falls vorhanden, Zeitzone in **TimeZoneContext** -Elements, sofern nicht  <br/> |
|**Exchange2010** und höher  <br/> |Ja  <br/> |Nein  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Interpretiert als Zeitzone im **TimeZoneContext** -element  <br/> |Zeitzone im **TimeZoneContext** -element  <br/> |
|**Exchange2010** und höher  <br/> |Nein  <br/> |Ja ( **StartTimeZone** und/oder **EndTimeZone** )  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Wenn das **StartTimeZone** -Element vorhanden ist, wird der Wert der [Starten](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) Elemente als die Zeitzone in der **StartTimeZone** -Element interpretiert. Andernfalls werden der Wert dieser Elemente als UTC interpretiert.  <br/> Wenn das **EndTimeZone** -Element vorhanden ist, wird der Wert des [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) -Elements als Zeitzone im **EndTimeZone** -Element interpretiert. Andernfalls wird der Wert der **End** -Element als UTC interpretiert.  <br/> Elemente außerhalb der [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) oder [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx) werden als UTC interpretiert.  <br/> |Zeitzone in der **StartTimeZone** -Element, falls vorhanden, wenn nicht UTC  <br/> |
|**Exchange2010** und höher  <br/> |Nein  <br/> |Nein  <br/> |Als UTC interpretiert  <br/> |Als Zeitzone gemäß den Wert interpretiert  <br/> |Als UTC interpretiert  <br/> |UTC  <br/> |
   
Beim Interpretieren von Antworten auf dem Server, sollten Sie den Wert der einzelnen Elemente überprüfen und Interpretieren Sie den Wert entsprechend. Exchange wird immer eine Zeitzone (UTC oder einer bestimmten Zeitzone) den Wert aufzunehmen.
  
## <a name="additional-time-zone-considerations-when-creating-appointments-and-meetings"></a>Zusätzliche Zeitzone Aspekte beim Erstellen von Terminen und Besprechungen

Wenn Sie einen Termin oder eine Besprechung erstellen, gilt die Zeitzone, die für die Startzeit gilt die Erstellung Zeitzone für den Termin. Zusätzlich zu steuern, wie die Date/times interpretiert werden, wenn Sie einen Termin oder eine Besprechung erstellt wird, hat die Zeitzone erstellen die folgenden Effekte für das Element:
  
- Wenn das Element ein ganztägiges Ereignis ist, möglicherweise nicht wie erwartet, wenn von einem Client angezeigt, die eine andere Zeitzone als die Zeitzone Erstellung verwendet wird angezeigt. Dies ist, da Zeit, [Wenn ein ganztägiges Ereignis erstellt wird](how-to-create-all-day-events-by-using-ews-in-exchange.md), die Start- und ganztägige Ereignisse sind Mitternacht der Erstellung Zeitzone angepasst. Dieser Zeit wird als Uhrzeit als Mitternacht in einer anderen Zeitzone angezeigt, damit das Element angezeigt werden kann, um zusätzliche Tage umfassen. Aus diesem Grund wird empfohlen, Sie die Zeitzone für den Kalender des Benutzers Primärclient konfiguriert, verwenden um nach Möglichkeit ganztägige Ereignisse erstellen.
    
- Wenn das Element einer Besprechung ist, wird die Zeitzone für die Erstellung dieser Zeitzone weicht von der Zeitzone des deren Clients in der Outlook-Informationsleiste auf die von den Teilnehmern empfangen Besprechungsanfragen angezeigt.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Terminen in einer bestimmten Zeitzone mithilfe der EWS in Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)
    
- [Aktualisieren Sie die Zeitzone für einen Termin im Exchange mithilfe der Exchange-Webdienste](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [DateTime-Struktur](http://msdn.microsoft.com/en-us/library/system.datetime%28v=vs.110%29.aspx)
    
- [TimeZoneInfo-Klasse](http://msdn.microsoft.com/en-us/library/system.timezoneinfo%28v=vs.110%29.aspx)
    

