---
title: Transaktionsprotokolle und Prüfpunktdateien für die Sicherung und Wiederherstellung in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Hier finden Sie Informationen zu Transaktionsprotokollen und Prüfpunktdateien und deren Verwendung zum Sichern und Wiederherstellen Exchange 2013-Daten.
ms.openlocfilehash: ae47c7757a1001f28c467ea58ec87b4ddbc5a5c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513262"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Transaktionsprotokolle und Prüfpunktdateien für die Sicherung und Wiederherstellung in Exchange

Hier finden Sie Informationen zu Transaktionsprotokollen und Prüfpunktdateien und deren Verwendung zum Sichern und Wiederherstellen Exchange 2013-Daten.
  
**Gilt für:** Exchange Server 2013 
  
In diesem Artikel wird beschrieben, wie Exchange Server 2013 Transaktionsprotokolle und Prüfpunktdateien verwendet, um Datenverluste zu verhindern. Es ist wichtig, diese Informationen zu beachten, wenn Sie Sicherungs- und Wiederherstellungsanwendungen entwickeln, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) in Versionen von Windows Server ab Windows Server 2008 verwenden.
  
## <a name="transaction-logs-in-exchange-2013"></a>Transaktionsprotokolle in Exchange 2013

Exchange 2013 verwaltet eine einzelne Gruppe von Transaktionsprotokolldateien für jede Datenbank. Eine Transaktion wird als jeder Vorgang definiert, der den Status oder Inhalt der Datenbank ändert. Die Transaktionsprotokolldateien für eine einzelne Datenbank zeichnen alle Transaktionen auf, die für die Datenbank ausgeführt wurden. Datensätze der Transaktionen werden in die Transaktionsprotokolle geschrieben, bevor sie in der Datenbank selbst erstellt werden, um sicherzustellen, dass alle zugesicherten Transaktionen im Falle eines Datenbankfehlers wiederhergestellt werden können. Exchange 2013-Datenbanktransaktionsprotokolle werden auf dem Datenträger gespeichert, bevor für die Transaktionen ein Commit für die Datenbankdatei ausgeführt wird. 
  
Die Aufzeichnung der Transaktionen vor dem Aktualisieren der Datenbank wird als Write-Ahead-Protokollierung bezeichnet. Um sicherzustellen, dass die Datenbank ordnungsgemäß wieder in den richtigen Zustand versetzt wird, schreibt Exchange 2013 Daten mithilfe von seitenbasierten Schreibvorgängen und Prüfpunkten in die Datenbankdateien. Bei regulären Vorgängen speichert der Exchange zuerst Datenbankänderungen in den Transaktionsprotokollen und nimmt diese Änderungen dann in einer speicherinternen Kopie der Datenbank vor. In den Transaktionsprotokollen werden der Anfang und das Ende jeder Transaktion aufgezeichnet. Dadurch wird sichergestellt, dass für spätere Rückgängig- oder Rollbackvorgänge in der Datenbank ausreichend Informationen verfügbar sind.
  
Bei der Wiederherstellung nach Fehlern, bei denen die Datenbankdatei auf dem Datenträger beschädigt ist, die Transaktionsprotokolle jedoch intakt sind, muss die Wiederherstellungsanwendung zuerst eine bekannte kopie der Datenbankdatei wiederherstellen.
  
Der Exchange speicher gibt die Transaktionen aus den zuvor gesicherten Transaktionsprotokollen wieder und gibt dann alle verbleibenden Transaktionen aus den Transaktionsprotokolldateien auf dem Datenträger wieder. Beachten Sie, dass manchmal Transaktionen verloren gehen können, wenn das System einen Fehler verursacht, zwischen dem Zeitpunkt, an dem die Transaktionen in den Transaktionsprotokollen aufgezeichnet werden, und dem Zeitpunkt, an dem sie tatsächlich in die Datenbankdateien geschrieben werden. 
  
In regelmäßigen Abständen überprüft der Exchange Speicher das In-Memory-Datenbankimage und bestimmt dann, welche Seiten geändert wurden. Der Exchange Speicher kombiniert die ausstehenden Änderungen und schreibt diese Seiten dann in die Datenbankdatei auf dem Datenträger.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Prüfpunktdateien in Exchange 2013

Eine Prüfpunktdatei zeichnet auf, welche protokollierten Transaktionen in die Datenbankdateien auf dem Datenträger geschrieben wurden. Der Prüfpunkt wird erweitert, wenn alle Datenbankseiten, die durch Einträge in den Transaktionsprotokollen geändert wurden, erfolgreich auf den Datenträger geschrieben werden. Da die Prüfpunktdatei aufzeichnet, welche Transaktionen sich bereits im Image der Datenträgerdatenbank befinden, muss der Exchange Speicher nur Transaktionen wiedergeben, die nach dem Prüfpunkt aufgetreten sind. Je nach Zeitraum zwischen Sicherungen kann dies die Anzahl der Transaktionen erheblich verringern, die in der Datenbank wiedergegeben werden müssen, wenn ein Systemfehler auftritt.
  
## <a name="see-also"></a>Siehe auch

- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Wiederherstellen Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    

