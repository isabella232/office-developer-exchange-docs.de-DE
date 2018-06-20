---
title: Wiederherstellen von Exchange 2013-Datenbanken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Hier finden Sie Informationen zu den verschiedenen Möglichkeiten, Ihre Exchange 2013-Datenbanken wiederhergestellt werden kann.
ms.openlocfilehash: d3ca3a884b0ad30f7d7968a9ed435b02aaf205e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756833"
---
# <a name="restoring-exchange-2013-databases"></a>Wiederherstellen von Exchange 2013-Datenbanken

Hier finden Sie Informationen zu den verschiedenen Möglichkeiten, Ihre Exchange 2013-Datenbanken wiederhergestellt werden kann. 
  
**Gilt für:** Exchange Server 2013 
  
Der Exchange-Writer, der enthalten ist, im Exchange Server 2013 gewisse Flexibilität bei, wie Sie Ihre Exchange-Datenbanken wiederherstellen ermöglicht. Mithilfe des Exchange-Writers in Exchange 2013 können Sie an den folgenden Orten die Shadow Copy Sicherungen wiederherstellen:
  
- Die ursprünglichen Datenbank, unabhängig davon, ob die Datenbank oder eines Transaktionsprotokolls Protokoll Pfad Konfiguration geändert wurde.
    
- Wiederherstellungsdatenbank.
    
- Alle Produktionsdatenbank, unabhängig davon, ob der Anzeigename der Datenbank den Namen in einem Sicherungssatz VSS übereinstimmt.
    
Wenn Ihre wiederherstellungsanwendung Informationen in der ursprünglichen Datenbank wiederhergestellt wird, müssen die Protokolldateien auf den Verzeichnispfad in Active Directory-Domänendienste (AD DS) angegebenen für diese Datenbank wiederhergestellt werden. Wenn die Anwendung an einen anderen Speicherort eine Datenbank wiederhergestellt wird, müssen die Protokolldateien wiederhergestellt werden, in einen Ordner namens **_restoredLogs** , die sich im Verzeichnis Datenbankdatei befindet. 
  
Beim Wiederherstellen auf einen Server oder eine Datenbank, die sich von der ursprünglichen Datenbank unterscheidet, muss Ihre wiederherstellungsanwendung sicherstellen, dass die Datenbank Directory Pfade zur Verfügung gestellt, VSS in AD DS übereinstimmen. Das Exchange-Verwaltungsshell-Cmdlet [Get-MailboxDatabase](http://technet.microsoft.com/en-us/library/bb124924%28v=exchg.150%29.aspx)können Sie um Informationen über vorhandene Datenbanken zu erhalten. Weitere Informationen über die Exchange-Verwaltungsshell finden Sie unter [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Die folgende Abbildung zeigt die Abfolge der Ereignisse in einer gewöhnlichen Wiederherstellung von Exchange-Datenbanken, die durch Volume Shadow Copy Service (VSS) verwaltet wird.
  
**Abbildung 1. Abfolge der Ereignisse zum Wiederherstellen von Datenbanken**

![Diagramm der Abfolge von Ereignissen beim Wiederherstellungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Wiederherstellen von Exchange-Datenbanken an den ursprünglichen Speicherort
<a name="bk_OriginalLocation"> </a>

Der Exchange-Writer ermöglicht, dass Anwendungen zum Wiederherstellen von Datenbanken und Transaktionsprotokolldateien an ihrem ursprünglichen Speicherort auf dem Exchange-Server. Standardmäßig gibt der Exchange-Writer die Transaktionsprotokolldateien nach die anfordernden Person bestätigt, dass während des Vorgangs [OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx) die Wiederherstellung abgeschlossen ist. Der wiederherstellungsanwendung muss die VSS- [SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx) -Methode verwenden, um zu verhindern, dass die Protokolldateien wiedergegeben. Die Protokolldateien können zu einem späteren Zeitpunkt wiedergegeben werden, wenn der Exchange-Administrator oder die Anwendung die wiederhergestellte Datenbank stellt wieder bereit. 
  
Beim Wiederherstellen von Datenbanken wieder auf ihre ursprünglichen Datenbank (beispielsweise, dass das Ziel-GUIDs in der Datenbank, mit denen in den Sicherungssatz ein übereinstimmen)-Objekte jedoch unterschiedliche Dateipfade, muss die Anwendung bestimmen der aktuellen Dateipfade und Wiederherstellen die Sicherungsdateien auf den entsprechende Dateipfade in den Datenbankeigenschaften angegeben. Die anfordernde Person muss rufen Sie die [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode, um die Exchange-Writer den Speicherort kommunizieren, in dem die Dateien wiederhergestellt werden, bevor der Writer mit dem Rest des Wiederherstellungsvorgangs fortgesetzt werden kann. Wenn **AddNewTarget** nicht aufgerufen wird, wird der Exchange-Writer davon ausgegangen, dass die Sicherungen in die Sicherung Metadatendokument angegebenen Dateipfade wiederhergestellt werden. 
  
In der Regel muss die Anwendung nicht Geben Sie einen neuen Pfad für Sicherungen, die von einer Kopie der Database Availability Group (DAG) ausgeführt werden. Exchange-Administratoren ändern Datenbank- oder Dateipfade nicht in der Regel. In einer DAG Konfiguration jedoch die backup-Anwendung möglicherweise die aktive Datenbank angeben und Pfade, melden Sie sich, da DAG Kopierpfade immer diesen Pfaden anders sind.
  
Beachten Sie, dass Exchange 2013 Wiederherstellen von Datenbankkopien für inaktive DAG nicht unterstützt. Nur, wenn die aktive Datenbankkopie wiederhergestellt wird, können DAG Kopien von Sicherungsdaten wiederhergestellt werden. Mithilfe der verschiedenen Daten Sicherungssätze oder versuchen, eine Teilmenge der Datenbankkopien wiederherzustellen kann die Datenbank unmountable vertraut verursachen. Backup Applikationen müssen nicht in diesem Fall die [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) -Funktion aufgerufen, da die Sicherungen in der ursprünglichen Datenbankobjekte wiederhergestellt werden, aus der sie erstellt wurden. Jedoch ist, wenn die backup-Anwendung **SetRestoreOptions ruft** und das XML-Metadatendokument die richtigen Parametern hat, das Ergebnis keinen Fehler. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Wiederherstellen von Exchange-Datenbanken in einer Wiederherstellungsdatenbank
<a name="bk_RecoveryDatabase"> </a>

Der Exchange-Writer können Sie Daten direkt auf einer Wiederherstellungsdatenbank wiederhergestellt. Bereitstellen der wiederhergestellten Daten als Wiederherstellungsdatenbank ermöglicht den Exchange-Administrator, um einzelne Postfächer und sogar für einzelne Elemente in einem Postfach wiederherzustellen.
  
Wenn eine Wiederherstellungsdatenbank bereits vorhanden ist, kann Ihre Anwendung Bereitstellung der Datenbank aufzuheben, Wiederherstellen von Daten auf die Datenbank- und Protokolldateien AutoWiederherstellen-Dateien und stellen Sie dann die Datenbank erneut bereit.
  
Jeder Exchange 2013-Server ermöglicht nur eine Wiederherstellungsdatenbank zu einem Zeitpunkt bereitgestellt werden soll. Der Server kann beliebig viele wiederhergestellte Datenbanken wie Speicherplatz zulässt, aber nur eine kann, als der Wiederherstellungsdatenbank bereitgestellt werden enthalten. Die Datenbank als der Wiederherstellungsdatenbank eingebunden wird die maximale Anzahl der Datenbanken gezählt, die zu einem Zeitpunkt bereitgestellt werden können. Eine wiederhergestellte Datenbank bereitgestellt wie Wiederherstellungsdatenbank ein Server nicht mit dem ursprünglichen Postfach keinerlei verknüpft ist.
  
Um einer Wiederherstellungsdatenbank Schäden, Ihrer Anwendung die [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) -Methode aufrufen und liefert ein XML-Dokument, der angibt, die Quelle und Ziel-Datenbank-GUIDs. Die Quelle GUIDs muss mit denen aus den Sicherungssatz ein übereinstimmen, und das Ziel GUIDs muss die Ziel-Datenbankeinträge in AD DS übereinstimmen. Die backup-Anwendung muss auch aufrufen, die [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode, um den Pfad zum Verzeichnis angeben, in dem die Dateien wiederhergestellt werden. Wenn die Datenbankdateien umbenannt werden müssen, wird der Exchange-Writer die Datenbank während des Vorgangs [OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx) umbenennen. Exchange erfordert die Transaktionsprotokolldateien in einem Unterordner ( **_restoredLogs**) wiederhergestellt werden unter den aktuellen Pfad der Transaktionsprotokolldateien. Wenn die Protokolldateien in einem anderen Speicherort wiederhergestellt werden, wird der Exchange-Writer einen Fehler zurück. Da Datenbanken bereitgestellt wird, als der Wiederherstellungsdatenbank nicht an ihrem ursprünglichen Speicherort wiederhergestellt werden, müssen sie in clean Shutdown-Status gebracht werden, bevor diese bereitgestellt werden können. Standardmäßig wird der Exchange-Writer alle wiederhergestellten Datenbanken in einem clean Shutdown-Status während Post-restore bringen. Wenn Ihre backup-Anwendung die [SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx) -Methode aufgerufen, der Exchange-Writer nicht die Protokolldateien wiedergeben wird und der Administrator oder Ihre backup-Anwendung benötigt, um die Datenbank in einen Zustand "clean Shutdown" vor dem Bereitstellen der -Datenbank. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Wiederherstellen von Exchange-Datenbanken auf einen Wiederherstellungsserver
<a name="bk_RecoveryServer"> </a>

In einigen Szenarien müssen Sie möglicherweise einen Sicherungssatz an einen anderen Server wiederherstellen; Beispielsweise müssen Sie möglicherweise durch die Postfachdatenbank auf einen anderen Exchange 2013-Server in der gleichen Exchange-Organisation Portieren von eines Serverausfalls wiederherstellen, oder auf einen dedizierten Server außerhalb der produktionsumgebung Postfach wiederherstellen wiederherstellen und Daten in öffentlichen Ordnern. 
  
In diesen Szenarien unterscheiden sich die Dateipfade für die Zieldatenbank sowie die Objekt-GUIDs als die für die ursprüngliche Datenbank. Aus diesem Grund muss die Anwendung die [SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx) -Methode mit einem XML-Dokument aufrufen, der angibt, die Quell- und Ziel Datenbankinformationen, und rufen Sie die [AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode zum Angeben der Directory Pfade ein, um die Sicherungsdateien zum Wiederherstellen . Für die Exchange-Writer ist Wiederherstellung wiederherstellen in einer Wiederherstellungsdatenbank identisch. Weitere Informationen finden Sie unter [Wiederherstellen von Exchange-Datenbanken in einer Wiederherstellungsdatenbank](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) weiter oben in diesem Artikel. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sicherung und Wiederherstellung Konzepte für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Referenz für die CChkSGFiles](cchksgfiles-class-reference.md)
    

