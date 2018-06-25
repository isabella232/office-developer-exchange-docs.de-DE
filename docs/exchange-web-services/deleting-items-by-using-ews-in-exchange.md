---
title: Löschen von Elementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c81e3160-e12b-47e0-b3d6-4be28537f301
description: Erfahren Sie, wie Sie die EWS Managed API verwenden können oder EWS in Exchange zu löschenden Elemente entweder durch Verschieben in den Ordner Gelöschte Elemente oder zu dem Dumpster.
ms.openlocfilehash: a475ebc6677e5f5003cc790a2d4d2b83c513f309
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756846"
---
# <a name="deleting-items-by-using-ews-in-exchange"></a>Löschen von Elementen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie die EWS Managed API verwenden können oder EWS in Exchange zu löschenden Elemente entweder durch Verschieben in den Ordner Gelöschte Elemente oder zu dem Dumpster.
  
Haben Sie schon einmal gebeten, sich selbst Was ist der Unterschied zwischen dem Verschieben von Elementen in den Ordner Gelöschte Objekte, und verschieben sie die Dumpster? Möglicherweise wissen möchten, die verschiedenen Optionen für die Behandlung gelöschter Elemente und wie diese Optionen in Ihrer Anwendung implementiert werden. Exchange-Webdienste (EWS) umfasst drei Optionen für die Behandlung gelöschte Elemente. In diesem Artikel wird hoffentlich von Verwechslungen deaktivieren möchten, zu den Unterschieden zwischen diesen.
  
## <a name="deleting-items---what-are-my-options"></a>Löschen von Elementen - was eigene Optionen sind?
<a name="bk_DeletingItemsOptions"> </a>

Bevor Sie die gesamte Umgebung zum Löschen von Objekten verstehen können, ist es wichtig, den Unterschied zwischen den folgenden erkannt:
  
- Der Ordner Gelöschte Objekte - Wenn Sie Elemente in einem Postfach löschen, wo sie dies ist.
    
- Die Dumpster (auch bekannt als des Ordners wiederherstellbare Elemente) - beim Entfernen von Elementen aus einem Postfach, wo sie dies ist.
    
Abbildung 1 und 2 zeigen, wie der Löschvorgang für Elemente und Ordner in einem Postfach aussieht. 

**Abbildung 1. Prozess zum Löschen von Elementen aus einem Postfach**

![Abbildung Where Elemente zu wechseln, wenn sie gelöscht werden. Gelöschte Elemente werden in den Ordner Gelöschte Objekte verschoben, und klicken Sie dann in den Ordner wiederherstellbare Elemente pro Aufbewahrungsrichtlinie, wo sie ablaufen und Permantently gelöscht werden verschoben werden.](media/Ex_DeleteItems_Source.png)

<br/>

**Abbildung 2. Prozess zum Löschen von Ordnern aus einem Postfach**

![Eine Abbildung, in der dargestellt wird, wie gelöschte Ordner in den Ordner "Gelöschte Elemente" verschoben werden und dann endgültig aus dem Postfach gelöscht werden können](media/Ex_.png)
   
Sie können Elemente und Ordner drei verschiedene Arten löschen, je nachdem, wie "permanent" möchten Sie den Löschvorgang zu.
  
**Tabelle 1: Optionen für das Löschen von Elementen mithilfe der Exchange-Webdienste**

|**Option**|**Was ist los**|
|:-----|:-----|
|Verschieben Sie in den Ordner Gelöschte Elemente  <br/> |Dies ist die geringsten Permanent Möglichkeit, Elemente zu löschen.<br/><br/>Dies entspricht dem setzen ein Blatt Papier im Papierkorb nach Ihren Schreibtisch. Sie können auf einfache Weise Code, wenn Sie wieder benötigen.<br/><br/>Sie können jede [Löschvorgang](deleting-items-by-using-ews-in-exchange.md#bk_howdoIdeleteitems) verwenden, die die Verschiebung der gelöschte Ordner Option zum Ausführen dieser Aktion implementiert.<br/><br/>[MoveItem-Vorgang](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) ( [Item.Move()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx)) oder der [MoveFolder-Vorgang](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) ( [Folder.Move()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx)) können auch um eines Elements oder Ordners in den Ordner Gelöschte Elemente zu verschieben.  <br/> |
|Vorläufiges löschen  <br/> |Das Element wird in den Ordner Löschvorgänge verschoben die Dumpster.<br/><br/>Dies ist wie in den Curbside Container für den Papierkorb leeren. Sie können weiterhin das Element zugreifen, falls erforderlich, sondern nur etwas komplizierter.  <br/><br/>Weitere Informationen zu den Dumpster (auch als "wiederherstellbare Elemente" bezeichnet) und Szenarien wie eDiscovery oder Rechtsstreitigkeiten Haltestatus finden Sie unter [Recoverable Items Folder](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx) auf TechNet.<br/><br/>Weiche Löschvorgänge werden nicht für Applikationen, abzielen Exchange 2007 empfohlen. In Exchange 2007 gekennzeichnete soft Löschvorgänge durch Einstellung etwas auf das Element, um anzugeben, dass es in verschoben werden sollen die Dumpster einiger Zeit.<br/><br/>Durchläufe vorläufiges löschen oder die Suche nach Elementen, die einen weichen über die [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)gelöscht wurden werden in Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2010-Versionen nicht unterstützt.  <br/><br/>**Hinweis**: Ordner nicht weiche gelöscht werden.           |
|Schwerer löschen  <br/> |Des Elements oder Ordners wird dauerhaft gelöscht.<br/><br/>Festplatte gelöschte Objekte befinden sich im Ordner bereinigt die Dumpster. Dies ist wie bei der recycling LKW Curbside Recycle Containers leert. Die Elemente können nicht zugegriffen werden, von einem e-Mail-Client wie Outlook oder Outlook Web App und, es sei denn, legen Sie für das Postfach gesperrt ist, die Elemente werden dauerhaft gelöscht nach einem bestimmten Zeitraum.<br/><br/>Weitere zur Aufbewahrung von Elementen im Artikel [wiederherstellbare Elemente Kontingente und Aufbewahrung von gelöschten Elementen konfigurieren](http://technet.microsoft.com/en-us/library/ee364752%28v=exchg.150%29.aspx).<br/><br/>**Hinweis**: Ordner sind nicht in den Ordner Benutzerkontenverwaltung platziert, wenn sie hart gelöscht werden. Festplatte gelöschte Ordner werden aus dem Postfach entfernt.  |
   
Die Verschiebung für den Ordner Gelöschte Objekte und die harte Löschoptionen sind transaktional, d. h., zu dem Zeitpunkt der Webdienstaufruf beendet wurde, das Element in den Ordner Gelöschte Objekte verschoben wurde oder die Dumpster.
  
Die folgende Abbildung zeigt, mit denen Sie die im Ordner-Ökosystem besser zu verstehen, die zum Speichern von gelöschter Elementen verwendet werden, dass die Hierarchie von Ordnern, die enthalten können Elemente gelöscht. Die Namen der Ordner sind in den Typ **DistinguishedFolderIdNameType** Schema oder der **WellKnownFolderName** -Aufzählung in die EWS Managed API angezeigt werden. 
  
**Abbildung 3. Hierarchie von Ordnern, die gelöschten Elemente enthalten**

![Eine Abbildung der Ordnerhierarchie der Ordner, die gelöschte Elemente in einem primären Postfach und in einem Archivpostfach enthalten können. Jeder Ordner in der Abbildung wird durch den jeweiligen Namen des definierten Ordners dargestellt.](media/Ex_FolderHierarchyDeletedItems.png)
  
**Tabelle 2: Ordner, die gelöschte Elemente enthalten**

|**Ordnername**|**Eingeführt in**|**Beschreibung**|
|:-----|:-----|:-----|
|deleteditems  <br/> |Exchange 2007  <br/> |Ordner Gelöschte Elemente "Standard". Elemente bleiben in diesem Ordner, bis sie vorläufig oder Festplatten-gelöschte sind oder ein Aufbewahrungszeitraum überschritten wurde. Und klicken Sie dann in einen Ordner in dem sie verschoben werden die Dumpster. Gelöschte Ordner befinden sich im Ordner "Gelöschte Elemente", und wenn diese vorläufig - oder Festplatten-gelöscht, werden sie dauerhaft aus dem Postfach entfernt und können nicht wiederhergestellt werden.  <br/> |
|recoverableitemsroot  <br/> |Exchange 2010  <br/> |Der Stamm des dem Dumpster, oder "wiederherstellbare Elemente". Dumpster Access wurde in EWS in Exchange 2010 implementiert. "Wiederherstellbare Elemente" ist der Anzeigename für diesen Ordner.  <br/> |
|recoverableitemsdeletions  <br/> |Exchange 2010  <br/> |Die Hauptseite Dumpster Ordner für ein Postfach. Vorläufig gelöschten Elemente und Elemente, die durch eine Aufbewahrungsrichtlinie aus dem Ordner Gelöschte Elemente verschoben werden in diesem Ordner platziert. "Löschen" ist der Anzeigename für diesen Ordner.  <br/> |
|recoverableitemsversions  <br/> |Exchange 2010  <br/> |Ältere Versionen eines Elements in dem gespeichert werden. Ältere Versionen eines Elements werden erstellt, wenn ein Element aktualisiert wird. Entwurf Elementversionen werden nicht in diesem Ordner gespeichert. Der Anzeigename dieses Ordners ist "Versionen".  <br/> |
|recoverableitemspurges  <br/> |Exchange 2010  <br/> |Wo werden die Elemente, die aus dem Ordner Löschvorgänge entfernt werden gespeichert. Alle Speichern von Festplatten gelöschten Elemente werden in diesem Ordner verschoben. Der Anzeigename für diesen Ordner lautet "Bereinigt".  <br/> |
|archiveddeletedtitems  <br/> |Exchange 2010  <br/> |Den standardmäßigen Ordner für gelöschte Objekte für ein Archivpostfach.  <br/> |
|archiverecoverablesitemsroot  <br/> |Exchange 2010  <br/> |Das Stammverzeichnis Dumpster Ordner für ein Archivpostfach. Archivierte Elemente, die sind vorläufig gelöschten werden in einem Unterordner in diesen Ordner verschoben.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Exchange 2010  <br/> |Die Hauptseite Dumpster Ordner für ein Archivpostfach. Archivierte Elemente verschoben und die Dumpster hier platziert werden.  <br/> |
|archiverecoverableitemsversions  <br/> |Exchange 2010  <br/> |In dem ältere Versionen von archivierten Elemente gespeichert werden.  <br/> |
|archiverecoverableitemspurges  <br/> |Exchange 2010  <br/> |In dem Elemente werden aus dem Archiv Löschvorgänge Festplatte gelöscht Ordner in dem Dumpster gespeichert werden. Alle Store Festplatte gelöscht archiviert Elemente sind in diesen Ordner verschoben.  <br/> |
   
## <a name="how-do-i-delete-items"></a>Wie lösche ich Elemente?
<a name="bk_howdoIdeleteitems"> </a>

Verwenden Sie eine der folgenden Optionen, um anzugeben, ob ein Element in den Ordner Gelöschte Objekte verschoben oder führen Sie eine vorläufig oder einer harte löschen:
  
- Den einfachen **DisposalType** -Typ, wenn Sie Exchange Zugriff auf EWS verwenden. 
    
- Die [DeleteMode-Enumeration](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx), wenn Sie die EWS Managed API verwenden.
    
Eine Anzahl von unterschiedlichen EWS-Vorgänge oder EWS Managed API-Methoden können Sie Elemente und Ordner von einem Postfach löschen.
  
**Tabelle 3: EWS-Vorgänge und EWS Managed API-Methoden zum Löschen von Elementen**

|**EWS-Vorgang**|**EWS Managed API-Methode**|**Eingeführt in**|**Funktionsweise**|
|:-----|:-----|:-----|:-----|
|[DeleteFolder-Vorgang](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |[Folder.Delete-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Ordner aus einem Postfach gelöscht. Mit Exchange-Webdienste können Sie batch-Ordner löschen. Mit der EWS Managed API können Sie nur einen einzelnen Ordner pro Aufruf löschen.  <br/> |
|[DeleteItem-Operation](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Item.Delete-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)<br/><br/>[ExchangeService.DeleteItems-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.exchangeservice.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Löscht Elemente aus einem Postfach.  <br/> |
|[EmptyFolder-Vorgang](http://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <br/> |[Folder.Empty-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.folder.empty%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Löscht alle Elemente in einem Ordner, und löscht optional alle Unterordner in einem Ordner.  <br/> |
|[ApplyConversationAction-Vorgang](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |[Conversation.EnableAlwaysDeleteItems-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx)<br/><br/>[Conversation.DeleteItems-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.conversation.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Legt eine Delete processing-Aktion für e-Mail-Nachrichten in einer Unterhaltung, damit sie gelöscht werden.  <br/> |
|[DeleteUserConfiguration-Vorgang](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete-Methode](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Löscht einen Ordner, Element verknüpft ist und verschiebt es um die Dumpster.  <br/> |
|[CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |[Appointment.Accept-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.accept%28v=exchg.80%29.aspx) <br/><br/>[Appointment.AcceptTentatively-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[Appointment.CancelMeeting-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)<br/><br/>[Appointment.Decline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.decline%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Accept-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.accept%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.AcceptTentatively-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Decline-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest.decline%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Indirekt verschiebt ein Element in den Ordner Gelöschte Objekte, wenn eine Antwort auf eine Besprechungsanfrage gesendet wird oder die Antwort für den Termin festgelegt ist.<br/><br/>Der Typ der Löschvorgang ist nicht für diesen Vorgang festgelegt. Die Besprechungsnachrichten werden in den Ordner Gelöschte Objekte verschoben, wenn ein Antwortobjekt vom Dienst erfolgreich verarbeitet wird.  <br/> |
   
Sie können auch Elemente in den Ordner Gelöschte Objekte mithilfe von Regeln für den Posteingang verschieben. Beispielsweise können Sie [Regeln erstellen](inbox-management-and-ews-in-exchange.md) , die eine Delete-Aktion. 
  
Einige Punkte, über das Löschen von Elementen zu beachten:
  
- Löschen einer Vorkommen eines sich wiederholenden Elements eine Verschiebung in den Ordner Gelöschte Objekte nicht ausgelöst oder die Dumpster. Dies führt eine Aktualisierung auf das Master-Shape wiederkehrenden Element von sich wiederholenden Reihe.
    
- Standardordner kann nicht aus dem Postfach gelöscht werden.
    
- Löschen von Besprechungen oder Besprechungsnachrichten wie Besprechungsanfragen und oder meeting Updates zu vermeiden. Stattdessen diese Elemente mithilfe von Antwortobjekte beantworten. Auf diese Weise werden die zugehörigen Kalenderelemente der des Responders oder des Organisators Aktionen entsprechend aktualisiert.
    
- Key für ein Element ändern, werden nicht aktualisiert, wenn das Element in den Ordner Gelöschte Objekte oder Löschvorgänge verschoben wird.
    
- Wenn Sie Ausführen einer harte für ein Element löschen, und rufen Sie dann eine [SyncFolderHierarchy Vorgang](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) oder [SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) EWS Managed API-Methode oder eine [SyncFolderItems Vorgang](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) oder [SyncFolderItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) -Methode, eine Änderung **Löschen** Eintrag wird zurückgegeben. Wenn Sie ein Element in den Ordner Gelöschte Objekte verschieben, wird ein **Update** ändern Eintrag zurückgegeben. Dies ist, da des Elements oder Ordners einen neuen Eigenschaftswert [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) verfügen. [Mehr über die Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md) synchronisieren Elemente gelöscht ist Teil des Szenarios. 
    
## <a name="find-out-more-about-deleting-items"></a>Hier erfahren Sie mehr über das Löschen von Elementen
<a name="findoutmore"> </a>

- [Ziehen Sie Benachrichtigungen für EWS Postfach löschen-bezogenen Ereignisse in Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Fehlerbehandlung Löschung-bezogene in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)    
- [Ordner "wiederherstellbare Elemente"](http://technet.microsoft.com/en-us/library/ee364755.aspx)    
- [Wiederherstellung einzelner Elemente in Exchange Server 2010](http://blogs.technet.com/b/exchange/archive/2009/09/25/3408389.aspx#_Single_Item_Recovery)    
- [Exchange 2013: Löschen einer Terminserie programmgesteuert von Exchange-Servern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-a-e1c7b89d)    
- [Exchange 2013: Löschen von Aufgaben in einem Konto auf Exchange-Servern programmgesteuert](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-tasks-13824637)    
- [Exchange 2013: Leeren Sie programmgesteuert Ordner auf Exchange-Servern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Empty-6487df37)    
- [Exchange 2013: Löschen Sie programmgesteuert Ordner von Exchange-Servern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-aa1a5823)    
- [Exchange 2013: Löschen von vielen Elementen programmgesteuert von Exchange-Servern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-many-064f8760)    
- [Exchange 2013: Löschen von Kontakten programmgesteuert aus Exchange-Servern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-3b8b0640)    
- [Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)    
- [Verwalten der permanenten Anwendungseinstellungen mithilfe von EWS in Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    

