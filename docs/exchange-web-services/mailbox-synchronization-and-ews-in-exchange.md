---
title: Postfach-Synchronisierung und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: Informieren Sie sich die Funktionsweise der Postfach-Synchronisierung bei Verwendung von EWS zum Zugreifen auf Exchange.
ms.openlocfilehash: 7bca2f7b754dcceee99e4bc24519f6e4f6423ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757045"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>Postfach-Synchronisierung und EWS in Exchange

Informieren Sie sich die Funktionsweise der Postfach-Synchronisierung bei Verwendung von EWS zum Zugreifen auf Exchange.
  
EWS in Exchange werden zwei Arten der Synchronisierung Postfachinhalt abgerufen und in der Inhalt von Postfächern geändert:
  
- Synchronisierung von Ordnern
    
- Element-Synchronisierung
    
In diesem Artikel lernen Sie sowohl Synchronisierungstypen, Funktionsweise der Synchronisierung, Entwurfsmuster Synchronisierung und bewährte Methoden Synchronisierung.
  
## <a name="folder-and-item-synchronization"></a>Ordner- und Synchronisierung
<a name="bk_typesofsyncs"> </a>

Synchronisierung Ordner synchronisiert wird eine Ordnerstruktur oder Ordner-Hierarchie. Element-Synchronisierung synchronisiert wird, die Elemente in einem Ordner. Beim Synchronisieren von Elementen müssen Sie jeden Ordner im Postfach unabhängig voneinander zu synchronisieren. EWS oder die EWS Managed API können in Ihrer Anwendung Sie die Ordner und Element-Synchronisierung implementieren.
  
**In Tabelle 1. EWS-Vorgänge und EWS Managed API-Methoden zum Synchronisieren von Ordnern und Elementen**

|**EWS-Vorgang**|**EWS Managed API-Methode**|
|:-----|:-----|
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Der Bereich der Synchronisierung, die auftritt, unterscheidet sich je nachdem, ob es einen anfänglichen oder eine laufende Sync, wie folgt:
  
- Eine anfängliche Synchronisierung synchronisiert alle Ordner oder Elemente auf dem Server an den Client. Nach der ersten Synchronisierung hat der Client einen Synchronisierungsstatus, den für zukünftige Synchronisierungen gespeichert. Der Synchronisierungsstatus stellt alle Änderungen auf dem Server, den der Server an den Client kommuniziert.
    
- Laufende Synchronisierung synchronisieren Sie alle Elemente oder Ordner, die hinzugefügt, gelöscht oder seit der vorherigen Synchronisierung geändert wurden. Der Server nutzt die Synchronisierungsstatus die Änderungen an den Client während der laufenden Synchronisierung Schleifen Unwichtigstes berechnet werden sollen.
    
Jede Synchronisierungsmethode oder der Vorgang gibt eine Liste der Änderungen nicht, den Ordner oder die Nachricht, die geändert zurück. Über die folgenden Änderungstypen werden Änderungen an Elemente und Ordner aufgeführt:
  
- Erstellen – Gibt an, dass eine neues Element oder einen Ordner auf dem Client erstellt werden soll.
    
- Update – Gibt an, dass eines Elements oder Ordners auf dem Client geändert werden soll.
    
- Löschen – Gibt an, dass eines Elements oder Ordners auf dem Client gelöscht werden soll.
    
- ReadStateChange für EWS oder ReadFlagChange für die EWS Managed API – gibt an, dass, die den Zustand "gelesen" des Artikels aus ungelesene zum Lesen oder Lesen auf ungelesene geändert hat.
    
In Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2010 SP2-Versionen werden Elemente und Ordner in der Reihenfolge von absteigend zurückgegeben. In früheren Versionen von Exchange werden Elemente und Ordner vom ältesten zum neuesten zurückgegeben.
  
## <a name="how-does-ews-synchronization-work"></a>Funktionsweise der EWS-Synchronisierung?
<a name="bk_howdoesitwork"> </a>

Kurz gesagt, wenn Sie ein Postfach zum ersten Mal synchronisiert sind, verwenden Sie das Verfahren wie in Abbildung 1 dargestellt. Obwohl Sie andere [Synchronisierung Entwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)verwenden können, sollten diesem Ansatz für skalierbare Applications.
  
**Abbildung 1. Entwurfsmuster für die anfängliche Synchronisierung**

![Abbildung des Entwurfsmusters für die anfängliche Synchronisierung. Der Client ruft "SyncFolderHierarchy" und "Load" oder "GetItem" zum Abrufen der Ordner und dann "SyncFolderItems" und "LoadPropertiesForItems" oder "GetItem" zum Abrufen der Elemente in allen Ordnern auf.](media/Exchange2013_SyncInitial.png)
  
Wenn Sie eine vorhandene Synchronisierungsstatus auf dem Client zum verwenden um ein Postfachs zu synchronisieren, wird empfohlen, dass Sie das Entwurfsmuster implementieren, wie in Abbildung 2 dargestellt. 
  
**Abbildung 2. Laufende Synchronisierung Entwurfsmuster**

![Abbildung des Entwurfsmusters für die fortlaufende Synchronisierung. Ein Client empfängt eine Benachrichtigung, ruft anschließend "SyncFolderHierarchy" oder "SyncFolderItems" auf, ruft die Eigenschaften ab, aktualisiert dann den Client oder aktualisiert das Lesekennzeichen auf dem Client.](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>Entwurfsmuster für die Synchronisierung
<a name="bk_syncpatterns"> </a>

Sie können eine der zwei Entwurfsmuster für die Synchronisierung in der Anwendung, um Ihre Postfächer auf dem aktuellen Stand zu halten: Benachrichtigung-basierte Synchronisation oder der Synchronisierung nur Ansatz.
  
Benachrichtigung-basierte Synchronisierung nutzt wie in [Abbildung 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork)dargestellt zu warnen, den Clients zum Tätigen eines Anrufs auf die EWS Managed API [SyncFolderItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) oder [SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) -Methode oder die EWS [SyncFolderHierarchy Benachrichtigungen ](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)oder [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) Vorgänge. Diese Art von Synchronisierung wird im Allgemeinen für skalierbare Applikationen empfohlen, aber möglicherweise nicht am besten für jeden Benutzer. Benachrichtigung-basierte Synchronisation hat die folgenden Vorteile: 
  
- Benachrichtigungen werden optimiert, um Anrufe an die Exchange-Back-End-Datenbank zu reduzieren. Ereignis Warteschlangen und Abonnements werden von den Mailbox-Server (oder den Clientzugriffsserver in Exchange 2010 und Exchange 2007) verwaltet. die Verwaltung der Ereignisse und Abonnements verwendet jedoch weniger Ressourcen als die Alternative häufigere Synchronisierung Anrufe an die Exchange-Datenbank. Darüber hinaus muss Exchange bestimmte [Richtlinien Drosselung](ews-throttling-in-exchange.md) für Benachrichtigungen und Abonnements, um Konsum von Ressourcen zu schützen. 
    
Es gibt jedoch auch einige Nachteile der Verwendung von Benachrichtigung-basierte Synchronisation:
  
- Benachrichtigungen sind lauten, da die meisten Szenarien mehrere Benachrichtigungen für einen Benutzer beabsichtigt beinhalten. Dies gilt insbesondere für den Ordner Kalender. Beispielsweise bei eine Besprechungsanfrage empfangen wird, werden mehrere Element- und Benachrichtigungen erstellt einschließlich einer benachrichtigungs an das Element und ein weiteres so ändern Sie das Element erstellen. Eine Möglichkeit zum Abwehren von diesen Nachteil ist um eine Verzögerung von einigen Sekunden in Ihren Anruf [Laden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx), [LoadPropertiesForItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx), [GetItem](http://msdn.microsoft.com/en-us/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)oder [GetFolder](http://msdn.microsoft.com/en-us/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx) zu erstellen. Im Fall einer Besprechungsanfrage Wenn Sie Anrufe an die **GetItem** Operation sofort vorgenommen haben Sie durch Aufrufen von das Element und ein weiteres so ändern Sie das Element erstellen möglicherweise. Rufen Sie stattdessen durch verzögern des Anrufs, Sie können den **GetItem** -Vorgang und die Änderungen, die die Erstellung und die Änderung des Elements gleichzeitig umfassen erhalten möchten. 
    
- Benachrichtigungen werden in der Warteschlange auf dem Postfachserver und Abonnements auf dem Postfachserver gespeichert sind. Wenn der Postfachserver, der das Abonnement verwaltet nicht verfügbar ist, verlieren Sie alle neuen Benachrichtigungen, Ihr Postfach wird nicht synchronisieren und Sie erneut auf die Benachrichtigungen abonnieren müssen.
    
- Sie müssen zum Planen von Strategien zur Risikominderung, Benachrichtigungen fehl. Auf diese Weise die zweite Methode, die Synchronisierung nur Entwurfsmuster, da es nur erfordert, dass der Client den Synchronisierungsstatus verwalten ausfallsicherer als Benachrichtigung-basierte Synchronisierung wird – es sind keine Probleme mit Affinität an den Postfachserver Verwalten von Abonnements aus.
    
Wenn implementiert wie empfohlen, stützt sich auf das Benachrichtigung-basiertes Abonnement Entwurfsmuster: 
  
- Benachrichtigungen zu bestimmen, *Wenn* die Daten geändert. 
    
- EWS Managed API, **SyncFolderHierarchy** oder **SyncFolderItems** -Methoden oder die EWS- **SyncFolderHierarchy** oder **SyncFolderItems** Vorgänge zu bestimmen, *welche* geändert werden soll, die Anzahl der zurückgegebenen Sync Ereignisse optimieren. Ein neues Element erstellt, aktualisiert oder gelöscht wurde? Das ist, müssen Sie wissen, von diesen Methoden verlassen Sie sich nicht auf diese Eigenschaft eine Liste der Änderungen. (Keine **GetItem** oder ein **LoadPropertiesForItems** Anruf auf alle Elemente oder Ordner zurückgegeben werden). 
    
- Mit der **Last** oder **LoadPropertiesForItems** in die EWS Managed API oder die EWS **GetItem** Operation um zu bestimmen, *wie* die Daten geändert und zum Abrufen von Eigenschaften vom Server nach Bedarf organisieren Batchanforderungen basiert Klicken Sie auf die Menge der Daten, die zurückgegeben wird. Einen Vergleich der Eigenschaften auf dem Client und diese nur zurückgegebene aus dem Server, und schließlich das Erstellen, löschen oder Ändern von des Elements oder Ordners auf dem Client folgt. 
    
Der Synchronisierung nur Ansatz beruht vollständig auf die Methoden **SyncFolderItems** und **SyncFolderHierarchy** EWS Managed API oder **SyncFolderHierarchy** oder **SyncFolderItems** EWS-Vorgänge, die Sie entweder aufrufen können kontinuierlich oder als ein Ereignis. Vor- und Nachteile dieser Option sowie sind. Der Synchronisierung nur Ansatz ist stabiler, weil der Synchronisierungsstatus auf dem Client auf Postfachebene gespeichert wird und eine eindeutige Beziehung zwischen den Synchronisierungsstatus und alle auf der Postfachserver, der die Benachrichtigungsabonnement verwaltet nicht erforderlich ist. Der Synchronisierung Ansatz kann einen Postfach Failover aufgrund dessen Unabhängigkeit vom Postfachserver überstehen. Der Synchronisierung Ansatz erhöht jedoch Wartezeit für den Benutzer, da Elemente für eine einzelne Intervallen oder zeitweilig unterbrochenen synchronisiert werden – nicht in Echtzeit beim Eintreffen Elemente. Dieser Ansatz ist auch teurer, da Sie tätigen Anrufe an die Exchange-Datenbank, wenn es möglich ist, dass keine Änderungen aufgetreten sind. 
  
## <a name="synchronization-best-practices"></a>Bewährte Methoden für Synchronisierung
<a name="bk_bestpractices"> </a>

Extrem skalierbar handelt wird empfohlen, dass Sie die folgenden bewährten Methoden, um die Postfächer in Ihrer Anwendung synchronisieren anwenden:
  
- Wenn die EWS Managed API **SyncFolderItems** oder **SyncFolderHierarchy** -Methode aufrufen, verwenden Sie den _IdOnly_ -Wert für den Parameter _PropertySet_ oder wenn die EWS mit **SyncFolderHierarchy** oder **SyncFolderItems** Vorgänge verwenden Sie den **IdOnly** -Wert für den [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) -Wert um Anrufe an die Exchange-Datenbank zu verringern. Rufen Sie die weitere Eigenschaften, die Sie in den Eigenschaftensatz, der **SyncFolderItems** oder **SyncFolderHierarchy** anfordern, Weitere Back-End-erstellten Anrufe. Ein neuer Anruf RPC erfolgt für jedes Eigenschaftswert angefordert, während nur ein RPC-Aufruf ausgeführt wird, zum Abrufen aller für eine Anforderung - unabhängig davon, die Anzahl der Ergebnisse auf Bericht **Artikelnummern ein.** . Damit eine **IdOnly** -Anforderung während führt zu eine Eigenschaft Eigenschaftensammlung Anforderung für den Betreff und der Absender in drei Datenbank Aufrufen einer Datenbankaufruf, führt: eines für den **Betreff**, den **Absender**und die **ItemId**.
    
- Rufen Sie nicht die EWS Managed API **Laden** oder **LoadPropertiesForItems** Methoden EWS **GetItem** oder der **GetFolder** -Vorgänge, für jedes Element in einer Antwort Synchronisierung. Analysieren Sie stattdessen die Ergebnisse; Änderungen am Status von Änderungen gesucht, die alle Eigenschaften abgerufen werden sollen, die keine erfordern wie gelesen werden. Wenn eine Antwort auf eine Änderung Zustand "gelesen" enthält, aktualisieren Sie einfach das Flag auf dem Client, und Sie fertig sind. keine Notwendigkeit, alle Elementeigenschaften erhalten möchten. Und stellen Sie sicher, dass Sie duplizieren keine Aufwand stammt vom selben Client ändern. Angenommen, wenn die Synchronisierung Antwort das Löschen eines Elements enthält und der Löschvorgang auf dem lokalen Client erfolgt, müssen Sie erneut Löschen der Nachricht oder alle Eigenschaften für dieses Element abrufen. 
    
- Vermeiden Sie die erste gedrosselt, die folgenden Schritte durch:
    
  - Wenn Sie die EWS Managed API **LoadPropertiesForItems** -Methode oder die EWS **GetItem** Operation die Elemente in einem Batch abgerufen aufrufen, führen Sie nicht zu viele Elemente in Ihrer Anforderung batch; Andernfalls erhalten Sie möglicherweise [gedrosselt](ews-throttling-in-exchange.md). Es wird empfohlen, dass Sie 10 Elemente pro Batch einschließen.
    
  - Stellen Sie nicht zu viele Anfragen zu kurz Zeit. Dies wird auch dazu führen, dass Einschränkung, und die Antwortzeit, anstatt kürzen Sie ihn. 
    
  - Wenn Sie Elemente Batchverarbeitung, batch-alle Elemente mit den gleichen Werten für die Attribute **Id** und **ChangeKey** des [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Elements. 
    
  - Wenn Sie die Schritte aus gedrosselt erhalten möchten, beenden Sie zusenden. Erneutes Senden Anfragen wird die Wiederherstellung Mühe verlängert. Stattdessen warten Sie auf der Rückseite Zeit an, die ablaufen aus, und versuchen Sie erneut Ihr Synchronisierungsanfragen zu senden.
    
- Je nach Typ der [Benachrichtigungsereignis](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes) empfangen: 
    
  - Rufen Sie für Ereignisse **NewMail** oder **geändert** die EWS Managed API **SyncFolderItems** -Methode oder der EWS- **SyncFolderItems** Vorgang ein, da Benachrichtigungen keine **ChangeKey**bereitstellen und Benachrichtigungen nicht Zustand "gelesen Legende" ändert.
    
  - Für **Gelöschte** Ereignisse Wenn die Benachrichtigungsabonnement vor den vorherigen Sync aktiv war, löschen Sie einfach das Ereignis lokal. Sie müssen nicht die EWS Managed API **SyncFolderItems** -Methode oder der Vorgang EWS **SyncFolderItems** unmittelbar nach der Löschvorgang aufrufen. 
    
  - Wenn ein Ereignis **geändert** von einer Änderung Zustand "gelesen" verursacht wurde, nicht rufen Sie die EWS Managed API **LoadPropertiesForItems** -Methode oder die EWS **GetItem** Operation auf, ändern Sie einfach die Kennzeichen für das Element. 
    
- Bei der Synchronisierung von Kalenderdaten gehen Sie wie folgt vor:
    
  - Verwenden Sie einen ähnlichen Synchronisierung Benachrichtigung-basierten Ansatz. Da **SyncFolderItem** keine Kalender Logik enthält, verwenden Sie die EWS Managed API [FindAppointments](http://msdn.microsoft.com/en-us/library/dd633767%28v=exchg.80%29.aspx) -Methode oder die EWS- [Vorgang FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit das [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -Element Termine zwischen zwei Datumsangaben anzeigen und dann Rufen Sie die EWS Managed API **LoadPropertiesForItems** -Methode oder die EWS **GetItem** Operation, die Elementeigenschaften für das Kalenderelement abgerufen. 
    
  - Führen Sie Abrufe nicht mit der EWS Managed API **FindAppointments** -Methode oder der Vorgang EWS **FindItem** und ein **CalendarView** -Element. 
    
- Bei der Synchronisierung von Suchordnern:
    
  - Verwenden Sie einen ähnlichen Synchronisierung Benachrichtigung-basierten Ansatz. 
    
  - Verwenden Sie Benachrichtigungen, um zu bestimmen, wann Daten ändert.
    
  - Da Sie in einem Suchordner **SyncFolderItem** verwenden können, verwenden Sie eine sortierte und ausgelagerten EWS Managed API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode oder EWS **FindItem** Vorgang mit dem [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) und [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) -Element, um zu bestimmen Was geändert. 
    
  - Verwenden Sie die EWS Managed API **LoadPropertiesForItems** -Methode oder die EWS **GetItem** Operation zum Abrufen von Daten. 
    
## <a name="filtered-synchronization"></a>Gefilterte Synchronisierung
<a name="bk_filteredsync"> </a>

Die EWS Managed API **SyncFolderItems** -Methode und der EWS- **SyncFolderItems** -Vorgang können Sie bestimmte Elemente, basierend auf deren Artikelnummern ein., durch Festlegen des _IgnoreItemIds_ -Parameters in die EWS Managed API oder das [ignorieren](http://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx) ignorieren Element in der Exchange-Webdienste. Dies ist ideal, wenn, beispielsweise Personen in einer e-Mail-Nachricht für alle Benutzer im Unternehmen gesendet Antworten beginnen. 
  
Vielleicht, kann ich meine Benachrichtigungen Filtern (und daher nur auslösen Synchronisierung) Wenn bestimmte Eigenschaften geändert werden? Obwohl, die angemessene, scheint, da Benachrichtigungsabonnements auf die Art der Änderung basieren (erstellen, aktualisieren und löschen), und nicht die Eigenschaft aktualisiert wird, kann nicht gefiltert werden Benachrichtigungen auf diese Weise. Stattdessen können Sie Folgendes:
  
- Verwenden Sie das Entwurfsmuster Benachrichtigung-basiertes Abonnement.
    
- Rufen Sie die EWS Managed API **SyncFolderItems** und **SyncFolderHierarchy** Methoden mehrmals mit dem _PropertySet_ -Parameter auf _IdOnly_ festgelegt, um Ihre Synchronisierungsstatus aktuellen Datensatz zu machen. Oder wenn EWS verwenden möchten, rufen Sie die **SyncFolderHierarchy** und **SyncFolderItems** Vorgänge wiederholt mit dem Wert **BaseShape** **IdOnly**. 
    
- Verwerfen die Antwort (durch nicht analysieren oder führen Sie eine beliebige Eigenschaft Vergleiche).
    
- Verwenden Sie die EWS Managed API **FindItems** -Methode oder der Vorgang EWS **FindItem** und Sortieren und Seite der Elemente im gefilterten Bereich vorab gefüllt, die Sie interessieren. 
    
- Verwenden der Synchronisierungsstatus weiterhin rufen Sie die EWS Managed API **SyncFolderItems** -Methode oder der Vorgang EWS **SyncFolderItems** , aber nur die Änderungen im Satz gefilterte Element überwachen. Wenn neue Elemente erstellt wurden, müssen Sie überprüfen, ob diese neue Elemente innerhalb der gefilterten Bereich befinden. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_filteredsync"> </a>

- [Synchronisieren von Ordnern in Exchange mithilfe der Exchange-Webdienste](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronisieren von Elementen mithilfe von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [Fehlerbehandlung Synchronisierung-bezogene in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [SyncFolderItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy-Vorgang](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [SyncFolderItems-Vorgang](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

