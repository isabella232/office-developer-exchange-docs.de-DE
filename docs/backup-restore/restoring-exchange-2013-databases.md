---
title: Wiederherstellen Exchange 2013-Datenbanken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Hier finden Sie Informationen zu den verschiedenen Möglichkeiten, wie Sie Ihre Exchange 2013-Datenbanken wiederherstellen können.
ms.openlocfilehash: 522128026bcbef893ce4909174d3fd9a95f1e8a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513276"
---
# <a name="restoring-exchange-2013-databases"></a>Wiederherstellen Exchange 2013-Datenbanken

Hier finden Sie Informationen zu den verschiedenen Möglichkeiten, wie Sie Ihre Exchange 2013-Datenbanken wiederherstellen können. 
  
**Gilt für:** Exchange Server 2013 
  
Der in Exchange Server 2013 enthaltene Exchange Writer ermöglicht eine gewisse Flexibilität bei der Wiederherstellung Ihrer Exchange Datenbanken. Mit dem Exchange Writer in Exchange 2013 können Sie Ihre Schattenkopiesicherungen an den folgenden Speicherorten wiederherstellen:
  
- Die ursprüngliche Datenbank, unabhängig davon, ob die Datenbank- oder Transaktionsprotokolldateipfadkonfiguration geändert wurde.
    
- Eine Wiederherstellungsdatenbank.
    
- Jede Produktionsdatenbank, unabhängig davon, ob der Anzeigename der Datenbank mit dem Namen in einem VSS-Sicherungssatz übereinstimmt.
    
Wenn die Wiederherstellungsanwendung Informationen in der ursprünglichen Datenbank wiederherstellt, müssen die Protokolldateien in dem Verzeichnispfad wiederhergestellt werden, der in Active Directory Domain Services (AD DS) für diese Datenbank angegeben ist. Wenn ihre Anwendung eine Datenbank an einem anderen Speicherort wiederhergestellt, müssen die Protokolldateien in einem Ordner namens **_restoredLogs** wiederhergestellt werden, der sich im Verzeichnis der Datenbankprotokolldatei befindet. 
  
Beim Wiederherstellen auf einem Server oder einer Datenbank, die sich von der ursprünglichen Datenbank unterscheidet, muss die Wiederherstellungsanwendung sicherstellen, dass die für VSS bereitgestellten Datenbankverzeichnispfade mit denen in AD DS übereinstimmen. Sie können das Cmdlet ["get-MailboxDatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)Exchange Management Shell" verwenden, um Informationen zu vorhandenen Datenbanken abzurufen. Weitere Informationen zur Exchange-Verwaltungsshell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Die folgende Abbildung zeigt die Abfolge von Ereignissen in einer typischen Wiederherstellung einer Exchange-Datenbank, die vom Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwaltet wird.
  
**Abbildung 1. Abfolge von Ereignissen zum Wiederherstellen von Datenbanken**

![Diagramm der Abfolge von Ereignissen beim Wiederherstellungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Wiederherstellen Exchange Datenbanken am ursprünglichen Speicherort
<a name="bk_OriginalLocation"> </a>

Mit dem Exchange Writer können Anwendungen Datenbanken und Transaktionsprotokolldateien an ihren ursprünglichen Speicherorten auf dem Exchange Server wiederherstellen. Standardmäßig gibt der Exchange Writer die Transaktionsprotokolldateien wieder, nachdem der Antragsteller bestätigt hat, dass die Wiederherstellung während des [OnPostRestore-Vorgangs](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) abgeschlossen ist. Die Wiederherstellungsanwendung muss die VSS [SetAdditionalRestores-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) verwenden, um zu verhindern, dass die Protokolldateien wiedergegeben werden. Die Protokolldateien können zu einem späteren Zeitpunkt wiedergegeben werden, wenn der Exchange-Administrator oder Ihre Anwendung die wiederhergestellte Datenbank erneut bereitgestellt. 
  
Beim Wiederherstellen von Datenbanken auf ihre ursprünglichen Datenbankobjekte (sodass die Ziel-GUIDs in der Datenbank mit denen im Sicherungssatz übereinstimmen), aber in anderen Dateipfaden muss die Anwendung die aktuellen Dateipfade ermitteln und die Sicherungsdateien in den entsprechenden Dateipfaden wiederherstellen, die in den Datenbankeigenschaften angegeben sind. Der Antragsteller muss die [AddNewTarget-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) aufrufen, um dem Exchange Writer den Speicherort mitzuteilen, an dem die Dateien wiederhergestellt werden, bevor der Writer mit dem restliche Wiederherstellungsprozess fortfahren kann. Wenn **AddNewTarget** nicht aufgerufen wird, geht der Exchange Writer davon aus, dass die Sicherungen in den im Sicherungsmetadatendokument angegebenen Dateipfaden wiederhergestellt werden. 
  
In der Regel muss Ihre Anwendung keinen neuen Pfad für Sicherungen angeben, die aus einer DaG-Kopie (Database Availability Group) ausgeführt werden. Exchange Administratoren in der Regel keine Datenbank- oder Protokolldateipfade ändern. In einer DAG-Konfiguration muss die Sicherungsanwendung jedoch möglicherweise die aktiven Datenbank- und Protokollpfade angeben, da sich DAG-Kopierpfade immer von diesen Pfaden unterscheiden.
  
Beachten Sie, dass Exchange 2013 das Wiederherstellen inaktiver DAG-Datenbankkopien nicht unterstützt. DAG-Kopien können nur dann aus Sicherungsdaten wiederhergestellt werden, wenn die aktive Datenbankkopie wiederhergestellt wird. Die Verwendung verschiedener Sicherungsdatensätze oder der Versuch, eine Teilmenge der Datenbankkopien wiederherzustellen, kann dazu führen, dass die Datenbank nicht mehr bereitgestellt werden kann. Sicherungsanwendungen müssen in diesem Fall nicht die [SetRestoreOptions-Funktion](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) aufrufen, da die Sicherungen in den ursprünglichen Datenbankobjekten wiederhergestellt werden, aus denen sie erstellt wurden. Wenn die Sicherungsanwendung jedoch **SetRestoreOptions aufruft** und das XML-Metadatendokument die richtigen Parameter aufweist, ist das Ergebnis kein Fehler. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Wiederherstellen Exchange Datenbanken in einer Wiederherstellungsdatenbank
<a name="bk_RecoveryDatabase"> </a>

Mit dem Exchange Writer können Sie Daten direkt in einer Wiederherstellungsdatenbank wiederherstellen. Die Bereitstellung der wiederhergestellten Daten als Wiederherstellungsdatenbank ermöglicht es dem Exchange-Administrator, einzelne Postfächer und sogar einzelne Elemente in einem Postfach wiederherzustellen.
  
Wenn bereits eine Wiederherstellungsdatenbank vorhanden ist, kann die Anwendung die Bereitstellung der Datenbank aufheben, die Daten in der Wiederherstellungsdatenbank und den Protokolldateien wiederherstellen und dann die Datenbank erneut bereitstellen.
  
Auf jedem Exchange 2013-Server kann jeweils nur eine Wiederherstellungsdatenbank bereitgestellt werden. Der Server kann so viele wiederhergestellte Datenbanken enthalten, wie der Speicherplatz zulässt, aber nur eine kann als Wiederherstellungsdatenbank bereitgestellt werden. Die als Wiederherstellungsdatenbank bereitgestellte Datenbank wird in der maximalen Anzahl von Datenbanken gezählt, die gleichzeitig bereitgestellt werden können. Eine wiederhergestellte Datenbank, die als Wiederherstellungsdatenbank eines Servers bereitgestellt wird, ist dem ursprünglichen Postfach in keiner Weise zugeordnet.
  
Zum Wiederherstellen einer Wiederherstellungsdatenbank muss die Anwendung die [SetRestoreOptions-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) aufrufen und ein XML-Dokument bereitstellen, das die QUELL- und Zieldatenbank-GUIDs angibt. Die Quell-GUIDs müssen mit denen aus dem Sicherungssatz übereinstimmen, und die Ziel-GUIDs müssen mit den Zieldatenbankeinträgen in AD DS übereinstimmen. Die Sicherungsanwendung muss auch die [AddNewTarget-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) aufrufen, um den Verzeichnispfad anzugeben, in dem die Dateien wiederhergestellt werden. Wenn die Datenbankdateien umbenannt werden müssen, benennt der Exchange Writer die Datenbank während des [OnPostRestore-Vorgangs](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) um. Exchange erfordert, dass die Transaktionsprotokolldateien in einem Unterordner ( **_restoredLogs**) unter dem aktuellen Pfad der Transaktionsprotokolldatei wiederhergestellt werden. Wenn die Protokolldateien an einem anderen Speicherort wiederhergestellt werden, gibt der Exchange Writer einen Fehler zurück. Da Datenbanken, die als Wiederherstellungsdatenbank bereitgestellt werden, nicht an ihrem ursprünglichen Speicherort wiederhergestellt werden, müssen sie in den Zustand des sauberen Herunterfahrens versetzt werden, bevor sie bereitgestellt werden können. Standardmäßig versetzt der Exchange Writer alle wiederhergestellten Datenbanken während der Wiederherstellung in einen Zustand des sauberen Herunterfahrens. Wenn ihre Sicherungsanwendung die [SetAdditionalRestores-Methode aufruft,](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) gibt der Exchange Writer die Protokolldateien nicht wieder, und entweder der Administrator oder Ihre Sicherungsanwendung muss die Datenbank in einen Zustand des sauberen Herunterfahrens versetzen, bevor die Datenbank eingebunden wird. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Wiederherstellen Exchange Datenbanken auf einem Wiederherstellungsserver
<a name="bk_RecoveryServer"> </a>

In einigen Szenarien müssen Sie möglicherweise einen Sicherungssatz auf einem anderen Server wiederherstellen. Beispielsweise müssen Sie nach einem schwerwiegenden Serverfehler möglicherweise eine Wiederherstellung durchführen, indem Sie die Postfachdatenbank auf einen anderen Exchange 2013-Server in derselben Exchange Organisation portieren oder auf einen dedizierten Server außerhalb der Produktionsumgebung wiederherstellen, um Postfach- und Öffentliche Ordnerdaten wiederherzustellen. 
  
In diesen Szenarien unterscheiden sich die Dateipfade für die Zieldatenbank sowie ihre Objekt-GUIDs von denen für die ursprüngliche Datenbank. Daher muss Ihre Anwendung die [SetRestoreOptions-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) mit einem XML-Dokument aufrufen, das die Quell- und Zieldatenbankinformationen angibt, und die [AddNewTarget-Methode](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) aufrufen, um die Verzeichnispfade anzugeben, in denen die Sicherungsdateien wiederhergestellt werden sollen. Für den Exchange Writer entspricht diese Wiederherstellung dem Wiederherstellen in einer Wiederherstellungsdatenbank. Weitere Informationen finden Sie unter [Wiederherstellen von Exchange Datenbanken in einer Wiederherstellungsdatenbank](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) weiter oben in diesem Artikel. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
    

