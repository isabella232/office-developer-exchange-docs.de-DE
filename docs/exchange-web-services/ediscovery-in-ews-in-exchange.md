---
title: eDiscovery in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Erfahren Sie mehr über eDiscovery in EWS in Exchange.
ms.openlocfilehash: 48e3fdb3a2f21f7dcfcb7eed21b586e099b249a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456094"
---
# <a name="ediscovery-in-ews-in-exchange"></a>eDiscovery in EWS in Exchange

Erfahren Sie mehr über eDiscovery in EWS in Exchange.
  
eDiscovery ist ein Webdienst für die Verbund Abfrage, mit dem externe Anwendungen Abfragen von Exchange-Daten ausführen können.
  
Die Ermittlung umfasst mehrere Phasen, darunter das identifizieren und beibehalten von Schlüsseldaten, das Ausmerzen und Überprüfen der Daten und das Erstellen von Daten vor Gericht. eDiscovery-Abfragen erleichtern den Ermittlungsprozess durch Bereitstellen eines einzelnen Discovery-Workflows in Exchange und SharePoint.
  
## <a name="ediscovery-operations"></a>eDiscovery-Vorgänge

Die eDiscovery-Funktionalität, die von EWS verfügbar gemacht wird, ist über Vorgänge verfügbar, die in Exchange Online eingeführt werden, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2013 beginnen. 
  
**Tabelle 1. Neue Vorgänge für eDiscovery**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Ruft Konfigurationsinformationen für in-Place-Speicher, gespeicherte Ermittlungs suchen und die für die Ermittlungs Suche aktivierten Postfächer ab.  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Ruft den Status eines abfragebasierten haltebereichs ab, der mithilfe des [SetHoldOnMailboxes-Vorgangs](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)festgelegt wird.  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Ruft Details zu Elementen ab, die nicht indiziert werden können. Dies umfasst, jedoch nicht auf die Element-ID, einen Fehlercode, eine Fehlerbeschreibung, bei dem Versuch, das Element zu indizieren, sowie zusätzliche Informationen zur Datei.  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können.  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Ruft eine Liste von Postfächern ab, für die der Client über die Berechtigung zum Durchsuchen oder Ausführen von eDiscovery verfügt.  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Sucht nach Elementen in bestimmten Postfächern, die Abfrageschlüsselwörtern entsprechen.  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Legt einen abfragebasierten Haltebereich für Elemente fest.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

