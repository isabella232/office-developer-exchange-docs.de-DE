---
title: eDiscovery in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Informationen Sie zu eDiscovery in EWS in Exchange.
ms.openlocfilehash: 6491fdd9f2246870a89bfa89bf7d97b972d67c92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756823"
---
# <a name="ediscovery-in-ews-in-exchange"></a>eDiscovery in EWS in Exchange

Informationen Sie zu eDiscovery in EWS in Exchange.
  
eDiscovery ist ein Verbundpartner Query-Webdienst, der externe Anwendungen, die zum Ausführen von Abfragen von Exchange-Daten ermöglicht.
  
Ermittlung besteht aus mehreren Phasen, einschließlich identifizieren und Beibehalten von wichtigen Daten, culling nach unten und Überprüfen der Daten und Daten in gerichtlichen erzeugt. eDiscovery-Abfragen erleichtern den Suchprozess durch Bereitstellen eines einzelnen Discovery Workflows über Exchange und SharePoint.
  
## <a name="ediscovery-operations"></a>eDiscovery-Vorgänge

EDiscovery-Funktionalität, die vom Exchange-Webdienste verfügbar gemacht wird ist über Vorgänge eingeführt in Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2013-Versionen verfügbar. 
  
**In Tabelle 1. Neue Vorgänge für eDiscovery**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |Ruft die Konfigurationsinformationen für Compliance-Archive, gespeicherte Discovery-Suche und die Postfächer, die für die Ermittlung Suche aktiviert sind.  <br/> |
|[GetHoldOnMailboxes](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |Ruft den Status einer abfragebasierte Aufbewahrung, die mit der [SetHoldOnMailboxes-Vorgang](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)festgelegt ist.  <br/> |
|[GetNonIndexableItemDetails](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |Ruft die Details zu den Elementen, die nicht indiziert werden können. Dies umfasst, jedoch ist nicht beschränkt auf, die Element-ID, ein Fehlercode, eine fehlerbeschreibung, wenn versucht wurde, das Element und zusätzliche Informationen zur Datei zu indizieren.  <br/> |
|[GetNonIndexableItemStatistics](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |Ruft die Anzahl der Elemente, die in einem Postfach nicht indiziert werden kann.  <br/> |
|[GetSearchableMailboxes](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |Ruft einer Liste der Postfächer, die der Client verfügt über die Berechtigung zum Durchsuchen oder zum Ausführen von eDiscovery auf.  <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |Sucht nach Elementen in bestimmte Postfächer, die von Abfrageschlüsselwörtern entsprechen.  <br/> |
|[SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |Legt ein abfragebasiertes enthalten Elemente.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

