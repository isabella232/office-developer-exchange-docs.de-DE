---
title: Löschen Sie Elemente mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c81e3160-e12b-47e0-b3d6-4be28537f301
description: Finden Sie heraus, wie Sie die verwaltete API EWS oder EWS in Exchange verwenden können, um Elemente entweder durch Verschieben in den Ordner „Gelöschte Elemente" oder in den Papierkorb zu löschen.
ms.openlocfilehash: a475ebc6677e5f5003cc790a2d4d2b83c513f309
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756846"
---
# <a name="deleting-items-by-using-ews-in-exchange"></a>Löschen Sie Elemente mithilfe von EWS in Exchange

Finden Sie heraus, wie Sie die verwaltete API EWS oder EWS in Exchange verwenden können, um Elemente entweder durch Verschieben in den Ordner „Gelöschte Elemente" oder in den Papierkorb zu löschen.
  
Haben Sie sich schon einmal gefragt, was der Unterschied zwischen dem Verschieben von Elementen in den Ordner "Gelöschte Elemente" und dem Verschieben von Dateien in den Papierkorb ist? Möglicherweise möchten Sie mehr über die verschiedenen Optionen des Umgangs mit gelöschten Elementen wissen und wie Sie diese Optionen anwenden können. Exchange-Webdienste (EWS) enthalten drei Optionen des Umgangs mit gelöschten Elementen. In diesem Artikel werden hoffentlich jegliche Unklarheiten über die Unterschiede zwischen diesen beiden Möglichkeiten geklärt.
  
## <a name="deleting-items---what-are-my-options"></a>Elemente löschen – Was sind meine Optionen?
<a name="bk_DeletingItemsOptions"> </a>

Bevor Sie das gesamte Spektrum zum Löschen von Elementen verstehen, müssen Sie den folgenden Unterschied würdigen:
  
- Der Ordner "Gelöschte Elemente" – Wenn Sie Elemente in einem Postfach löschen, ist dies der Ort, an den diese Elemente verschoben werden.
    
- Der Papierkorb (auch bekannt als "wiederherstellbare Elemente") – Wenn Sie Elemente in einem Postfach löschen, ist dies der Ort, an den diese Elemente verschoben werden.
    
Die Schaubilder 1 und 2 zeigen, wie der Löschvorgang für Elemente und Ordner in einem Postfach aussieht. 

**Abbildung 1. Verfahren zum Löschen von Elementen aus einem Postfach**

![Eine Abbildung, die zeigt, wohin Elemente verschoben werden, sobald sie gelöscht wurden. Gelöschte Elemente werden in den Ordner "Gelöschte Elemente" verschoben, und dann, je nach Aufbewahrungsrichtlinie, in den Ordner "Wiederherstellbare Elemente" verschoben, bis sie verfallen und endgültig gelöscht werden.](media/Ex_DeleteItems_Source.png)

<br/>

**Abbildung 2. Verfahren zum Löschen von Ordnern aus einem Postfach**

![Eine Abbildung, in der dargestellt wird, wie gelöschte Ordner in den Ordner "Gelöschte Elemente" verschoben werden und dann endgültig aus dem Postfach gelöscht werden.](media/Ex_.png)
   
Sie können Elemente und Ordner auf drei verschiedene Arten löschen, je nachdem, wie lange das Element bis zur endgültigen Löschung aufbewahrt werden soll.
  
**Tabelle 1: Optionen für das Löschen von Elementen durch Verwendung von EWS**

|**Option**|**Aktionen**|
|:-----|:-----|
|In den Ordner "Gelöschte Elemente" verschieben  <br/> |Dies ist die kürzestmögliche Dauer zur Entfernung von Elementen.<br/><br/>Sie können dies damit vergleichen, ein Blatt Papier in den Papierkorb bei Ihrem Schreibtisch zu werfen. Sie können es ganz einfach wieder an sich nehmen, sobald Sie es wieder benötigen.<br/><br/>Sie können jeglichen [Löschvorgang](deleting-items-by-using-ews-in-exchange.md#bk_howdoIdeleteitems) ausführen, der das Element in den Ordner „Gelöschte Elemente“ verschiebt, um diese Aktion auszuführen.<br/><br/>Sie können genauso den [Vorgang „Element verschieben“](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) ( [Item.Move()](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx)) oder den [Vorgang „Ordner verschieben“](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) ( [Folder.Move()](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx)) nutzen, um ein Element oder Ordner in den Ordner „Gelöschte Elemente" zu verschieben.  <br/> |
|Vorläufig löschen  <br/> |Das Element wird in den Ordner „Entfernen" im Papierkorb verschoben. <br/><br/>Dies können Sie damit vergleichen, wenn Sie Ihren Papierkorb in Ihrem Müllcontainer am Straßenrand ausleeren. Sie können auf das Element bei Bedarf weiterhin zugreifen, nun ist es nur ein wenig schwieriger.  <br/><br/>Wenn Sie mehr über den Papierkorb (auch „wiederherstellbare Elemente" genannt) und über Fallbeispiele wie eDiscovery oder Rechtsstreitigkeiten erfahren möchten, finden Sie alle Informationen unter dem [Ordner „wiederherstellbare Elemente"](http://technet.microsoft.com/de-DE/library/ee364755%28v=exchg.150%29.aspx) auf TechNet.<br/><br/>Vorläufige Löschvorgänge sind nicht für Apps geeignet, die auf Exchange 2007 abzielen. In Exchange 2007 werden vorläufige Löschvorgänge so behandelt, dass ein Bit auf das Element gesetzt wird, um herauszustellen, dass es zu einem unbestimmten Zeitpunkt in den Papierkorb verschoben wird.<br/><br/>Vorläufig gelöschte Traversalen, oder die Suchaktionen nach  Elementen, die vorläufig über die[„Element finden“ Aktion gelöscht wurden, werden weder von Exchange Online, Exchange Online als Teil von Office 365, noch anderen Versionen von Exchange, beginnend bei Exchange 2010, unterstützt.  <br/><br/>**Hinweis**: Die Ordner können nicht vorläufig gelöscht werden.           |
|Dauerhaft löschen  <br/> |Das Element wird dauerhaft gelöscht.<br/><br/>Dauerhaft gelöschte Elemente befinden sich im Ordner „Bereinigt" des Papierkorbs. Dies ist vergleichbar mit der Müllabfuhr, die den Mülleimer am Straßenrand entleert. Der Zugriff auf die Elemente erfolgt weder über einen E-Mail-Klienten wie Outlook oder die Outlook Web App, außer es wurde ein bestimmter Bereich für das Postfach festgelegt, der gewisse Elemente einbehält. Ansonsten werden die Elemente nach Ablauf eines festgelegten Zeitraumes endgültig gelöscht.<br/><br/>Sie können weitere Informationen zur Aufbewahrungszeit im Artikel [Einstellungen zur Aufbewahrungszeit von gelöschten Elementen und Anteil an wiederherstellbaren Elementen](http://technet.microsoft.com/de-DE/library/ee364752%28v=exchg.150%29.aspx) finden.<br/><br/>**Hinweis**: Die Ordner werden nicht in den Ordner „Bereinigt" verschoben, sobald sie gelöscht wurden. Endgültig gelöschte Ordner werden aus dem Postfach entfernt.  |
   
Das Verschieben in den Ordner „Gelöschte Elemente" und die Möglichkeiten, Elemente endgültig zu löschen, sind transaktional. Dies bedeutet, dass, sobald alle Web Service-Aufrufe abgeschlossen sind, das Element in den Ordner „Gelöschte Elemente" oder in den Papierkorb  verschoben wurde.
  
Damit Sie die Funktionsweise der Ordner, die gelöschte Elementen aufbewahren, besser verstehen, zeigt die folgende Abbildung die Hierarchie der Ordner, die gelöschte Elemente enthalten können. Die Namen der Ordner, so wie sie im Schema-Typ **DistinguishedFolderIdNameType** oder unter der Aufzählung **WellKnownFolderName** in der EWS API auftauchen. 
  
**Abbildung 3. Hierarchie der Ordner, in denen gelöschte Elemente gespeichert werden**

![Eine Abbildung der Ordnerhierarchie der Ordner, die gelöschte Elemente in einem primären Postfach und in einem Archivpostfach enthalten können. Jeder Ordner in der Abbildung wird durch den jeweiligen Namen des definierten Ordners dargestellt.](media/Ex_FolderHierarchyDeletedItems.png)
  
**Abbildung 2: Ordner, die gelöschte Elemente enthalten**

|**Ordnername**|**Eingeführt in**|**Beschreibung**|
|:-----|:-----|:-----|
|gelöschte Elemente  <br/> |Exchange 2007  <br/> |Dies ist die Voreinstellung des Ordners „Gelöschte Elemente". Elemente verbleiben in diesem Ordner, bis sie vorläufig oder endgültig gelöscht werden oder ein Aufbewahrungszeitraum abgelaufen ist. Dann werden sie in einen Ordner im Papierkorn verschoben. Gelöschte Ordner werden in den Ordner „Gelöschte Elemente" verschoben, and sobald sie vorübergehend oder endgültig gelöscht sind, werden sie dauerhaft aus dem Postfach entfernt und es ist nicht mehr möglich, sie wiederherzustellen.  <br/> |
|recoverableitemsroot  <br/> |Exchange 2010  <br/> |Dies ist der Ursprung des Papierkorbes, oder der Ordner „Wiederherstellbare Elemente“. Zugriff auf den Papierkorb wurde in EWS in Exchange 2010 eingeführt. Der Anzeigename dieses Ordners lautet „Wiederherstellbare Elemente".  <br/> |
|recoverableitemsdeletions  <br/> |Exchange 2010  <br/> |Der primäre Papierkorb Ordner des Postfachs. Vorübergehend gelöschte Elemente und Elemente, die durch eine Aufbewahrungsrichtlinie aus dem Ordner „Gelöschte Elemente" verschoben wurden, werden in diesem Ordner gespeichert. Der Anzeigename dieses Ordners lautet „Gelöschte Elemente“.  <br/> |
|recoverableitemsversions  <br/> |Exchange 2010  <br/> |Hier werden ältere Versionen eines Elements gespeichert. Alte Versionen eines Elements werden erstellt, wenn ein Element aktualisiert wird. Element-Entwürfe werden nicht unter diesem Ordner gespeichert. Der Anzeigename dieses Ordners lautet „Entwürfe“.  <br/> |
|recoverableitemspurges  <br/> |Exchange 2010  <br/> |Hier befinden sich Elemente, die aus dem Ordner „Gelöschte Elemente“ entfernt wurden. Alle gelagerten, endgültig gelöschten Elemente werden in diesen Ordner verschoben. Der Anzeigename dieses Ordners lautet „Bereinigt“.  <br/> |
|archiveddeletedtitems  <br/> |Exchange 2010  <br/> |Dies ist die Voreinstellung des Ordners „Gelöschte Elemente“ für ein Archivpostfach.  <br/> |
|archiverecoverablesitemsroot  <br/> |Exchange 2010  <br/> |Der ursprüngliche Papierkorb für ein Archivpostfach. Archivierte Elemente, die vorübergehend gelöscht wurden, werden in einen Unterordner in diesem Ordner verschoben.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Exchange 2010  <br/> |Dies ist der primäre Papierkorb für ein Archivpostfach. Archivierte Elemente, die in den Papierkorb verschoben wurden, befinden sich hier.  <br/> |
|archiverecoverableitemsversions  <br/> |Exchange 2010  <br/> |Hier werden ältere Versionen von archivierten Elementen gespeichert.  <br/> |
|archiverecoverableitemspurges  <br/> |Exchange 2010  <br/> |Hier werden endgültig gelöschte Elemente gespeichert, die aus dem Archiv-Ordner „Gelöschte Elemente“ in den Papierkorb verschoben wurden. Alle gelagerten, endgültig gelöschten, archivierten Elemente werden in diesen Ordner verschoben.  <br/> |
   
## <a name="how-do-i-delete-items"></a>Wie lösche ich Elemente?
<a name="bk_howdoIdeleteitems"> </a>

Verwenden Sie eine der folgenden Optionen, um anzugeben, ob ein Element in den Ordner "Gelöschte Elemente" verschieben oder führen Sie eine vorläufig löschen oder ein endgültiges Löschen:
  
- Dies ist das einfache Modell **DisposalType** der bei Nutzung von EWS angewendet wird, um Exchange aufzurufen. 
    
- Dies ist die [DeleteMode Aufzählung](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx), die auftaucht, sobald Sie die von EWS verwaltete API verwenden. 
    
Sie können viele verschiedene EWS Funktionen oder von EWS verwaltete API Methoden verwenden, um Elemente und Ordner aus einem Postfach zu löschen.
  
**Tabelle 3: EWS Funktionen und von EWS verwaltete API-Methoden zum Löschen von Elementen **

|**EWS-Vorgang**|**Von EWS verwaltete API-Methode**|**Eingeführt in**|**Funktion der Einstellung**|
|:-----|:-----|:-----|:-----|
|[DeleteFolder-Vorgang](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |[Folder.Delete-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Diese Funktion löscht Ordner aus einem Postfach. Mit EWS können Sie direkt mehrere Ordner löschen. Mit der von EWS verwalteten API können Sie nur einen Ordner pro Klick löschen.  <br/> |
|[DeleteItem-Vorgang](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Item.Delete-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)<br/><br/>[ExchangeService.DeleteItems-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.exchangeservice.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Diese Funktion löscht Elemente aus einem Postfach.  <br/> |
|[EmptyFolder-Vorgang](http://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <br/> |[Folder.Empty-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.folder.empty%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Diese Funktion löscht alle Elemente in einem Ordner sowie, wenn gewünscht, auch alle Unterordner in einem Ordner.  <br/> |
|[ApplyConversationAction-Vorgang](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |[Conversation.EnableAlwaysDeleteItems-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx)<br/><br/>[Conversation.DeleteItems-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.conversation.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Diese Funktion legt das Löschen von E-Mail-Nachrichten in einer Unterhaltung fest, damit diese direkt entfernt werden.  <br/> |
|[DeleteUserConfiguration-Vorgang](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete-Methode](http://msdn.microsoft.com/de-DE/library/exchange/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Diese Funktion löscht ein Element, das mit einem Ordner verknüpft ist, und verschiebt es in den Papierkorb.  <br/> |
|[CreateItem-Vorgang](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |[Appointment.Accept-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.accept%28v=exchg.80%29.aspx) <br/><br/>[Appointment.AcceptTentatively-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[Appointment.CancelMeeting-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)<br/><br/>[Appointment.Decline](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment.decline%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Accept-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingrequest.accept%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.AcceptTentatively-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingrequest.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[MeetingRequest.Decline-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingrequest.decline%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Hiermit wird das Element indirekt in den Ordner „gelöschte Elemente" verschoben, sobald eine Antwort auf eine Besprechungsanfrage gesendet wird oder sobald die Antwort einen bestimmten Termin festgelegt.<br/><br/>Der Typ Löschvorgang ist für diesen Vorgang nicht festgelegt. Die Besprechungsnachrichten werden in den Ordner „gelöschte Elemente" verschoben, sobald eine Antwort erfolgreich verarbeitet wurde.  <br/> |
   
Sie können Elemente auch mithilfe von Posteingangsregeln in den Ordner „gelöschte Elemente" verschieben. Sie können beispielsweise [Regeln erstellen](inbox-management-and-ews-in-exchange.md), mit der Sie eine Aktion löschen. 
  
Einige Dinge müssen Sie bei der Entfernung von Elementen beachten:
  
- Wenn Sie eine Terminserie löschen, verschieben Sie das Element hiermit weder in den Ordner „Gelöschte Elemente" noch in den Papierkorb. Dies führt stattdessen zu einem Update des Haupt-Elements der Terminserie.
    
- Sie können keine Standard Ordner aus dem Postfach löschen. 
    
- Vermeiden Sie das Löschen von Besprechungen oder Besprechungsnachrichten, wie Besprechungsanfragen und oder Besprechungs-Updates. Antworten Sie stattdessen auf diese Elemente mit Antwort-Objekten. Auf diese Weise werden die zugehörigen Kalender-Elemente aktualisiert, um das Verhalten der Antwortenden oder des Veranstalters wiederzugeben.
    
- Sie updaten oder ändern den Key des Elements nicht, sobald das Element in den Ordner „Gelöschte Elemente“ oder „Löschvorgänge“ verschoben wird.
    
- Wenn Sie ein Element endgültig löschen, und dann einen[SyncFolderHierarchy Vorgang](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) oder eine [SyncFolderHierarchy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) von EWS verwaltete API-Methode oder einen [SyncFolderItems Vorgang](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)oder eine [SyncFolderItems](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) Methode anwenden wird ein Änderungs-Eintrag zum **Löschen** angewandt. Wenn Sie ein Element in den Ordner „Gelöschte Elemente" verschieben, wird ein **Update** Änderungs-Eintrag angewandt. Dies passiert, da das Element oder der Ordner einen neuen [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) Eigenschaftswert bekommt. [Lesen Sie mehr über die Synchronisierung](mailbox-synchronization-and-ews-in-exchange.md), falls das Synchronisieren von gelöschten Elementen zu Ihren Tätigkeiten gehört. 
    
## <a name="find-out-more-about-deleting-items"></a>Hier finden Sie weitere Informationen zum Löschen von Elementen
<a name="findoutmore"> </a>

- [Abrufbenachrichtigungen für EWS löschbezogene Postfachereignisse in Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Umgang mit Fehlern, die durch Löschen hervorgerunfen wurden in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)    
- [Ordner „Wiederherstellbare Elemente"](http://technet.microsoft.com/de-DE/library/ee364755.aspx)    
- [Die Wiederherstellung einzelner Elemente in Exchange Server 2010](http://blogs.technet.com/b/exchange/archive/2009/09/25/3408389.aspx#_Single_Item_Recovery)    
- [Exchange 2013: Das Löschen einer Terminserie wird von Exchange-Servern programmgesteuert](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-a-e1c7b89d)    
- [Exchange 2013: Das Löschen von Aufgaben aus einem Konto auf Exchange-Servern ist programmgesteuert](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-tasks-13824637)    
- [Exchange 2013: Die Leerung von Ordnern auf Exchange-Servern ist programmgesteuert](http://code.msdn.microsoft.com/exchange/Exchange-2013-Empty-6487df37)    
- [Exchange 2013: Das Löschen von Ordner wird von Exchange-Servern programmgesteuert](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-aa1a5823)    
- [Exchange 2013: Löschen Sie mehrere Elemente programmgesteuert über Exchange-Server ](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-many-064f8760)    
- [Exchange 2013: Löschen Sie Kontakte programmgesteuert über Exchange-Server](http://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-3b8b0640)    
- [Löschen Sie Termine und sagen Sie Besprechungen mit EWS in Exchange ab](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)    
- [Verwalten Sie wiederkehrenden App Einstellungen über die Nutzung von EWS in Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    

