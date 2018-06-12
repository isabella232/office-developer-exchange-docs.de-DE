---
title: Posteingangsverwaltung und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3dfa0fc9-64bb-4d18-bff7-bf6b3bed4a0d
description: Erfahren Sie, wie Sie Ihren Posteingang in Ihrer verwalteten EWS-API oder EWS-Anwendung mithilfe von Posteingangsregeln und der Liste der blockierten Absender verwalten können.
ms.openlocfilehash: fe06c5ee87e2679506ca7247c5fc2c96912dee86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757019"
---
# <a name="inbox-management-and-ews-in-exchange"></a>Posteingangsverwaltung und EWS in Exchange

Erfahren Sie, wie Sie Ihren Posteingang in Ihrer verwalteten EWS-API oder EWS-Anwendung mithilfe von Posteingangsregeln und der Liste der blockierten Absender verwalten können.
  
Exchange-Postfächer verfügen über Features, mit denen Benutzer ihre eingehenden E-Mail-Nachrichten automatisch organisieren können. Alle diese Features funktionieren auf dem Server ohne Eingreifen des Benutzers, dienen aber unterschiedlichen Zwecken. Die verwaltete EWS-API und EWS ermöglichen den Zugriff auf diese Features, damit Ihre Benutzer ihre Posteingänge verwalten können.
  
**In Tabelle 1. Posteingang Management-features**

|**Aktion**|**Verwenden Sie...**|
|:-----|:-----|
|Ergreifen von Maßnahmen für eingehende Nachrichten (z. B. Verschieben in einen anderen Ordner oder löschen) basierend auf bestimmten Kriterien (z. B. Absender, Betreff oder Anlagen)  <br/> |Posteingangsregeln  <br/> |
|Löschen aller eingehenden E-Mail-Nachrichten eines bestimmten Absenders  <br/> |Liste der geblockten Absender  <br/> |
   
## <a name="inbox-rules"></a>Posteingangsregeln
<a name="bk_InboxRules"> </a>

Seien wir ehrlich: Nicht alle E-Mail-Nachrichten sind gleichberechtigt. Für jede E-Mail, die ein Benutzer von seinem Vorgesetzten erhält, gibt es eine von einer Internet-Videoverteilerliste für Katzenvideos, der er vor Jahren beigetreten und nie mehr verlassen hat. Katzenvideos sind zwar unterhaltsam, erzeugen aber riesige Datenmengen, sodass  wichtige Nachrichten einfach im Meer der Verteilungslisten-E-Mails in einem Posteingang verloren gehen können. Viele Benutzer verwenden Posteingangsregeln, um diese Nachrichten auszusortieren, damit der Posteingang übersichtlicher wird. Mit Exchange-Webdienste (EWS) kann Ihre Anwendung die Leistungsfähigkeit von Regeln optimal nutzen.
  
Die EWS Managed API bietet die [ExchangeService.GetInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) und [ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) Methoden zum Arbeiten mit Regeln. EWS bietet die [GetInboxRules](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) und [UpdateInboxRules](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) Vorgänge für die Arbeit mit Regeln. Beachten Sie jedoch, dass die EWS Managed API und EWS beim Arbeiten mit Posteingangsregeln die folgenden Einschränkungen gelten: 
  
- EWS kann nicht auf "Nur-Client"-Regeln oder Regeln zugreifen oder diese erstellen, die in Outlook für die Ausführung "nur auf diesem Computer" festgelegt sind.
    
- Um die aktuellen Regeln mithilfe von EWS zu ändern, müssen Sie den Outlook-Regel-BLOB entfernen, sofern vorhanden. Dies bedeutet, dass durch das Verwenden von EWS zum Ändern von Regeln alle Regeln, die zuvor mithilfe von Outlook ausgeschaltet (deaktiviert) wurden, gelöscht werden.  
    
### <a name="how-do-rules-work"></a>Wie funktionieren Regeln?
<a name="bk_HowRulesWork"> </a>

Das Regelmodul fungiert als Gatekeeper Postfach eines Benutzers. Eintreffen eine Nachricht in das Postfach des Benutzers, aber bevor die Nachricht im Posteingang angezeigt wird, wird die Nachricht gegen eine sortierte Liste der Regeln ausgewertet. Beachten Sie, dass dies nur zu hinzukommen Zeitpunkt und nur im Posteingang auftritt. Diese Regeln bestehen aus drei Teilen: [Bedingungen](#bk_Conditions), [Aktionen](#bk_Actions)und [Ausnahmen](#bk_Exceptions).
  
Beginnend mit der Regel ganz oben in der Regelliste führt das Regelmodul die folgenden Schritte aus, bis das Ende der Regelliste erreicht ist:
  
1. Überprüft die Nachricht, um festzustellen, ob sie alle Kriterien der Regel erfüllt.
    
1. Wenn sie alle Bedingungen erfüllt, wird die Auswertung mit Schritt 2 fortgesetzt.
    
2. Wenn sie nicht alle Bedingungen erfüllt, lädt das Regelmodul die nächste Regel in der Liste und beginnt dann wieder bei Schritt 1.
    
2. Überprüft die Nachricht, um festzustellen, ob sie Ausnahmen der Regel erfüllt.
    
1. Wenn Ausnahmen erfüllt werden, lädt das Regelmodul die nächste Regel in der Liste und beginnt dann wieder bei Schritt 1.
    
2. Wenn sie keine der Ausnahmen erfüllt, wird die Bewertung mit Schritt 3 fortgesetzt.
    
3. Führt die Aktionen durch, die in der Regel für die Nachricht angegeben sind.
    
1. Wenn die Aktion "Verarbeiten weiterer Regeln beenden" angegeben ist, führt das Regelmodul alle anderen Aktionen für die Nachricht aus und wird dann ohne Auswertung zusätzlicher Regeln für die Nachricht beendet.
    
2. Wenn die Aktion "Verarbeiten weiterer Regeln beenden" nicht angegeben ist, lädt das Regelmodul die nächste Regel in der Liste und beginnt dann wieder bei Schritt 1.
    
Die folgende Abbildung zeigt den Prozess, dem das Regelmodul folgt.
  
**Abbildung 1: Regeln Engine (Übersicht)**

![Ein Diagramm, das die Schritte zeigt, die das Regelmodul verwendet, angefangen mit der Bewertung der Regel, gefolgt von der Feststellung, ob die Regelkriterien erfüllt werden, und dann der Durchführung der Aktion oder dem Wechsel zur nächsten Regel, bis der Vorgang abgeschlossen ist.](media/Ex15_Rules_EngineOverview.png)
  
### <a name="putting-the-pieces-together---parts-of-a-rule"></a>Zusammensetzen der Teile - Teile einer Regel
<a name="bk_Pieces"> </a>

Eine Möglichkeit zum Visualisieren der Teile einer Regel ist, stellen Sie sich, dass Sie die Anweisungen an eine Person zuweisen möchten, die mit Ihrer eingehenden e-Mails organisieren beauftragt ist. An diese Person Sie sagen: "beim Empfang einer Nachricht, die \<Bedingungen hier einfügen\>, führen Sie \<Aktionen hier einfügen\>, es sei denn, die Nachricht \<Ausnahmen hier einfügen\>. Werfen wir näher an jeden Teil.
  
#### <a name="conditions"></a>Bedingungen
<a name="bk_Conditions"> </a>

[Bedingung](http://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx) wird beschrieben, wann eine Regel angewendet werden soll. Während Sie die Bedingungen einer Regel (was in einer Regel, die für jede Nachricht empfangen gilt) weglassen können, ist es ganz häufiger für Regeln für die Bedingungen verfügen, die auf eine Teilmenge der eingehenden Nachrichten gelten. Einige Beispiele sind "Wenn eine Nachricht von Sadie ist" oder "eine Nachricht an die Verteilerliste 'Cat Video Benutzern' gesendet wird". Regeln können mehrere Bedingungen haben. Wenn mehr als eine Bedingung von Regeln vorhanden sind, müssen in der Reihenfolge für das Regelmodul angegebene Aktion ausführen aller Bedingungen erfüllt sein. 
  
#### <a name="actions"></a>Aktionen
<a name="bk_Actions"> </a>

[Vorgänge](http://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx) beschrieben, was geschieht, wenn eine Regel angewendet wird. Beispiele sind "Verschieben der Nachricht in den Ordner"Katzen"" oder "Markieren der Nachricht mit der Wichtigkeit 'Niedrig'". Regeln können mehrere Aktionen haben. Wenn Sie mehrere Aktionen für eine Regel angeben, werden alle Aktionen ausgeführt, wenn die Regel angewendet wird. 
  
#### <a name="exceptions"></a>Ausnahmen
<a name="bk_Exceptions"> </a>

[Ausnahmen](http://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx) beschreiben bei eine Regel nicht angewendet werden soll, auch wenn die in die Bedingungen angegebenen Kriterien erfüllt sind. Beispiele sind "außer wenn die Nachricht nur an mich gesendet wird" oder "es sei denn, wenn die Nachricht von Mom". Eine Regel kann mehrere Ausnahmen haben. Wenn Regeln mehr als eine Ausnahme haben und Ausnahmen erfüllt sind, wird die Regel nicht angewendet. 
  
### <a name="example-herding-those-cats"></a>Beispiel: Verwalten dieser Katzen
<a name="bk_Example"> </a>

Werfen wir einen Blick darauf, wie Ihre Benutzer diese Regeln verwenden können, um den Datenverkehr von der Verteilerliste mit den Internetkatzenvideos zu vermeiden. Nehmen wir Folgendes an:
  
- Diese Nachrichten werden an eine Verteilerliste namens "Fans von Internetkatzenvideos" gesendet.
    
- Möchten, dass Ihre Benutzer schließlich diese Nachrichten lesen, die sie gerade nicht möchten, dass sie ihren Posteingang belegt. Sie würden vielmehr in einen Ordner namens "Katzen" file.
    
- Ihre Benutzer möchten Nachrichten, die an diese Verteilerliste von deren Müttern gesendet werden, sofort lesen, da Mama die witzigsten Videos sendet.
    
Das Regelmodul erhält folgende Anweisung: "Beim Eintreffen einer Nachricht, die an die Verteilerliste 'Fans von Internetkatzenvideos' gesendet wird, verschiebe diese in den Ordner 'Katzen', es sei denn, die Nachricht ist von Mama".  
  
**In Tabelle 2. Regel-definition**

|**Regel-Webpart**|**Wert**|
|:-----|:-----|
|Bedingungen  <br/> |Gesendet an die Verteilerliste 'Fans von Internetkatzenvideos'  <br/> |
|Aktionen  <br/> |Verschieben der Nachricht in den Ordner 'Katzen'  <br/> UND Verarbeiten weiterer Regeln beenden  <br/> |
|Ausnahmen  <br/> |Von 'Mama'  <br/> |
   
> [!NOTE]
> Beachten Sie, dass "Verarbeiten weiterer Regeln beenden" eine der Aktionen in der resultierenden Regel ist. Im Allgemeinen ist es ratsam, diese Aktion einzuschließen, um Verwirrung darüber zu vermeiden, welche Regeln für eine bestimmte Nachricht gilt. Durch Auslasen dieser Aktion und ordnungsgemäßem Sortieren Ihrer Regeln können Sie jedoch eine erweiterte Verarbeitung von eingehenden Nachrichten erzielen. In diesem Fall ist es wahrscheinlich sicher, dass Nachrichten mit Internetkatzenvideos keine erweiterte Verarbeitung benötigen. 
  
Kurz nach dem Erstellen dieser Regel trifft eine neue Nachricht ein. Eine Mitarbeiterin sendet eine Nachricht an die Verteilerliste. Wenn wir die Arbeit des Regelmoduls einmal mental ausführen, erfüllt die Nachricht allen angegebenen Bedingungen (sie wird an 'Fans von Internetkatzenvideos' gesendet) und keine der Ausnahmen (sie ist nicht von 'Mama'), also wird die Regel angewendet, und die Nachricht wird in den Ordner 'Katzen' verschoben.
  
Die folgende Abbildung zeigt, wie die Regel auf eine eingehende E-Mail-Nachricht angewendet wird.
  
**Abbildung 2. Eingehende Nachricht wird durch eine Regel verarbeitet.**

![Eine Illustration, die zeigt, wie eine neue Nachricht von einem Kollegen an die Verteilungsliste gesendet wird. Die Nachricht erfüllt alle Bedingungen und keine der in der Regel definierten Ausnahmen und wird in den Ordner "Cats" verschoben.](media/Ex15_Rules_RuleEvaluationSample.png)
  
## <a name="blocking-senders"></a>Blockieren von Absendern
<a name="bk_Blocking"> </a>

Obwohl Sie eine Regel erstellen können, die alle e-Mail-Nachrichten von einem bestimmten Absender in den Junk-e-Mailordner verschieben möchten, können Sie auch hierzu mithilfe der Liste blockierter Absender in den Junk-e-Mail-Optionen. Da es ein Grenzwert, wie viele Regeln, die ein Benutzer ausführen kann besteht, ist es sinnvoll, verwenden Sie die Liste der blockierten Absender. Sie können [bestimmten e-Mail-Adressen aus der Liste blockierter Absender hinzufügen oder entfernen](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md) , indem Sie die [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS-Vorgang. Beachten Sie, dass in der Reihenfolge für EWS der Liste blockierter Absender Zugriff auf das Postfach des Benutzers aus der e-Mail-Adresse eine e-Mail-Nachricht enthalten muss, die Sie hinzufügen oder entfernen möchten. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_InThisSection"> </a>

- [Verwalten von Posteingangsregeln mithilfe der EWS in Exchange](how-to-manage-inbox-rules-by-using-ews-in-exchange.md)
    
- [Hinzufügen und Entfernen von e-Mail-Adressen aus der Liste blockierter Absender mithilfe der EWS in Exchange](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [GetInboxRules-Vorgang](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [UpdateInboxRules-Vorgang](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    
- [MarkAsJunk Operation](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)
    

