---
title: Verteilergruppen und EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: Erfahren Sie mehr über die verschiedenen Typen von Verteilergruppen, die in Exchange verfügbar sind, und wie Sie diese in Ihrer verwalteten EWS-API oder EWS-Anwendung verwalten können.
ms.openlocfilehash: 71dc1a1e4c71310943eb19f8a5d6b3f470ab7ccb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512303"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>Verteilergruppen und EWS in Exchange

Erfahren Sie mehr über die verschiedenen Typen von Verteilergruppen, die in Exchange verfügbar sind, und wie Sie diese in Ihrer verwalteten EWS-API oder EWS-Anwendung verwalten können.
  
Eine Verteilergruppe ist eine Sammlung von E-Mail-Adressen, die mit einem einzelnen Alias oder E-Mail-Adresse verknüpft sind. Verteilergruppen (auch verteilerlisten genannt) ermöglichen es einem Benutzer, E-Mails mithilfe einer einzigen Empfängeradresse an mehrere Personen zu senden. Da die Mitgliedschaft in Verteilergruppen und damit die Nachrichtenempfänger außerhalb einzelner E-Mail-Threads verwaltet werden können, bieten Verteilergruppen eine hervorragende Möglichkeit, die Verteilung von E-Mails an eine Benutzergruppe zu ermöglichen. Sie können Verteilergruppen mithilfe der verwalteten EWS-API, EWS und der Exchange-Verwaltungsshell programmgesteuert erstellen und verwalten. Bevor Sie mit der Programmierung beginnen, sehen wir uns die verschiedenen Arten von Verteilergruppen an, die verfügbar sind, und Ihre Optionen für deren Verwaltung.
  
## <a name="types-of-distribution-groups"></a>Typen von Verteilergruppen

Exchange unterstützt drei Arten von Verteilergruppen:
  
- [Universelle Verteilergruppen](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) – Universelle Active Directory-Verteilergruppenobjekte, die E-Mail-aktiviert sind. Universelle Verteilergruppen werden verwendet, um Nachrichten an eine Gruppe von Empfängern zu verteilen. 
    
- [Sicherheitsgruppen](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) – Active Directory-Objekte, die E-Mail-aktiviert sind; auch als universelle Sicherheitsgruppen bezeichnet. Sicherheitsgruppen werden verwendet, um Ressourcen in Active Directory Domain Services (AD DS) Zugriffsberechtigungen zuzuweisen und Nachrichten zu verteilen. 
    
- [Kontaktgruppen](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) – private Verteilergruppen, die sich im Postfach eines Benutzers befinden. 
    
Welche Art von Verteilergruppe Sie auswählen, hängt davon ab, wo Sie die Verteilergruppe speichern möchten, wer sie verwenden wird und wofür sie verwendet wird.

<a name="bk_DistributionGroup"> </a>

### <a name="universal-distribution-groups"></a>Universelle Verteilergruppen

Sie können universelle Verteilergruppen verwenden, um Empfängergruppen in einem einzelnen Alias oder einer E-Mail-Adresse zu konsolidieren. Da universelle Verteilergruppen in AD DS gespeichert sind, kann jeder sie zum Senden von E-Mails verwenden, einschließlich Benutzern außerhalb Ihrer Organisation. Sie können die verwaltete EWS-API oder EWS verwenden, um eine Verteilergruppe zu erweitern. Zum Erstellen und Verwalten von Verteilergruppen müssen Sie jedoch [Exchange Verwaltungsshell-Cmdlets](#bk_UsingEMS)verwenden.
  
Sie können auch universelle Verteilergruppen verwenden, um eine Sammlung von Räumen zu enthalten. Beispielsweise, um Benutzern die Suche nach einem Konferenzraum für eine Besprechung zu erleichtern. Benutzer können einer Besprechungsanfrage eine Raumliste – eine universelle Verteilergruppe, die Raumressourcenpostfächer enthält – hinzufügen, um einen verfügbaren Raum zu finden, ohne jeden Raum einzeln hinzufügen zu müssen.
  
Sie können eine statische universelle Verteilergruppe erstellen, die bis zum Aktualisieren der Mitgliedschaft gleich bleibt, oder Sie können eine dynamische universelle Verteilergruppe erstellen. Eine dynamische universelle Verteilergruppe fragt E-Mail-aktivierte Active Directory-Objekte ab und erstellt die Gruppenmitgliedschaft basierend auf den Ergebnissen. Die Gruppenmitgliedschaft wird jeweils neu berechnet, wenn eine E-Mail-Nachricht an die Gruppe gesendet wird. 

<a name="bk_SecurityGroup"> </a>

### <a name="security-groups"></a>Sicherheitsgruppen

Universelle Verteilergruppen und Sicherheitsgruppen sind auf die meisten Arten identisch. Im Gegensatz zu universellen Verteilergruppen können Sie jedoch Sicherheitsgruppen verwenden, um Netzwerkressourcen in AD DS Berechtigungen zuzuweisen. Sie können die verwaltete EWS-API oder EWS nicht zum Erstellen und Verwalten von Sicherheitsgruppen verwenden. Stattdessen verwenden Sie [Exchange Verwaltungsshell-Cmdlets.](#bk_UsingEMS) Wie universelle Verteilergruppen können Sie jedoch die verwaltete EWS-API oder EWS verwenden, um Sicherheitsgruppen zu erweitern.

<a name="bk_ContactGroup"> </a>

### <a name="contact-groups"></a>Kontaktgruppen

Wenn Sie nicht jedem Benutzer administrativen Zugriff auf den Server gewähren möchten, um Verteilergruppen zu erstellen, aber sie zum Senden einer einzelnen Nachricht an eine große Sammlung von Personen aktivieren möchten, können Sie dazu Kontaktgruppen verwenden. Einer Kontaktgruppe ist keine E-Mail-Adresse zugeordnet, und sie ist nur im Postfach eines Benutzers vorhanden. andere Benutzer haben keinen Zugriff darauf. Sie können [die verwaltete EWS-API oder EWS verwenden, um Kontaktgruppen zu erstellen.](how-to-create-contact-groups-by-using-ews-in-exchange.md)
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>Verwalten von Verteilergruppen mithilfe der verwalteten EWS-API oder EWS

Sie können die verwaltete EWS-API oder EWS verwenden, um eine universelle Verteilergruppe oder Sicherheitsgruppe zu erweitern und die Erstellung und Verwaltung einer Kontaktgruppe zu steuern. Sie können diese Technologien jedoch nicht verwenden, um die Mitglieder dieser Gruppen zu erstellen oder zu bearbeiten. 
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Verwalten von Verteilergruppen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|**Verwenden Sie...**|
|:-----|:-----|:-----|
|[ContactGroup-Klassenmethoden](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Erstellen Sie eine Kontaktgruppe im Exchange Store.<br/><br/>**HINWEIS:** Sie können keine universelle Verteiler- oder Sicherheitsgruppe mithilfe der verwalteten EWS-API oder EWS erstellen.           |
|[ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Erweitern Sie eine universelle Verteilergruppe, Sicherheitsgruppe oder Kontaktgruppe, indem Sie eine Liste ihrer Mitglieder abrufen.  <br/> |
|[FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Suchen Sie nach Kontaktgruppen im Postfach.  <br/> |
|[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Dient zum Abrufen einer Auflistung aller Räume in einer angegebenen Raumliste in einer Organisation. Eine Raumliste ist eine Verteilergruppe, die nur Raumressourcenpostfächer enthält.  <br/> |
|[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Suchen Sie nach möglichen Kandidaten, und geben Sie sie zurück, um mit einem mehrdeutigen Namen übereinzugleichen. Die Kandidaten können Verteilergruppen sein.  <br/> |
   
Sie können die von der [ExpandGroup-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) oder dem [ExpandDL-Vorgang](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) zurückgegebenen Informationen verwenden, um zu bestimmen, welche Typen von Mitgliedern in der Gruppe vorhanden sind. Die Membertypen werden durch die Enumeration der verwalteten [MailboxType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) EWS-API und das MailboxType EWS-Element definiert. [](https://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) 
  
**Tabelle 2. Typen von Verteilergruppen-Mitgliedstypen**

|**MailboxType-Enumerationswert**|**MailboxType-Elementwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Postfach  <br/> |Postfach  <br/> |Ein E-Mail-aktiviertes Active Directory-Objekt.  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |Eine Verteilergruppe, die in der Gruppe enthalten ist, die Sie gerade erweitert haben. Um eine vollständige Liste der Mitglieder zu erhalten, erweitern Sie auch diese Gruppe.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |Eine Gruppe von Kontakten, die sich im Postfach befindet und nur für Benutzer dieses Postfachs verfügbar ist.  <br/> |
|Kontakt  <br/> |Kontakt  <br/> |Ein Exchange Datenbankkontakt oder Active Directory-E-Mail-Kontakt.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>Verwalten von Verteilergruppen mithilfe der Exchange-Verwaltungsshell

Sie können [Exchange Verwaltungsshell-Cmdlets verwenden,](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx) um universelle Verteilergruppen und Sicherheitsgruppen in Ihrem Code zu erstellen und zu verwalten. 
  
> [!NOTE]
> Sie können Exchange Verwaltungsshell-Cmdlets nicht zum Verwalten von Kontaktgruppen verwenden. 
  
**Tabelle 3. Exchange Cmdlets der Verwaltungsshell für die Arbeit mit Verteilergruppen**

|**Cmdlet**|**Verwenden Sie...**|
|:-----|:-----|
|[Disable-DistributionGroup](https://technet.microsoft.com/library/aa997942%28v=exchg.150%29.aspx) <br/> |Entfernen von E-Mail-Funktionen aus einer E-Mail-aktivierten Verteilergruppe.  <br/> |
|[Enable-DistributionGroup](https://technet.microsoft.com/library/aa998916%28v=exchg.150%29.aspx) <br/> |E-Mail-Aktivierung einer vorhandenen universellen Gruppe.  <br/> |
|[Get-DistributionGroup](https://technet.microsoft.com/library/bb124755%28v=exchg.150%29.aspx) <br/> |Abfrage vorhandener Verteilergruppen.  <br/> |
|[New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx) <br/> |Erstellen sie eine Verteilergruppe.  <br/> |
|[Remove-DistributionGroup](https://technet.microsoft.com/library/aa997627%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen Verteilergruppe aus AD DS.  <br/> |
|[Set-DistributionGroup](https://technet.microsoft.com/library/bb124955%28v=exchg.150%29.aspx) <br/> |Ändern der Einstellungen einer vorhandenen Verteilergruppe.  <br/> |
|[Add-DistributionGroupMember](https://technet.microsoft.com/library/bb124340%28v=exchg.150%29.aspx) <br/> |Hinzufügen eines Empfängers zu einer Verteilergruppe.  <br/> |
|[Get-DistributionGroupMember](https://technet.microsoft.com/library/aa996367%28v=exchg.150%29.aspx) <br/> |Suchen vorhandener Verteilergruppenmitglieder.  <br/> |
|[Remove-DistributionGroupMember](https://technet.microsoft.com/library/aa998016%28v=exchg.150%29.aspx) <br/> |Entfernen eines vorhandenen Empfängers aus einer Verteilergruppe.  <br/> |
|[Update-DistributionGroupMember](https://technet.microsoft.com/library/dd335049%28v=exchg.150%29.aspx) <br/> |Dient zum Aktualisieren eines Mitglieds einer angegebenen Verteilergruppe.  <br/> |
|[Get-DynamicDistributionGroup](https://technet.microsoft.com/library/bb124762%28v=exchg.150%29.aspx) <br/> |Rufen Sie die Einstellungen für eine vorhandene dynamische Verteilergruppe ab.  <br/> |
|[New-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125127%28v=exchg.150%29.aspx) <br/> |Erstellen sie eine dynamische Verteilergruppe.  <br/> |
|[Remove-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125038%28v=exchg.150%29.aspx) <br/> |Löschen einer vorhandenen dynamischen Verteilergruppe. Mit diesem Cmdlet wird die dynamische Verteilergruppe aus AD DS entfernt.  <br/> |
|[Set-DynamicDistributionGroup](https://technet.microsoft.com/library/bb123796%28v=exchg.150%29.aspx) <br/> |Ändern der Einstellungen einer vorhandenen dynamischen Verteilergruppe.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Erstellen von Kontaktgruppen mithilfe von EWS in Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)   
- [Aufrufen Exchange-Verwaltungsshell-Cmdlets über verwalteten Code](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)
    

