---
title: Verteilergruppen und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: Informationen Sie zu den verschiedenen Typen von Verteilergruppen, die in Exchange verfügbar sind und wie Sie sie in die EWS Managed API oder EWS-Anwendung verwalten können.
ms.openlocfilehash: 9b54bfd75f7d68f08c767171d99251b5ce86b7c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756835"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>Verteilergruppen und EWS in Exchange

Informationen Sie zu den verschiedenen Typen von Verteilergruppen, die in Exchange verfügbar sind und wie Sie sie in die EWS Managed API oder EWS-Anwendung verwalten können.
  
Eine Verteilergruppe ist eine Auflistung von e-Mail-Adressen, die eine einzelne Alias oder die e-Mail-Adresse zugeordnet sind. Verteilergruppen (manchmal auch als Verteilerlisten bezeichnet) Aktivieren eines Benutzers senden von e-Mails an mehrere Personen mithilfe einer einzelnen Adresse des Empfängers. Da Gruppenmitgliedschaft Verteilung und daher die Empfänger der Nachricht außerhalb der einzelnen e-Mail-Threads verwaltet werden können, bieten Verteilergruppen eine hervorragende Möglichkeit, die Verteilung von e-Mail-Nachrichten an eine Gruppe von Benutzern zu ermöglichen. Sie können programmgesteuert erstellen und Verwalten von Verteilergruppen mithilfe der EWS Managed API, EWS und der Exchange-Verwaltungsshell. Bevor Sie Programmierung beginnen, betrachten wir die verschiedenen Typen von Verteilergruppen, die verfügbar sind und Ihre Optionen verwaltet werden können.
  
## <a name="types-of-distribution-groups"></a>Typen von Verteilergruppen

Exchange unterstützt drei Typen von Verteilergruppen:
  
- [Universelle Verteilergruppen](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) – Active Directory universelle Verteilergruppenobjekte, die e-Mail-aktiviert sind. Universelle Verteilergruppen dienen zum Verteilen von Nachrichten an eine Gruppe von Empfängern. 
    
- [Sicherheitsgruppen](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) – Active Directory-Objekte, die e-Mail-aktivierte; sind auch bekannt als universellen Sicherheitsgruppen. Sicherheitsgruppen werden Zuweisung von Zugriffsberechtigungen auf Ressourcen in Active Directory-Domänendienste (AD DS) sowie zum Verteilen von Nachrichten verwendet. 
    
- [Bildschirm "Kontaktgruppen"](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) – Private Verteilergruppen, die im Postfach des Benutzers gespeichert sind. 
    
Der Typ der Verteilergruppe, die Sie auswählen, hängt, in dem Sie zum Speichern der Verteilergruppe, die sie verwenden möchten, Planen und was er für verwendet werden soll.
  
### <a name="universal-distribution-groups"></a>Universelle Verteilergruppen
<a name="bk_DistributionGroup"> </a>

Universelle Verteilergruppen können Gruppen von Empfängern in einer einzelnen Alias oder die e-Mail-Adresse konsolidieren. Da universelle Verteilergruppen in AD DS gespeichert werden, können damit alle Benutzer zum Senden von e-Mails, einschließlich der Benutzer außerhalb Ihrer Organisation. Sie können die EWS Managed API oder EWS verwenden, um eine Verteilergruppe zu erweitern, aber zum Erstellen und Verwalten von Verteilergruppen, müssen Sie die [Exchange-Verwaltungsshell-Cmdlets](#bk_UsingEMS)verwenden.
  
Universelle Verteilergruppen können auch eine Auflistung von Räumen enthalten. Geben Sie beispielsweise Folgendes ein, um Benutzern die Suche nach einem Konferenzraum für eine Besprechung zu erleichtern. Benutzer können eine Raumliste hinzufügen – eine universelle Verteilergruppe, die Ressource raumpostfächer enthält – auf eine Besprechungsanfrage verfügbaren Raum suchen, ohne dass jedem Raum einzeln hinzugefügt.
  
Sie können eine statische universelle Verteilergruppe, die die gleichen, bis Sie zum Aktualisieren der Mitgliedschaft bleibt erstellen, oder Sie können eine dynamische universelle Verteilergruppe erstellen. Eine dynamische universelle Verteilergruppe fragt Active Directory e-Mail-aktivierte Objekte und Mitglied der Gruppe basierend auf den Ergebnissen erstellt. Mitgliedschaft in der Gruppe wird neu berechnet, wenn eine e-Mail-Nachricht an die Gruppe gesendet wird. 
  
### <a name="security-groups"></a>Sicherheitsgruppen
<a name="bk_SecurityGroup"> </a>

Universelle Verteilergruppen und Sicherheitsgruppen sind in den meisten Arten identisch. Im Gegensatz zu universelle Verteilergruppen können Sie Sicherheitsgruppen jedoch Netzwerkressourcen in AD DS Berechtigungen zuweisen. Sie können die EWS Managed API oder EWS zum Erstellen und Verwalten von Sicherheitsgruppen verwenden. Verwenden Sie stattdessen die [Exchange-Verwaltungsshell-Cmdlets](#bk_UsingEMS). Aber genau wie universelle Verteilergruppen, können Sie die EWS Managed API oder EWS verwenden, um Sicherheitsgruppen zu erweitern.
  
### <a name="contact-groups"></a>Kontaktgruppen
<a name="bk_ContactGroup"> </a>

Wenn nicht alle Benutzer administrative Zugriff auf dem Server für das Erstellen von Verteilergruppen ermöglichen möchten, aber sie eine Nachricht an eine große Sammlung von Personen senden können sollen, können Sie diese Schritte mithilfe von Kontaktgruppen durchführen. Eine Gruppe von Kontakte keine e-Mail-Adresse zugeordnet, und befindet sich nur im Postfach eines Benutzers; andere Benutzer wird nicht darauf zugreifen können. [Verwenden Sie die EWS Managed API oder EWS Kontaktgruppen erstellen](how-to-create-contact-groups-by-using-ews-in-exchange.md)können.
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>Verwalten von Verteilergruppen mithilfe des EWS Managed API oder EWS

Sie können die EWS Managed API oder EWS um eine universelle Verteilergruppe oder Sicherheitsgruppe erweitern und die Erstellung und Verwaltung einer Kontaktgruppe steuern verwenden. jedoch können Sie diese Technologien zum Erstellen oder Bearbeiten der Mitglieder dieser Gruppen verwenden. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Verwaltung von Verteilergruppen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|**Verwenden Sie zum...**|
|:-----|:-----|:-----|
|Methoden der [ContactGroup-Klasse](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)  <br/> |[CreatItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Erstellen Sie eine Gruppe von Kontakte im Exchange-Speicher.  <br/> > [!NOTE]> Sie können keine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe von EWS Managed API oder EWS erstellen.           |
|[ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[Der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Erweitern Sie eine universelle Verteilergruppe, eine Sicherheitsgruppe oder eine Gruppe von Kontakten durch Abrufen einer Liste der aktivierbaren Elemente aus.  <br/> |
|[FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Suchen Sie nach einer Kontaktgruppen im Postfach.  <br/> |
|[GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Eine Auflistung von allen Chatrooms in einer angegebenen Raumliste in einer Organisation abzurufen. Eine Raumliste ist eine Verteilergruppe, die nur raumpostfächer Ressource enthält.  <br/> |
|[ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Suchen nach und mögliche Kandidaten entsprechend einen mehrdeutigen Name zurückgegeben. Die Kandidaten können Verteilergruppen sein.  <br/> |
   
Durch die [ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) -Methode oder der Vorgang [der ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) zurückgegebene Informationen können Sie bestimmen, welche Typen der Elemente in der Gruppe sind. Die Membertypen werden durch die [MailboxType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) EWS Managed API-Aufzählung und das [MailboxType](http://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) EWS-Element definiert. 
  
**In Tabelle 2. Verteilung Gruppe Membertypen**

|**MailboxType-Enumerationswert ab**|**MailboxType-Elementwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Postfach  <br/> |Postfach  <br/> |Ein e-Mail-aktivierte Active Directory-Objekt.  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |Eine Verteilergruppe, die innerhalb der Gruppe, die Sie soeben erweitert enthalten sind. Wenn Sie eine vollständige Liste der Elemente erhalten möchten, erweitern Sie diese Gruppe ebenfalls.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |Eine Gruppe von Kontakten, die im Postfach befindet und ist nur verfügbar für Benutzer von dem Postfach.  <br/> |
|Kontakt  <br/> |Kontakt  <br/> |Ein Exchange-Datenbank Kontakt oder die e-Mail-Kontakt Active Directory.  <br/> |
   
## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>Verwalten von Verteilergruppen mithilfe der Exchange-Verwaltungsshell
<a name="bk_UsingEMS"> </a>

Sie können die [Exchange-Verwaltungsshell-Cmdlets verwenden](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx) , um universelle Verteilergruppen und Sicherheitsgruppen in Ihrem Code erstellen und verwalten. 
  
> [!NOTE]
> Sie können Exchange-Verwaltungsshell-Cmdlets zum Verwalten von Kontaktgruppen verwenden. 
  
**Tabelle 3. Exchange-Verwaltungsshell-Cmdlets für die Arbeit mit Verteilergruppen**

|**Cmdlet**|**Verwenden Sie zum...**|
|:-----|:-----|
|[Disable-DistributionGroup](http://technet.microsoft.com/en-us/library/aa997942%28v=exchg.150%29.aspx) <br/> |E-Mail-Funktionen aus einer e-Mail-aktivierten Verteilergruppe zu entfernen.  <br/> |
|[Enable-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998916%28v=exchg.150%29.aspx) <br/> |Eine vorhandene universelle Gruppe e-Mail-aktivieren.  <br/> |
|[Get-DistributionGroup](http://technet.microsoft.com/en-us/library/bb124755%28v=exchg.150%29.aspx) <br/> |Abfrage nach vorhandenen Verteilergruppen.  <br/> |
|[New-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx) <br/> |Erstellen einer Verteilergruppe an.  <br/> |
|[Remove-DistributionGroup](http://technet.microsoft.com/en-us/library/aa997627%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen Verteilergruppe von AD DS.  <br/> |
|[Set-DistributionGroup](http://technet.microsoft.com/en-us/library/bb124955%28v=exchg.150%29.aspx) <br/> |Ändern der Einstellungen einer vorhandenen Verteilergruppe an.  <br/> |
|[Add-DistributionGroupMember](http://technet.microsoft.com/en-us/library/bb124340%28v=exchg.150%29.aspx) <br/> |Empfänger an eine Verteilergruppe hinzufügen.  <br/> |
|[Get-DistributionGroupMember](http://technet.microsoft.com/en-us/library/aa996367%28v=exchg.150%29.aspx) <br/> |Hier finden Sie vorhandene Verteilergruppe Mitglieder der Gruppe.  <br/> |
|[Remove-DistributionGroupMember](http://technet.microsoft.com/en-us/library/aa998016%28v=exchg.150%29.aspx) <br/> |Entfernen Sie einen vorhandenen Empfänger aus einer Verteilergruppe ein.  <br/> |
|[Update-DistributionGroupMember](http://technet.microsoft.com/en-us/library/dd335049%28v=exchg.150%29.aspx) <br/> |Aktualisieren Sie ein Mitglied einer angegebenen Verteilergruppe.  <br/> |
|[Get-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb124762%28v=exchg.150%29.aspx) <br/> |Abrufen der Einstellungen auf einer vorhandenen dynamischen Verteilergruppe an.  <br/> |
|[Neue DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125127%28v=exchg.150%29.aspx) <br/> |Erstellen Sie eine dynamische Verteilergruppe an.  <br/> |
|[Remove-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125038%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen dynamischen Verteilergruppe an. Dieses Cmdlet entfernt die dynamische Verteilergruppe aus AD DS.  <br/> |
|[Set-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb123796%28v=exchg.150%29.aspx) <br/> |Ändern der Einstellungen einer vorhandenen dynamischen Verteilergruppe an.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_UsingEMS"> </a>

- [Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    
- [Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Aufrufen von Exchange-Verwaltungsshell-Cmdlets aus verwaltetem Code](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)
    

