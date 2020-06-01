---
title: Synchronisierung von Postfächern und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: Erfahren Sie, wie die Postfachsynchronisierung funktioniert, wenn Sie EWS zum Zugreifen auf Exchange verwenden.
localization_priority: Priority
ms.openlocfilehash: 5dc700c7feb9fce6121a27ee73fc1a58e88e643a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456260"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>Synchronisierung von Postfächern und EWS in Exchange

Erfahren Sie, wie die Postfachsynchronisierung funktioniert, wenn Sie EWS zum Zugreifen auf Exchange verwenden.
  
EWS in Exchange verwendet zwei Synchronisierungsarten zum Abrufen von Postfachinhalten und Änderungen an Postfachinhalten:
  
- Synchronisierung von Ordnern
    
- Synchronisierung von Elementen
    
In diesem Artikel erfahren Sie mehr über die beiden Synchronisierungsarten, die Funktionsweise der Synchronisierung, Entwurfsmuster für die Synchronisierung sowie bewährte Methoden für die Synchronisierung.
  
## <a name="folder-and-item-synchronization"></a>Synchronisierung von Ordnern und Elementen
<a name="bk_typesofsyncs"> </a>

Bei der Ordnersynchronisierung wird eine Ordnerstruktur oder Ordnerhierarchie synchronisiert. Bei der Elementsynchronisierung werden die Elemente in einem Ordner synchronisiert. Wenn Sie Elemente synchronisieren, müssen Sie jeden Ordner im Postfach separat synchronisieren. Sie können EWS oder die verwaltete EWS-API in Ihrer Anwendung verwenden, um sowohl die Ordner- als auch die Elementsynchronisierung zu implementieren.
  
**Tabelle 1: EWS-Vorgänge und von EWS verwaltete API-Methoden zum Synchronisieren von Ordnern und Elementen**

|**EWS-Vorgang**|**Von EWS verwaltete API-Methode**|
|:-----|:-----|
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Der Umfang der ausgeführten Synchronisierung variiert in Abhängigkeit davon, ob es sich um eine erste oder eine fortlaufende Synchronisierung handelt:
  
- Bei einer ersten Synchronisierung werden alle Ordner oder Elemente auf dem Server auf den Client synchronisiert. Nach der ersten Synchronisierung weist der Client einen Synchronisierungsstatus auf, der für zukünftige Synchronisierungen gespeichert wird. Der Synchronisierungsstatus stellt alle Änderungen auf dem Server dar, die der Server an den Client kommuniziert hat.
    
- Bei fortlaufenden Synchronisierungen werden alle Elemente oder Ordner synchronisiert, die hinzugefügt, gelöscht oder seit der vorherigen Synchronisierung geändert wurden. Der Server verwendet den Synchronisierungsstatus, um die Änderungen zu berechnen, die während der laufenden Synchronisierungsschleifen an den Client gemeldet werden.
    
Jede Synchronisierungsmethode oder jeder Vorgang gibt eine Liste von Änderungen zurück, und nicht den eigentlichen Ordner oder die Nachricht, der bzw. die geändert wurde. Änderungen an Elementen und Ordnern werden anhand der folgenden Änderungstypen gemeldet:
  
- Erstellen – Gibt an, dass ein neues Element oder ein neuer Ordner auf dem Client erstellt werden soll.
    
- Aktualisieren – Gibt an, dass ein neues Element oder ein neuer Ordner auf dem Client geändert werden soll.
    
- Löschen – Gibt an, dass ein Element oder ein Ordner auf dem Client gelöscht werden soll.
    
- ReadStateChange für EWS oder ReadFlagChange für die verwaltete EWS-API – Gibt an, dass der Lesestatus des Elements geändert wurde, entweder von ungelesen zu gelesen oder von gelesen zu ungelesen.
    
In Exchange Online, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2010 SP2 werden Elemente und Ordner in der Reihenfolge vom neuesten zum ältesten Element/Ordner zurückgegeben. In früheren Versionen von Exchange werden Elemente und Ordner in der Reihenfolge vom ältesten zum neuesten Element/Ordner zurückgegeben.
  
## <a name="how-does-ews-synchronization-work"></a>Wie funktioniert die EWS-Synchronisierung?
<a name="bk_howdoesitwork"> </a>

Kurz zusammengefasst: Wenn Sie ein Postfach zum ersten Mal synchronisieren, verwenden Sie den Vorgang, wie in Abbildung 1 dargestellt. Sie können zwar andere [Synchronisierungsentwurfsmuster](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) verwenden, dieser Ansatz wird jedoch für skalierbare Anwendungen empfohlen.
  
**Abbildung 1. Entwurfsmuster für erste Synchronisierung**

![Abbildung des Entwurfsmusters für die anfängliche Synchronisierung. Der Client ruft "SyncFolderHierarchy" und "Load" oder "GetItem" zum Abrufen der Ordner und dann "SyncFolderItems" und "LoadPropertiesForItems" oder "GetItem" zum Abrufen der Elemente in allen Ordnern auf.](media/Exchange2013_SyncInitial.png)
  
Wenn Sie einen vorhandenen Synchronisierungsstatus auf dem Client verwenden, um ein Postfach zu synchronisieren, wird empfohlen, dass Sie das in Abbildung 2 dargestellte Entwurfsmuster implementieren. 
  
**Abbildung 2. Entwurfsmuster für fortlaufende Synchronisierung**

![Abbildung des Entwurfsmusters für die fortlaufende Synchronisierung. Ein Client empfängt eine Benachrichtigung, ruft anschließend "SyncFolderHierarchy" oder "SyncFolderItems" auf, ruft die Eigenschaften ab, aktualisiert dann den Client oder aktualisiert das Lesekennzeichen auf dem Client.](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>Synchronisierungsentwurfsmuster
<a name="bk_syncpatterns"> </a>

Sie können eines der beiden Synchronisierungsentwurfsmuster in Ihrer Anwendung verwenden, um Ihre Postfächer auf dem neuesten Stand zu halten: benachrichtigungsbasierte Synchronisierung oder der Ansatz, bei dem nur eine Synchronisierung ausgeführt wird.
  
Die benachrichtigungsbasierte Synchronisation, wie in [Abbildung 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork) dargestellt, basiert auf Benachrichtigungen, um den Client darauf aufmerksam zu machen, dass er die Methoden [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) oder [ SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) der verwalteten EWS-API oder die Vorgänge [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) oder [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) von EWS aufrufen soll. Diese Art von Synchronisierung wird im Allgemeinen für skalierbare Anwendungen empfohlen, ist aber möglicherweise nicht für alle Benutzer optimal geeignet. Die benachrichtigungsbasierte Synchronisierung weist die folgenden Vorteile auf: 
  
- Benachrichtigungen sind so optimiert, dass die Anzahl von Aufrufen der Back-End-Exchange-Datenbank reduziert wird. Ereigniswarteschlangen und Abonnements werden vom Postfachserver (bzw. vom Clientzugriffsserver in Exchange 2010 und Exchange 2007) verwaltet. Die Verwaltung der Ereignisse und Abonnements verwendet jedoch weniger Ressourcen als die Alternative, die in häufigeren Synchronisierungsaufrufen der Exchange-Datenbank besteht. Exchange verfügt darüber hinaus über bestimmte [Einschränkungsrichtlinien](ews-throttling-in-exchange.md) für Benachrichtigungen und Abonnements, um den Verbrauch von Ressourcen zu schützen. 
    
Es gibt bei der benachrichtigungsbasierten Synchronisierung jedoch auch einige Nachteile:
  
- Benachrichtigungen sind sehr komplex, da in den meisten Szenarien mehrere Benachrichtigungen für eine Beabsichtigung des Benutzers verwendet werden. Dies gilt insbesondere für den Ordner „Kalender“. Wenn beispielsweise eine einzelne Besprechungsanfrage empfangen wird, werden mehrere Element- und Ordnerbenachrichtigungen erstellt, einschließlich einer Benachrichtigung zum Erstellen des Elements sowie eine weitere Benachrichtigung zum Ändern des Elements. Eine Möglichkeit, um diesen Nachteil zu verhindern, besteht darin, eine Verzögerung von ein paar Sekunden in den [Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx)-, [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)-, [GetItem](https://msdn.microsoft.com/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)- oder [GetFolder](https://msdn.microsoft.com/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx)-Aufruf einzubauen. Wenn Sie im Falle einer Besprechungsanfrage unmittelbar Aufrufe des **GetItem**-Vorgangs vorgenommen haben, haben Sie vielleicht einen Aufruf zum Erstellen des Elements und einen weiteren zum Ändern des Elements. Durch Verzögern des Aufrufs können Sie stattdessen den **GetItem**-Vorgang einmal aufrufen und dadurch gleichzeitig die Änderungen abrufen, die mit dem Erstellen und Ändern des Elements einhergehen. 
    
- Benachrichtigungen werden auf dem Postfachserver in der Warteschlange platziert, und Abonnements werden auf dem E-Mail-Server gespeichert. Wenn der Postfachserver, der das Abonnement verwaltet, nicht verfügbar ist, gehen alle neuen Benachrichtigungen verloren, das Postfach wird nicht synchronisiert, und Sie müssen die Benachrichtigungen erneut abonnieren.
    
- Sie müssen Lösungsstrategien planen für den Fall, dass Benachrichtigungen fehlschlagen. Der zweite Ansatz, das Entwurfsmuster, das nur die Synchronisierung umfasst, ist daher stabiler als die benachrichtigungsbasierte Synchronisierung, da hier der Client nur den Synchronisierungsstatus aufrechterhalten muss – es gibt keine Probleme mit Affinität zum Postfachserver, der das Abonnement verwaltet.
    
Wenn die benachrichtigungsbasierte Synchronisierung wie empfohlen implementiert wird, basiert dieses Entwurfsmuster auf Folgendem: 
  
- Benachrichtigungen, um zu ermitteln, *wann* die Daten geändert wurden. 
    
- Auf den Methoden **SyncFolderHierarchy** oder **SyncFolderItems** der verwalteten EWS-API oder auf den Vorgängen **SyncFolderHierarchy** oder **SyncFolderItems** von EWS, um zu bestimmen, *was* geändert wurde, wodurch die Anzahl zurückgegebener Synchronisierungsereignisse optimiert wird. Wurde ein neues Element erstellt, aktualisiert oder gelöscht? Das ist alles, was Sie von diesen Methoden wissen müssen. Sie sind für die Eigenschaftenlisten von Änderungen nicht auf die Methoden angewiesen. (Führen Sie keinen **GetItem**- oder **LoadPropertiesForItems**-Aufruf für alle zurückgegebenen Elemente oder Ordner aus). 
    
- Verwenden Sie die Methoden **Load** oder **LoadPropertiesForItems** in der verwalteten EWS-API oder den **GetItem**-Vorgang von EWS, um zu ermitteln *wie* die Daten geändert wurden und um bei Bedarf Eigenschaften vom Server abzurufen, wodurch Batchanforderungen basierend auf der Datenmenge organisiert werden, die zurückgegeben werden. Darauf folgt ein Vergleich der Eigenschaften auf dem Client mit denjenigen, die soeben vom Server zurückgegeben wurden und letztendlich das Erstellen, Löschen oder Ändern des Elements oder Ordners auf dem Client. 
    
Der Ansatz, bei dem nur die Synchronisierung ausgeführt wird, basiert vollständig auf den Methoden **SyncFolderItems** und **SyncFolderHierarchy** der verwalteten EWS-API oder auf den EWS-Vorgängen **SyncFolderHierarchy** oder **SyncFolderItems**, die Sie entweder fortlaufend oder als zeitlich festgelegtes Ereignis aufrufen. Auch für diesen Ansatz gibt es Vor- und Nachteile. Der Ansatz, bei dem nur die Synchronisierung ausgeführt wird, ist stabiler, weil der Synchronisierungsstatus auf dem Client unter der Postfachebene gespeichert wird und keine eindeutige Beziehung zwischen dem Synchronisierungsstatus und einem Postfachserver erforderlich ist, der das Benachrichtigungsabonnement verwaltet. Die Synchronisierungsansatz kann aufgrund seiner Unabhängigkeit vom Postfachserver ein Postfachfailover überleben. Durch den Synchronisierungsansatz wird jedoch die Latenz für den Benutzer erhöht, da Elemente zeitgesteuert oder zeitweilig synchronisiert werden und nicht in Echtzeit beim Eintreffen von Elementen. Dieser Ansatz ist auch teurer, da Sie Aufrufe der Exchange-Datenbank ausführen, auch wenn möglicherweise keine Änderungen aufgetreten sind. 
  
## <a name="synchronization-best-practices"></a>Bewährte Methoden für die Synchronisierung
<a name="bk_bestpractices"> </a>

Für stark skalierbare Anwendungen empfehlen wir, dass Sie die folgenden bewährten Methoden zum Synchronisieren von Postfächern in Ihrer Anwendung anwenden:
  
- Verwenden Sie beim Aufrufen der **SyncFolderItems**- oder **SyncFolderHierarchy**-Methode der verwalteten EWS-API den Wert _IdOnly_ für den _propertySet_-Parameter, oder verwenden Sie bei Verwendung der EWS-Vorgänge **SyncFolderHierarchy** oder **SyncFolderItems** den Wert **IdOnly** für den Wert [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx), um Aufrufe der Exchange-Datenbank zu reduzieren. Je mehr Eigenschaften Sie im Eigenschaftensatz des **SyncFolderItems**- oder **SyncFolderHierarchy**-Aufrufs anfordern, desto mehr Back-End-Aufrufe werden erstellt. Für jeden angeforderten Eigenschaftenwert wird ein neuer RPC-Aufruf erstellt, wohingegen nur ein RPC-Aufruf vorgenommen wird, um alle **ItemIds** einer Anforderung abzurufen – unabhängig von der Anzahl zu meldender Ergebnisse. Eine **IdOnly**-Anforderung führt also zu einem Datenbankaufruf, wohingegen eine Anforderung eines Eigenschaftenbehälters für den Betreff und den Absender zu drei Datenbankaufrufen führt: einer für **Subject**, einer für **Sender** und einer für **ItemId**.
    
- Rufen Sie nicht die Methoden **Load** oder **LoadPropertiesForItems** der verwalteten EWS-API oder die EWS-Vorgänge **GetItem** oder **GetFolder** für jedes Element in einer Synchronisierungsantwort auf. Analysieren Sie stattdessen die Ergebnisse; suchen Sie nach Änderungen, für die nicht alle Eigenschaften abgerufen werden müssen, z. B. Änderungen des Lesestatus. Wenn eine Antwort eine Änderung des Lesestatus enthält, aktualisieren Sie einfach die Kennzeichnung auf dem Client und schon sind Sie fertig. Sie müssen nicht alle Elementeigenschaften abrufen. Und stellen Sie sicher, dass Sie sich nicht zusätzlichen Aufwand machen, indem Sie Änderungen erstellen, die vom selben Client stammten. Wenn die Synchronisierungsantwort beispielsweise das Löschen eines Elements enthält, und das Löschen erfolgte auf dem lokalen Client, so müssen Sie die Nachricht nicht erneut löschen oder alle Eigenschaften für dieses Element abrufen. 
    
- Vermeiden Sie Einschränkungen, indem Sie folgendermaßen vorgehen:
    
  - Wenn Sie die **LoadPropertiesForItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **GetItem** aufrufen, um die Elemente in einem Batch abzurufen, fügen Sie nicht zu viele Elemente in Ihre Anforderung ein; andernfalls kommt es zu einer [Drosselung](ews-throttling-in-exchange.md). Wir empfehlen, 10 Elemente pro Batch einzuschließen.
    
  - Stellen Sie nicht zu viele Anforderungen in zu kurzer Zeit. Dies führt auch zu einer Drosselung und zu einer längeren Reaktionszeit. 
    
  - Bei der Batchverarbeitung von Elementen sollten Sie alle Elemente mit denselben Werten für die Attribute **Id** und **ChangeKey** des [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)-Elements in einem Batch zusammenfassen. 
    
  - Wenn es zu einer Einschränkung kommt, beenden Sie das Senden von Anforderungen. Durch erneutes Senden von Anforderungen dauert die Wiederherstellung länger. Warten Sie stattdessen, bis die Sperrzeit abgelaufen ist, und versuchen Sie dann erneut, Ihre Synchronisierungsanforderungen zu senden.
    
- In Abhängigkeit vom Typ des empfangenen [Benachrichtigungsereignisses](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes): 
    
  - Rufen Sie für **NewMail**- oder **Modified**-Ereignisse die **SyncFolderItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **SyncFolderItems** auf, da Benachrichtigungen keinen **ChangeKey** bereitstellen und keine Änderungen des Lesestatus aufrufen.
    
  - Wenn das Benachrichtigungsabonnement vor der vorherigen Synchronisierung aktiv war, können Sie bei **Deleted**-Ereignissen das Ereignis einfach lokal löschen. Sie müssen die **SyncFolderItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **SyncFolderItems** nicht unmittelbar nach dem Löschen aufrufen. 
    
  - Wenn ein **Modified**-Ereignis von einer Änderung des Lesestatus verursacht wurde, rufen Sie nicht die **LoadPropertiesForItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **GetItem** auf, ändern Sie nur die Kennzeichnung des Elements. 
    
- Gehen Sie bei der Synchronisierung von Kalenderdaten wie folgt vor:
    
  - Verwenden Sie einen Ansatz, der der benachrichtigungsbasierten Synchronisierung ähnlich ist. Da **SyncFolderItem** keine Kalenderlogik umfasst, verwenden Sie die [FindAppointments](https://msdn.microsoft.com/library/dd633767%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API oder den EWS-Vorgang [FindItem Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit dem [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)-Element, um Termine zwischen zwei Datumsangaben anzuzeigen, und rufen Sie dann die **LoadPropertiesForItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **GetItem** auf, um die Elementeigenschaften für das Kalenderelement abzurufen. 
    
  - Führen Sie keine Abfragen mithilfe der **FindAppointments**-Methode der verwalteten EWS-API oder des EWS-Vorgangs **FindItem** Vorgang mit einem **CalendarView**-Element durch. 
    
- Bei der Synchronisierung von Suchordnern:
    
  - Verwenden Sie einen Ansatz, der der benachrichtigungsbasierten Synchronisierung ähnlich ist. 
    
  - Verwenden Sie Benachrichtigungen, um zu ermitteln, wann Daten geändert wurden.
    
  - Da Sie **SyncFolderItem** nicht in einem Suchordner verwenden können, verwenden Sie eine sortierte und ausgelagerte [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API oder den EWS-Vorgang **FindItem** mit festgelegtem [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)- und [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx)-Element, um zu ermitteln, was sich geändert hat. 
    
  - Verwenden Sie die **LoadPropertiesForItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **GetItem** zum Abrufen von Daten. 
    
## <a name="filtered-synchronization"></a>Gefilterte Synchronisierung
<a name="bk_filteredsync"> </a>

Dank der **SyncFolderItems**-Methode der verwalteten EWS-API und des EWS-Vorgangs **SyncFolderItems** können Sie bestimmte Elemente basierend auf deren ItemIds ignorieren, indem Sie den _ignoreItemIds_-Parameter in der verwalteten EWS-API oder das [Ignore](https://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx)-Element in EWS ignorieren. Dies ist ideal, wenn Personen in einer E-Mail-Nachricht, die an alle Mitarbeiter im Unternehmen gesendet wurde, allen antworten möchten. 
  
Sie fragen sich vielleicht, ob Sie Benachrichtigungen filtern (und damit nur die Synchronisierung auslösen) können, wenn sich bestimmte Eigenschaften ändern. Dies erscheint zwar sinnvoll, da Benachrichtigungsabonnements auf dem Typ der Änderung (Erstellen, Aktualisieren, Löschen) basieren und nicht auf der aktualisierten Eigenschaft, es ist aber nicht möglich, Benachrichtigungen derart zu filtern. Sie können stattdessen Folgendes tun:
  
- Verwenden Sie das benachrichtigungsbasierte Entwurfsmuster.
    
- Rufen Sie die Methoden **SyncFolderItems** und **SyncFolderHierarchy** der verwalteten EWS-API wiederholt auf, wobei der _propertySet_-Parameter auf _IdOnly_ festgelegt ist, damit Ihr Synchronisierungsstatus aktualisiert wird. Wenn Sie EWS verwenden, rufen Sie die Vorgänge **SyncFolderHierarchy** und **SyncFolderItems** wiederholt auf, wobei der Wert **BaseShape** auf **IdOnly** festgelegt ist. 
    
- Verwerfen Sie die Antwort (analysieren Sie sie nicht, und führen Sie keine Eigenschaftenvergleiche durch).
    
- Verwenden Sie **FindItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **FindItem**, und führen Sie eine Sortierung und Auslagerung aus, um die Elemente in dem gefilterten Bereich, der für Sie relevant ist, vorab zu füllen. 
    
- Verwenden Sie den Synchronisierungsstatus, um dann die **SyncFolderItems**-Methode der verwalteten EWS-API oder den EWS-Vorgang **SyncFolderItems** aufzurufen, aber überwachen Sie nur die Änderungen in dem gefilterten Elementsatz. Wenn neue Elemente erstellt werden, müssen Sie prüfen, ob sich diese neuen Elemente in Ihrem gefilterten Bereich befinden. 
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_filteredsync"> </a>

- [Synchronisieren von Ordnern unter Verwendung von EWS in Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Synchronisieren von Elementen unter Verwendung von EWS in Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [Umgang mit Fehlern im Zusammenhang mit der Synchronisierung in EWS in Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [SyncFolderItems-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy-Vorgang](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [SyncFolderItems-Vorgang](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

