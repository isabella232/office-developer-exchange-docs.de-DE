---
title: eDiscovery in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Erfahren Sie mehr über eDiscovery in EWS in Exchange.
ms.openlocfilehash: 0b4f211e7f8a6ec085fd03ada1cc5a35187106e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512310"
---
# <a name="ediscovery-in-ews-in-exchange"></a>eDiscovery in EWS in Exchange

Erfahren Sie mehr über eDiscovery in EWS in Exchange.
  
eDiscovery ist ein Webdienst für Sammelabfragen, mit dem externe Anwendungen Abfragen von Exchange Daten ausführen können.
  
Die Ermittlung besteht aus mehreren Phasen, darunter das Identifizieren und Beibehalten von Schlüsseldaten, das Auswendigen und Überprüfen der Daten und das Erstellen von Daten vor Gericht. eDiscovery-Abfragen erleichtern den Ermittlungsprozess, indem ein einzelner Ermittlungsworkflow über Exchange und SharePoint bereitgestellt wird.
  
## <a name="ediscovery-operations"></a>eDiscovery-Vorgänge

Die eDiscovery-Funktion, die von EWS verfügbar gemacht wird, ist über Vorgänge verfügbar, die in Exchange Online eingeführt wurden, Exchange Online als Teil von Office 365 und Versionen von Exchange ab Exchange 2013. 
  
**Tabelle 1. Neue Vorgänge für eDiscovery**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Ruft Konfigurationsinformationen für in-situ-Haltebereiche, gespeicherte Suchvorgänge und die Postfächer ab, die für die Ermittlungssuche aktiviert sind.  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Ruft den Status eines abfragebasierten Haltebereichs ab, der mithilfe des [SetHoldOnMailboxes-Vorgangs](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)festgelegt wird.  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Ruft Details zu Elementen ab, die nicht indiziert werden können. Dazu gehören, aber nicht beschränkt auf, der Elementbezeichner, ein Fehlercode, eine Fehlerbeschreibung, wann versucht wurde, das Element zu indiziert, und zusätzliche Informationen zur Datei.  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können.  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Ruft eine Liste der Postfächer ab, für die der Client über die Berechtigung zum Suchen oder Ausführen von eDiscovery verfügt.  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Sucht nach Elementen in bestimmten Postfächern, die Abfragestichwörtern entsprechen.  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Legt einen abfragebasierten Haltebereich für Elemente fest.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

