---
title: Verteilergruppen und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: Erfahren Sie mehr über die verschiedenen Arten von Verteilergruppen, die in Exchange verfügbar sind, und wie Sie diese in ihrer verwaltete EWS-API-oder EWS-Anwendung verwalten können.
ms.openlocfilehash: 083a2c7380e8b9677ddacc9ae3c9465d6a9db97f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528433"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>Verteilergruppen und EWS in Exchange

Erfahren Sie mehr über die verschiedenen Arten von Verteilergruppen, die in Exchange verfügbar sind, und wie Sie diese in ihrer verwaltete EWS-API-oder EWS-Anwendung verwalten können.
  
Eine Verteilergruppe ist eine Sammlung von E-Mail-Adressen, die mit einem einzelnen Alias oder E-Mail-Adresse verknüpft sind. Verteilergruppen (auch manchmal als Verteilerlisten bezeichnet) ermöglichen einem Benutzer das Senden von e-Mails an mehrere Personen mithilfe einer einzelnen Empfängeradresse. Da Verteilergruppenmitgliedschaften und somit die Nachrichtenempfänger außerhalb einzelner e-Mail-Threads verwaltet werden können, bieten Verteilergruppen eine hervorragende Möglichkeit, die Verteilung von e-Mails an eine Gruppe von Benutzern zu ermöglichen. Sie können programmgesteuert Verteilergruppen mithilfe der verwaltete EWS-API, EWS und der Exchange-Verwaltungsshell erstellen und verwalten. Bevor Sie mit der Programmierung beginnen, erforschen wir die verschiedenen Arten von Verteilergruppen, die verfügbar sind, und Ihre Optionen für deren Verwaltung.
  
## <a name="types-of-distribution-groups"></a>Arten von Verteilergruppen

Exchange unterstützt drei Arten von Verteilergruppen:
  
- [Universelle Verteilergruppen](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) : Active Directory universelle Verteilergruppenobjekte, die e-Mail-aktiviert sind. Universelle Verteilergruppen werden verwendet, um Nachrichten an eine Gruppe von Empfängern zu verteilen. 
    
- [Sicherheitsgruppen](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) – Active Directory Objekte, die e-Mail-aktiviert sind; wird auch als universelle Sicherheitsgruppen bezeichnet. Sicherheitsgruppen werden zum Zuweisen von Zugriffsberechtigungen zu Ressourcen in Active Directory-Domänendienste (AD DS) sowie zum Verteilen von Nachrichten verwendet. 
    
- [Kontaktgruppen](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) – private Verteilergruppen, die sich im Postfach eines Benutzers befinden. 
    
Der Typ der Verteilergruppe, die Sie auswählen, hängt davon ab, wo Sie die Verteilergruppe speichern möchten, wer Sie verwenden wird und wofür Sie verwendet wird.

<a name="bk_DistributionGroup"> </a>

### <a name="universal-distribution-groups"></a>Universelle Verteilergruppen

Sie können universelle Verteilergruppen verwenden, um Gruppen von Empfängern in einem einzelnen Alias oder einer einzigen e-Mail-Adresse zu konsolidieren. Da universelle Verteilergruppen in AD DS gespeichert werden, können Sie von jedem Benutzer zum Senden von e-Mails verwendet werden, einschließlich Benutzern außerhalb Ihrer Organisation. Sie können die verwaltete EWS-API oder EWS zum Erweitern einer Verteilergruppe verwenden, aber zum Erstellen und Verwalten von Verteilergruppen müssen Sie [Exchange-Verwaltungsshell-Cmdlets](#bk_UsingEMS)verwenden.
  
Sie können auch universelle Verteilergruppen verwenden, um eine Sammlung von Räumen zu enthalten; Damit können Benutzer beispielsweise einen Konferenzraum für eine Besprechung leichter finden. Benutzer können eine Raumliste – eine universelle Verteilergruppe, die Raum Ressourcenpostfächer enthält – einer Besprechungsanfrage hinzufügen, um einen verfügbaren Raum zu finden, ohne jeden Raum einzeln hinzufügen zu müssen.
  
Sie können eine statische universelle Verteilergruppe erstellen, die so lange bleibt, bis Sie die Mitgliedschaft aktualisieren, oder Sie können eine dynamische universelle Verteilergruppe erstellen. Eine dynamische universelle Verteilergruppe fragt Active Directory e-Mail-aktivierten Objekte ab und erstellt die Gruppenmitgliedschaft basierend auf den Ergebnissen. Die Gruppenmitgliedschaft wird jeweils neu berechnet, wenn eine E-Mail-Nachricht an die Gruppe gesendet wird. 

<a name="bk_SecurityGroup"> </a>

### <a name="security-groups"></a>Sicherheitsgruppen

Universelle Verteilergruppen und Sicherheitsgruppen sind auf die meisten Arten identisch. Im Gegensatz zu universellen Verteilergruppen können Sie Sicherheitsgruppen verwenden, um Netzwerkressourcen in AD DS Berechtigungen zuzuweisen. Das verwaltete EWS-API oder EWS kann nicht zum Erstellen und Verwalten von Sicherheitsgruppen verwendet werden. Stattdessen verwenden Sie [Exchange-Verwaltungsshell-Cmdlets](#bk_UsingEMS). Aber wie universelle Verteilergruppen können Sie die verwaltete EWS-API oder EWS verwenden, um Sicherheitsgruppen zu erweitern.

<a name="bk_ContactGroup"> </a>

### <a name="contact-groups"></a>Kontaktgruppen

Wenn Sie nicht jedem Benutzer Administratorzugriff auf den Server erteilen möchten, um Verteilergruppen zu erstellen, aber diese zum Senden einer einzelnen Nachricht an eine große Sammlung von Personen aktivieren möchten, können Sie dies mithilfe von Kontaktgruppen tun. Einer Kontaktgruppe ist keine e-Mail-Adresse zugeordnet, und Sie ist nur im Postfach eines Benutzers vorhanden. andere Benutzer haben keinen Zugriff darauf. Sie können [die verwaltete EWS-API oder EWS verwenden, um Kontaktgruppen zu erstellen](how-to-create-contact-groups-by-using-ews-in-exchange.md).
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>Verwalten von Verteilergruppen mithilfe der verwaltete EWS-API oder EWS

Sie können die verwaltete EWS-API oder EWS verwenden, um eine universelle Verteilergruppe oder Sicherheitsgruppe zu erweitern und die Erstellung und Verwaltung einer Kontaktgruppe zu steuern. Sie können diese Technologien jedoch nicht verwenden, um die Mitglieder dieser Gruppen zu erstellen oder zu bearbeiten. 
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Verwalten von Verteilergruppen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|**Verwenden für...**|
|:-----|:-----|:-----|
|[Contactgroup-Klassen](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) Methoden  <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Erstellen Sie eine Kontaktgruppe im Exchange-Informationsspeicher.<br/><br/>**Hinweis**: Sie können keine universelle Verteilergruppe oder Sicherheitsgruppe mithilfe von verwaltete EWS-API oder EWS erstellen.           |
|[ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Erweitern Sie eine universelle Verteilergruppe, Sicherheitsgruppe oder Kontaktgruppe, indem Sie eine Liste der Mitglieder abrufen.  <br/> |
|[FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Suchen Sie im Postfach nach Kontaktgruppen.  <br/> |
|[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Dient zum Abrufen einer Auflistung aller Räume in einer angegebenen Raumliste in einer Organisation. Eine Raumliste ist eine Verteilergruppe, die nur Raum Ressourcenpostfächer enthält.  <br/> |
|[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Suchen und zurückgeben möglicher Kandidaten, die mit einem eindeutigen Namen übereinstimmen. Die Kandidaten können Verteilergruppen sein.  <br/> |
   
Sie können die von der [expando](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) -Methode oder dem [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) -Vorgang zurückgegebenen Informationen verwenden, um zu bestimmen, welche Typen von Elementen in der Gruppe sind. Die Membertypen werden durch die [Postfachtyp](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) -verwaltete EWS-API-Aufzählung und das [mailboxtype](https://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) -EWS-Element definiert. 
  
**Tabelle 2. Verteilergruppen-Mitgliedstypen**

|**Postfachtyp-Aufzählungswert**|**Mailboxtype-Elementwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Postfach  <br/> |Postfach  <br/> |Ein e-Mail-aktiviertes Active Directory-Objekt.  <br/> |
|Publicgroup  <br/> |PublicDL  <br/> |Eine Verteilergruppe, die in der soeben expandierenden Gruppe enthalten ist. Um eine vollständige Liste der Mitglieder zu erhalten, erweitern Sie auch diese Gruppe.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |Eine Gruppe von Kontakten, die sich im Postfach befindet und nur Benutzern dieses Postfachs zur Verfügung steht.  <br/> |
|Kontakt  <br/> |Kontakt  <br/> |Ein Exchange-Daten Bank Kontakt oder Active Directory e-Mail-Kontakt.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>Verwalten von Verteilergruppen mithilfe der Exchange-Verwaltungsshell

Sie können [Exchange-Verwaltungsshell-Cmdlets](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx) zum Erstellen und Verwalten universeller Verteilergruppen und Sicherheitsgruppen in Ihrem Code verwenden. 
  
> [!NOTE]
> Sie können keine Exchange-Verwaltungsshell-Cmdlets zum Verwalten von Kontaktgruppen verwenden. 
  
**Tabelle 3. Exchange-Verwaltungsshell-Cmdlets für die Verwendung von Verteilergruppen**

|**Cmdlet**|**Verwenden für...**|
|:-----|:-----|
|[Disable-DistributionGroup](https://technet.microsoft.com/library/aa997942%28v=exchg.150%29.aspx) <br/> |Entfernen von e-Mail-Funktionen aus einer e-Mail-aktivierten Verteilergruppe.  <br/> |
|[Enable-DistributionGroup](https://technet.microsoft.com/library/aa998916%28v=exchg.150%29.aspx) <br/> |E-Mail-Aktivierung einer vorhandenen universellen Gruppe.  <br/> |
|[Get-DistributionGroup](https://technet.microsoft.com/library/bb124755%28v=exchg.150%29.aspx) <br/> |Abfrage nach vorhandenen Verteilergruppen.  <br/> |
|[New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx) <br/> |Erstellen Sie eine Verteilergruppe.  <br/> |
|[Remove-DistributionGroup](https://technet.microsoft.com/library/aa997627%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen Verteilergruppe aus AD DS.  <br/> |
|[Set-DistributionGroup](https://technet.microsoft.com/library/bb124955%28v=exchg.150%29.aspx) <br/> |Ändern Sie die Einstellungen einer vorhandenen Verteilergruppe.  <br/> |
|[Add-DistributionGroupMember](https://technet.microsoft.com/library/bb124340%28v=exchg.150%29.aspx) <br/> |Hinzufügen eines Empfängers zu einer Verteilergruppe.  <br/> |
|[Get-DistributionGroupMember](https://technet.microsoft.com/library/aa996367%28v=exchg.150%29.aspx) <br/> |Suchen Sie nach vorhandenen Verteilergruppenmitgliedern.  <br/> |
|[Remove-DistributionGroupMember](https://technet.microsoft.com/library/aa998016%28v=exchg.150%29.aspx) <br/> |Entfernen eines vorhandenen Empfängers aus einer Verteilergruppe.  <br/> |
|[Update-DistributionGroupMember](https://technet.microsoft.com/library/dd335049%28v=exchg.150%29.aspx) <br/> |Aktualisieren Sie ein Mitglied einer angegebenen Verteilergruppe.  <br/> |
|[Get-DynamicDistributionGroup](https://technet.microsoft.com/library/bb124762%28v=exchg.150%29.aspx) <br/> |Dient zum Abrufen der Einstellungen für eine vorhandene dynamische Verteilergruppe.  <br/> |
|[New-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125127%28v=exchg.150%29.aspx) <br/> |Erstellen Sie eine dynamische Verteilergruppe.  <br/> |
|[Remove-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125038%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen dynamischen Verteilergruppe. Dieses Cmdlet entfernt die dynamische Verteilergruppe aus AD DS.  <br/> |
|[Set-DynamicDistributionGroup](https://technet.microsoft.com/library/bb123796%28v=exchg.150%29.aspx) <br/> |Ändern Sie die Einstellungen einer vorhandenen dynamischen Verteilergruppe.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Kontaktgruppen mithilfe von EWS in Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)   
- [Aufrufen von Exchange-Verwaltungsshell-Cmdlets aus verwaltetem Code](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)
    

