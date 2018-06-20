---
title: Sicherung und Wiederherstellung für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Hier finden Sie Informationen zum Erstellen der Sicherung und Wiederherstellen Sie Anwendungen für Exchange 2013.
ms.openlocfilehash: 9eceb3d512a73ad9cb07a01864fb8b029d5b5772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756801"
---
# <a name="backup-and-restore-for-exchange"></a>Sicherung und Wiederherstellung für Exchange
  
Exchange Server 2013 bietet Database Availability Groups (DAGs), die gespeicherte Daten sicher und verfügbar ist, halten und reduzieren die Notwendigkeit für benutzerdefinierte Sicherung und Wiederherstellung von Anwendungen helfen. DAGs aktivieren Offsite Datenredundanz, um sicherzustellen, dass Daten werden nicht verloren gehen. Jedoch weiterhin viele Disaster Recovery-Pläne enthalten traditionellere Sicherung und Wiederherstellung von Methoden und Systeme, einschließlich benutzerdefinierte Anwendungen, für die Redundanz mit der DAG. Um die Verfügbarkeit der Daten und Redundanz in Ihrer Organisation zu gewährleisten, können Sie benutzerdefinierte Anwendungen erstellen, die Exchange-Server und Windows Server-Betriebssystem-Technologien zum Sichern und Wiederherstellen von Exchange-Daten verwenden.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Sicherungstechnologien in Exchange 2013

Exchange 2013 enthält eine-Plug-In für Windows Server-Sicherung, mit denen Administratoren können VSS-basierte Sicherungskopien der Exchange-Daten zu erstellen. Administratoren können auch Windows Server-Sicherung zum Sichern und Wiederherstellen von Exchange-Datenbanken. Wenn Sie eine Sicherung erstellen und die Anwendung für Exchange 2013 wiederherstellen, müssen Sie zum Erstellen einer Exchange-fähigen Anwendung, die den VSS Writer für Exchange 2013 unterstützt, und verwenden Sie die CHKSGFILES-API zum Überprüfen der Konsistenz von, dass die Sicherung. Weitere Informationen finden Sie unter [backup Validate-Integrität mithilfe der API für CHKSGFILES in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>VSS Writer in Exchange 2013

Exchange 2013 führt eine bedeutende Änderung in die VSS Writer-Architektur in Exchange Server 2010 und Exchange Server 2007. Exchange 2010 und Exchange 2007 umfassen zwei VSS Writer: eine in der Exchange-Informationsspeicherdienst (store.exe) und das andere in der Exchange-Replikationsdienst (msexchangerepl.exe). In Exchange 2013, die VSS Writer-Funktionalität in der Exchange-Replikationsdienst befindet sich. Die Sicherung und Wiederherstellung Anwendung verwendet des neuen VSS-Writers, die Microsoft Exchange-Writer aufgerufen, um aktive und passive Datenbankkopien zu sichern, und Informationen zum Wiederherstellen der Sicherung Datenbankkopien. Obwohl der neue VSS Writer in der Exchange-Replikationsdienst ausgeführt wird, muss der Exchange-Informationsspeicherdienst in Reihenfolge für den Writer verfügbar sein soll ausgeführt werden. Daher sind beide Dienste zum Sichern oder Wiederherstellen von Exchange-Datenbanken erforderlich.
  
Obwohl die VSS Writer-Architektur in Exchange 2013 aktualisiert wurde, wird die zugrunde liegende Funktionalität wurde nicht geändert. Wenn Sie eine Anwendung für Sicherung und Wiederherstellung für Exchange 2010 erstellt haben, müssen Sie keine Änderungen an Ihre Anwendung für Exchange 2013 vorgenommen. Achten Sie darauf, dass die Anwendung zur Sicherstellung der Kompatibilität mit den neuesten erneut kompilieren. Für Sicherung und Wiederherstellung Applikationen für Exchange 2007 oder früheren Versionen erstellt wurden müssen Sie schreiben Sie den Code, um die neuesten CHKSGFILES-API verwenden.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Was müssen Sie wissen über VSS-Sicherung und Wiederherstellung

|Wenn Sie wissen möchten, zu...|Lesen Sie diesen Artikel|
|:-----|:-----|
|Anwendungsarchitekturen  <br/> |Sicherung und Wiederherstellung Anwendungen verwenden, VSS Sichern von Exchange-Datenbanken in der Regel ein Hintergrunddienst, der die Sicherung ausgeführt wird, eine scheduling-Dienst und eine Windows-GUI-Anwendung-Konsole, die Steuerelemente und konfiguriert die Sicherung bestehen und System wiederherstellen.  <br/> |
|Remoteverwendung  <br/> |VSS zum Sichern von Exchange-Servern verwenden, müssen auf dem Computer Windows Server 2008 ausführen, auf denen Exchange-Informationsspeicher-Prozess ausgeführt wird. Aufgrund der Flexibilität in großen Speichersystemen möglicherweise die Hardware, auf der Speichervolumes nicht physisch Teil des Computers mit Windows Server 2008.  <br/> |
|Sprachen und Tools  <br/> |Eine beliebige COM-kompatible Sprache können Sie VSS verwenden Es wird am häufigsten in C++-Anwendung verwendet. Da Sie den Exchange-Speicher durchführen, um Schattenkopien erstellt haben, sind backup in der Regel dringende, die in den meisten Fällen macht Sprachen wie Visual Basic oder VBScript verwenden.  <br/> |
|Verwaltete Implementierung  <br/> |Sie können die VSS-APIs in einer Umgebung mit verwaltetem Code über eine COM-Interop-Assembly.  <br/> |
|Skriptfähigkeit  <br/> |Ja, aber nicht empfohlen.  <br/> |
|Verfügbare Test- und Debuggingtools  <br/> |Keine besondere Tools sind erforderlich, um Anwendungen Debuggen, mit denen die Windows VSS an.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Referenz für die CChkSGFiles](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Siehe auch

- [Volumeschattenkopie-Dienst (Windows)](http://msdn.microsoft.com/en-us/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange-Verwaltungsshell](../management/exchange-management-shell.md)   
- [Transport-Agents in Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

