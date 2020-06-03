---
title: Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Hier finden Sie Informationen zu Transaktionsprotokollen und Prüfpunktdateien sowie dazu, wie diese zum Sichern und Wiederherstellen von Exchange 2013 Daten verwendet werden.
ms.openlocfilehash: 5b01fc6924f82e76943795df877ae84b1fde087b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456388"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange

Hier finden Sie Informationen zu Transaktionsprotokollen und Prüfpunktdateien sowie dazu, wie diese zum Sichern und Wiederherstellen von Exchange 2013 Daten verwendet werden.
  
**Gilt für:** Exchange Server 2013 
  
In diesem Artikel wird beschrieben, wie Exchange Server 2013 Transaktionsprotokolle und Prüfpunktdateien zur Verhinderung von Datenverlust verwendet. Bei der Entwicklung von Sicherungs-und Wiederherstellungsanwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) in Windows Server-Versionen mit Windows Server 2008 verwenden, ist es wichtig, diese Informationen zu berücksichtigen.
  
## <a name="transaction-logs-in-exchange-2013"></a>Transaktionsprotokolle in Exchange 2013

Exchange 2013 verwaltet eine einzelne Gruppe von Transaktionsprotokolldateien für jede Datenbank. Eine Transaktion ist als jede Operation definiert, die den Status oder den Inhalt der Datenbank ändert. Die Transaktionsprotokolldateien für eine einzelne Datenbank zeichnen alle Transaktionen auf, die für die Datenbank ausgeführt wurden. Datensätze der Transaktionen werden in die Transaktionsprotokolle geschrieben, bevor Sie in der Datenbank selbst vorgenommen werden, um sicherzustellen, dass alle zugesicherten Transaktionen im Falle eines Datenbankfehlers wiederhergestellt werden können. Exchange 2013 Datenbank-Transaktionsprotokolle werden auf dem Datenträger gespeichert, bevor die Transaktionen an die Datenbankdatei übergeben werden. 
  
Die Aufzeichnung der Transaktionen vor der Aktualisierung der Datenbank wird als Write-Ahead-Protokollierung bezeichnet. Um sicherzustellen, dass die Datenbank ordnungsgemäß wieder in den ordnungsgemäßen Zustand zurückgeführt wird, schreibt Exchange 2013 Daten in die Datenbankdateien mithilfe von seitenbasierten Schreibvorgängen und Prüfpunkten. Während regulärer Vorgänge zeichnet das Exchange-Informationsspeicher zunächst Datenbankänderungen in den Transaktionsprotokollen auf und nimmt dann diese Änderungen an einer speicherinternen Kopie der Datenbank vor. Die Transaktionsprotokolle zeichnen den Anfang und das Ende jeder Transaktion auf. Dadurch wird sichergestellt, dass für spätere rückgängig-oder Rollback-Vorgänge in der Datenbank ausreichende Informationen verfügbar sind.
  
Bei der Wiederherstellung nach Fehlern, bei denen die Datenbankdatei auf dem Datenträger beschädigt ist, die Transaktionsprotokolle jedoch intakt sind, muss Ihre Wiederherstellungsanwendung zuerst eine bekanntermaßen einwandfreie Kopie der Datenbankdatei wiederherstellen.
  
In der Exchange-Informationsspeicher werden die Transaktionen aus den zuvor gesicherten Transaktionsprotokollen wiedergegeben, und anschließend werden alle verbleibenden Transaktionen aus den Transaktionsprotokolldateien der Festplatte wiedergegeben. Beachten Sie, dass Transaktionen manchmal verloren gehen können, wenn das System zwischen dem Auftreten der Transaktionen in den Transaktionsprotokollen und der tatsächlichen Speicherung in die Datenbankdateien fehlschlägt. 
  
In regelmäßigen Abständen prüft das Exchange-Informationsspeicher das in-Memory-Datenbankbild und bestimmt dann, welche Seiten geändert wurden. Das Exchange-Informationsspeicher kombiniert die ausstehenden Änderungen und schreibt diese Seiten dann in die Datenbankdatei auf dem Datenträger.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Prüfpunktdateien in Exchange 2013

Eine Prüfpunktdatei zeichnet die protokollierten Transaktionen auf, die in die Datenbankdateien auf der Festplatte geschrieben wurden. Der Prüfpunkt ist fortgeschritten, wenn alle Datenbankseiten, die von Einträgen in den Transaktionsprotokollen geändert wurden, erfolgreich auf den Datenträger geschrieben wurden. Da in der Prüfpunktdatei aufgezeichnet wird, welche Transaktionen sich bereits im Daten Bank Abbild auf der Festplatte befinden, muss der Exchange-Informationsspeicher nur Transaktionen wiedergeben, die nach dem Prüfpunkt aufgetreten sind. Je nach Zeitraum zwischen Sicherungen kann dies erheblich verringern die Anzahl der Transaktionen, die in der Datenbank wiedergegeben werden müssen, wenn ein Systemfehler auftritt.
  
## <a name="see-also"></a>Siehe auch

- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Wiederherstellen Exchange 2013 Datenbanken](restoring-exchange-2013-databases.md)
    

