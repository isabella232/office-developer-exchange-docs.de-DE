---
title: Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: Hier finden Sie Informationen zu Transaktionsprotokolle und Prüfpunktdateien sowie deren Verwendung zum Sichern und Wiederherstellen von Exchange 2013-Daten.
ms.openlocfilehash: 53f128348bb2e8895bc1eefaf62402fa348c81ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756830"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>Transaktionsprotokolle und Prüfpunktdateien für Sicherung und Wiederherstellung in Exchange

Hier finden Sie Informationen zu Transaktionsprotokolle und Prüfpunktdateien sowie deren Verwendung zum Sichern und Wiederherstellen von Exchange 2013-Daten.
  
**Gilt für:** Exchange Server 2013 
  
In diesem Artikel wird beschrieben, wie Exchange Server 2013-Transaktionsprotokolle und Prüfpunktdateien verwendet, um Datenverluste zu verhindern. Es ist wichtig, dass diese Informationen beim Entwickeln von Sichern und Wiederherstellen von Webanwendungen, die in Versionen von Windows Server beginnend mit Windows Server 2008 den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.
  
## <a name="transaction-logs-in-exchange-2013"></a>In Exchange 2013-Transaktionsprotokolle

Exchange 2013 verwaltet einen einzelnen Satz von Transaktionsprotokolldateien für jede Datenbank. Eine Transaktion ist definiert als alle Vorgänge, die das Bundesland oder den Inhalt der Datenbank ändert. Die Transaktionsprotokolldateien für eine einzelne Datenbankdatensatz alle Transaktionen in der Datenbank ausgeführt werden soll. Datensätze der Transaktionen werden in die Transaktionsprotokolle geschrieben, bevor sie in der Datenbank selbst, gemacht werden, um sicherzustellen, dass alle übergebenen Transaktionen im Fall eines Ausfalls Datenbank wiederhergestellt werden können. Transaktionsprotokolle für Exchange 2013-Datenbank werden auf dem Datenträger gespeichert, bevor die Transaktionen auf die Datenbank übernommen werden. 
  
Die Aufzeichnung der Transaktionen vor dem Aktualisieren der Datenbank wird die Write-ahead-Logging aufgerufen. Um sicherzustellen, dass die Datenbank auf den ordnungsgemäßen Status ordnungsgemäß wieder aufgenommen wurde, schreibt Exchange 2013 Daten in die Datenbankdateien mithilfe von Schreibvorgänge-basierten und Prüfpunkte. Während des normalen Betriebs der Exchange-Informationsspeicher zeichnet zunächst in die Transaktionsprotokolle Datenbank Änderungen, und klicken Sie dann auf eine speicherinterne Kopie der Datenbank werden diese Änderungen vorgenommen. Tragen Sie die Transaktionsprotokolle Anfang und Ende jeder Transaktion. Dadurch wird sichergestellt, dass ausreichend Informationen weiter unten rückgängig gemacht oder Rollback für Vorgänge in der Datenbank verfügbar ist.
  
Beim Wiederherstellen von Fehlern in dem die Datenbankdatei auf dem Datenträger ist beschädigt, und die Transaktionsprotokolle intakt sind, muss Ihre wiederherstellungsanwendung zuerst eine gute Kopie der Datenbankdatei wiederherstellen.
  
Exchange-Speicher gibt die Transaktionen, die zuvor gesicherte Transaktion protokolliert, und klicken Sie dann die Transaktionsprotokolldateien auf dem Datenträger für die verbleibenden Transaktionen gibt. Beachten Sie, dass in einigen Fällen Transaktionen gelöscht werden können, wenn das System zwischen schlägt fehl, wenn die Transaktionen in der Transaktionsprotokolle erfasst werden, und wenn sie tatsächlich in die Datenbankdateien geschrieben werden. 
  
In regelmäßigen Abständen, Exchange-Speicher überprüft das Datenbankbild in-Memory-, und klicken Sie dann bestimmt, welche Seiten geändert haben. Exchange-Speicher kombiniert die ausstehenden Änderungen, und klicken Sie dann auf die Datenbank auf dem Datenträger schreibt diese Seiten.
  
## <a name="checkpoint-files-in-exchange-2013"></a>Prüfpunktdateien in Exchange 2013

Ein Prüfpunkt Datei Datensätze, die Transaktionen protokolliert wurden in die Datenbankdateien auf dem Datenträger geschrieben. Der Prüfpunkt wird geändert, wenn die Datenbankseiten, die von Einträgen in die Transaktionsprotokolle geändert wurden erfolgreich geschrieben werden auf dem Datenträger. Da die Prüfpunktdatei aufzeichnet, welche Transaktionen bereits in der auf dem Datenträger Datenbankbild sind, muss Exchange-Speicher nur Wiedergeben von Transaktionen, die nach dem Checkpoint aufgetreten sind. Je nach den Zeitraum zwischen den Sicherungen kann dies die Anzahl der Transaktionen der reduziert werden, die in die Datenbank wiedergegeben werden, wenn ein Systemfehler auftritt.
  
## <a name="see-also"></a>Siehe auch

- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
- [Wiederherstellen von Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    

