---
title: Kalender und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: Weitere Informationen zu Kalendern, Kalenderordnern und -elementen, Terminen und Besprechungen in Exchange.
ms.openlocfilehash: bb9702118ff1db66862a5788c2d8f58dd55c4d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756818"
---
# <a name="calendars-and-ews-in-exchange"></a>Kalender und EWS in Exchange

Weitere Informationen zu Kalendern, Kalenderordnern und -elementen, Terminen und Besprechungen in Exchange.
  
Sie sind wahrscheinlich mit den vielen Kalenderfunktionen in E-Mail-Clients wie Outlook vertraut, mit denen Sie Termine pflegen, Besprechungen planen, die Verfügbarkeit anderer Personen prüfen, Teilnehmer einladen und Besprechungen ändern oder absagen können.
  
Kalenderbezogene Funktionen in Exchange unterscheiden sich etwas von den Optionen in einem Client wie Outlook. Statt Informationen anzuzeigen, können Sie mit EWS in Exchange beispielsweise Informationen erstellen, speichern, senden oder ändern. Um EWS zum Arbeiten mit Kalendern zu verwenden, müssen Sie vertraut sein mit Konzepten wie beispielsweise der Informationsspeicherung, Zeiten, Serien und Nachrichtenflüssen. Genauer gesagt, müssen Sie mit Folgendem vertraut sein:
  
- Kalenderordner, Kalenderelemente und Kalenderansichten
    
- Besprechungsanfragen, Antworten, Planung, Teilnehmern, Ressourcen, Räumen und Verfügbarkeit
    
- Zeiträumen, Zeitzonen und Start- und Endzeiten von Besprechungen und Terminen
    
- Terminserien, Serienmustern, Ausnahmen und einzelnen Instanzen von Terminen und Besprechungen
    
Glücklicherweise bieten EWS und die verwaltete EWS-API zahlreiche Vorgänge und Methoden, mit denen Sie eine Vielzahl von kalenderbezogenen Aufgaben ausführen können. Sie können beispielsweise die verwaltete EWS-API verwenden, um mit nur wenigen Codezeilen eine Besprechung zu erstellen und Einladungen an die Teilnehmer versenden, wie im folgenden Beispiel veranschaulicht wird.
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## <a name="calendar-folders-and-calendar-items"></a>Kalenderordner und Kalenderelemente
<a name="bk_CalendarFolder"> </a>

Kalenderordner enthalten Kalenderelemente. Kalenderordner besitzen eine [Ordnerklasse](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) von **IPF.Appointment**, und können nur Elemente enthalten, die durch die verwaltete [ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx)-EWS-API-Eigenschaft definiert sind, die mit einem [Appointment-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)-Objekt oder dem EWS-[CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)-Element verknüpft ist. 
  
Elemente in einem Kalenderordner unterscheiden sich etwas von Elementen in anderen Ordnern eines Postfachs, da Vorkommen in einer Terminserie und Ausnahmen in einer Terminserie keine tatsächlichen Elemente in einem Postfach sind, sondern intern als Anlagen eines Serienmasters gespeichert werden. Um alle Termine in einem angegebenen Datumsbereich abzurufen, müssen Sie deshalb eine Kalenderansicht verwenden. Weitere Informationen zum Abrufen von Terminen und Kalenderansichten finden Sie unter [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).
  
## <a name="meetings-and-appointments"></a>Besprechungen und Termine
<a name="bk_meetings"> </a>

Der wesentliche Unterschied zwischen Besprechungen und Terminen besteht darin, dass Besprechungen über Teilnehmer verfügen und Termine nicht. Intern verwendet Exchange dasselbe Objekt für Besprechungen und Termine. Zum Arbeiten mit Besprechungen und Terminen verwenden Sie die verwaltete EWS-API-[Appointment-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) oder das EWS- [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)-Element. 
  
Termine und Besprechungen können einzelne Instanzen oder teil einer [Terminserie](recurrence-patterns-and-ews.md) sein, da Termine jedoch keine Teilnehmer, Räume oder Ressourcen umfassen, muss dafür keine Nachricht gesendet werden.
  
Da Besprechungen das Senden und Antworten auf Anfragen und Aktualisierungen umfasst, ist dazu mehr Aufwand nötig, als nur auf Elemente in einem Kalenderordner zuzugreifen. Sie sind auch mit einem Workflow verknüpft. Besprechungen müssen geplant werden, wenn Teilnehmer verfügbar sind und können außerdem die Reservierung eines Besprechungsraums oder von Ressourcen wie einem Projektor oder anderen Dingen umfassen.
  
Zum Besprechungsworkflow gehören in der Regel folgende Schritte:
  
1. Ein Meeting wird erstellt und mit Informationen wie Start- und Endzeit, Ort und einem Nachrichtentext befüllt.
    
2. Dann wird eine Liste mit potenziellen Teilnehmern, Ressourcen und dem Raum erstellt.
    
3. Anschließend wird der Verfügbarkeitsstatus der Teilnehmer überprüft. 
    
4. Daraufhin wird eine Besprechungsanfrage an die Teilnehmer gesendet.
    
5. Teilnehmer antworten auf die Besprechungsanfrage mit der Absicht, an der Besprechung teilzunehmen oder nicht. Teilnehmer können außerdem eine andere Zeit für die Besprechung vorschlagen.
    
6. Besprechungen können abgesagt oder aktualisiert werden, dadurch wird in der Regel ein neues Versenden von E-Mails an die Teilnehmer ausgelöst.
    
## <a name="calendars-and-time"></a>Kalender und die Uhrzeit
<a name="bk_Time"> </a>

Uhrzeitbezogene Funktionen sind integraler Bestandteil von Kalendern. Termine und Besprechungen weisen Start- und Endzeiten auf, Zeiträume und andere zeitbezogene Eigenschaften, wie z. B.die Zeit der Nachrichtenerstellung, Versendung und des Empfangs. Auf Basis der Start- und Endzeit können Termine und Besprechungen aus dem Kalenderordner abgerufen werden. Terminserien weisen Anfangs- und Endzeiten auf. Und Besprechungen treten innerhalb einer angegeben Zeitzone auf, die in der Weltwirtschaft immer wichtiger werden.
  
Uhrzeiten werden auf einem Exchange-Server intern in der koordinierten Weltzeit (Coordinated Universal Time, UTC) gespeichert. Exchange wandelt sie basierend auf den Clienteinstellungen in die Uhrzeit der lokalen Zeitzone um. [DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)-Eigenschaften beziehen sich auf die lokale Zeitzone des Computers. 
  
## <a name="recurring-series"></a>Terminserie
<a name="bk_recurrence"> </a>

Eine Terminserie von Terminen oder Besprechungen besteht aus einem Serienmaster, einer Gruppe von Serienelementen, und optional aus einer Gruppe von Ausnahmeelementen. Serieninformationen werden im Serienmasterelement gespeichert. Das [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx)-EWS-Element ist mit Vorkommen und Ausnahmen in einer Serie verknüpft, außerdem können Sie die verwaltete [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/dd635978%28v=EXCHG.80%29.aspx)-EWS-API-Methode verwenden, um den Serienmaster abzurufen. Mithilfe einer Serieninstanz können Sie nach allen der Serie zugeordneten Elementen und Informationen suchen. 
  
Beachten Sie, dass Serieneigenschaften zu allen Kalenderelementen vorhanden sind, sie werden jedoch nur bei den Serienmasterelementen ausgefüllt. Zusätzlich zu einem Index aller Vorkommen in einer Serie besitzt der Serienmaster einen Verweis zu geänderten und gelöschten Vorkommen und Serienmustern (z. B. täglich, wöchentlich, monatlich oder jährlich).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [Rufen Sie Raumlisten mithilfe von EWS in Exchange ab](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [Verarbeiten von Kalenderelementen in Batches in Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [Serienmuster und EWS](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

