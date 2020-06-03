---
title: Wiederherstellen Exchange 2013 Datenbanken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: Hier finden Sie Informationen zu den verschiedenen Möglichkeiten zum Wiederherstellen der Exchange 2013 Datenbanken.
ms.openlocfilehash: 9fe417bda5dc728af619da02d62ada6e920f731d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528673"
---
# <a name="restoring-exchange-2013-databases"></a>Wiederherstellen Exchange 2013 Datenbanken

Hier finden Sie Informationen zu den verschiedenen Möglichkeiten zum Wiederherstellen der Exchange 2013 Datenbanken. 
  
**Gilt für:** Exchange Server 2013 
  
Der in Exchange Server 2013 enthaltene Exchange-Writer ermöglicht eine gewisse Flexibilität bei der Wiederherstellung Ihrer Exchange-Datenbanken. Wenn Sie den Exchange-Writer in Exchange 2013 verwenden, können Sie Ihre Shadow Copy-Sicherungen an den folgenden Speicherorten wiederherstellen:
  
- Die ursprüngliche Datenbank, unabhängig davon, ob die Datei Pfadkonfiguration der Datenbank oder des Transaktionsprotokolls geändert wurde.
    
- Eine Wiederherstellungsdatenbank.
    
- Jede Produktionsdatenbank, unabhängig davon, ob der Anzeigename der Datenbank mit dem Namen in einem VSS-Sicherungssatzes übereinstimmt.
    
Wenn Ihre Wiederherstellungsanwendung Informationen in der ursprünglichen Datenbank wieder herstellt, müssen die Protokolldateien in dem Verzeichnispfad wiederhergestellt werden, der in Active Directory-Domänendienste (AD DS) für diese Datenbank angegeben ist. Wenn Ihre Anwendung eine Datenbank an einem anderen Speicherort wieder herstellt, müssen die Protokolldateien in einem Ordner mit dem Namen **_restoredLogs** , der sich im Datenbankprotokolldatei Verzeichnis befindet, wiederhergestellt werden. 
  
Bei der Wiederherstellung auf einem Server oder einer Datenbank, die sich von der ursprünglichen Datenbank unterscheidet, muss Ihre Wiederherstellungsanwendung sicherstellen, dass die für VSS bereitgestellten Datenbankverzeichnis Pfade denen in AD DS entsprechen. Sie können das Cmdlet [Get-MailboxDatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)Exchange-Verwaltungsshell verwenden, um Informationen zu vorhandenen Datenbanken abzurufen. Weitere Informationen zum Exchange-Verwaltungsshell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
In der folgenden Abbildung ist die Abfolge der Ereignisse in einer typischen Wiederherstellung einer Exchange-Datenbank dargestellt, die vom Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwaltet wird.
  
**Abbildung 1. Sequenz von Ereignissen zum Wiederherstellen von Datenbanken**

![Diagramm der Abfolge von Ereignissen beim Wiederherstellungsprozess. Die Abfolge beginnt mit den Startvorgängen des Exchange-Speichers und setzt sich in zahlreichen Schritten zwischen dem Exchange Writer, VSS und der Clientanwendung fort.](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Wiederherstellen von Exchange-Datenbanken am ursprünglichen Speicherort
<a name="bk_OriginalLocation"> </a>

Der Exchange-Writer ermöglicht es Anwendungen, Datenbanken und Transaktionsprotokolldateien an ihren ursprünglichen Speicherorten auf dem Exchange-Server wiederherzustellen. Standardmäßig werden die Transaktionsprotokolldateien vom Exchange-Writer wiedergegeben, nachdem die Anforderung bestätigt hat, dass die Wiederherstellung während des [OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) -Vorgangs abgeschlossen ist. Die Wiederherstellungsanwendung muss die VSS- [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) -Methode verwenden, um zu verhindern, dass die Protokolldateien wiedergegeben werden. Die Protokolldateien können zu einem späteren Zeitpunkt wiedergegeben werden, wenn der Exchange-Administrator oder Ihre Anwendung die wiederhergestellte Datenbank erneut einbinden. 
  
Wenn Sie Datenbanken wieder auf ihre ursprünglichen Datenbankobjekte wiederherstellen (sodass die Ziel-GUIDs in der Datenbank mit denen im Sicherungssatzes übereinstimmen), aber mit unterschiedlichen Dateipfaden, muss die Anwendung die aktuellen Dateipfade ermitteln und die Sicherungsdateien in den entsprechenden Dateipfaden wiederherstellen, die in den Datenbankeigenschaften angegeben sind. Die anfordernde Person muss die [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode aufrufen, um dem Exchange-Writer den Speicherort zu kommunizieren, an dem die Dateien wiederhergestellt werden, bevor der Writer mit dem Rest des Wiederherstellungsvorgangs fortfahren kann. Wenn **AddNewTarget** nicht aufgerufen wird, geht der Exchange-Writer davon aus, dass die Sicherungen in den Dateipfaden wiederhergestellt werden, die im Dokument Sicherungsmetadaten angegeben sind. 
  
In der Regel muss Ihre Anwendung keinen neuen Pfad für Sicherungen angeben, die von einer DAG-Kopie (Database Availability Group) ausgeführt werden. Exchange-Administratoren ändern normalerweise keine Datenbank-oder Protokolldateipfade. In einer DAG-Konfiguration muss die Sicherungsanwendung jedoch möglicherweise die aktiven Datenbank-und Protokollpfade angeben, da sich die Pfade von DAG-Kopien immer von diesen Pfaden unterscheiden.
  
Beachten Sie, dass Exchange 2013 das Wiederherstellen inaktiver DAG-Datenbankkopien nicht unterstützt. DAG-Kopien können nur dann aus Sicherungsdaten wiederhergestellt werden, wenn die aktive Datenbankkopie wiederhergestellt wird. Wenn Sie unterschiedliche Sicherungsdaten Sätze verwenden oder versuchen, eine Teilmenge der Datenbankkopien wiederherzustellen, kann dies dazu führen, dass die Datenbank nicht mehr bereitgestellt wird. Sicherungsanwendungen müssen in diesem Fall nicht die Funktion [setrestoreoptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) aufrufen, da die Sicherungen in den ursprünglichen Datenbankobjekten wiederhergestellt werden, aus denen Sie erstellt wurden. Wenn die Sicherungsanwendung **setrestoreoptions** aufruft und das XML-Metadaten-Dokument die richtigen Parameter aufweist, ist das Ergebnis jedoch kein Fehler. 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Wiederherstellen von Exchange-Datenbanken in einer Wiederherstellungsdatenbank
<a name="bk_RecoveryDatabase"> </a>

Mit dem Exchange-Writer können Sie Daten direkt in einer Wiederherstellungsdatenbank wiederherstellen. Durch das Einbinden der wiederhergestellten Daten als Wiederherstellungsdatenbank kann der Exchange-Administrator einzelne Postfächer und sogar einzelne Elemente in einem Postfach wiederherstellen.
  
Wenn bereits eine Wiederherstellungsdatenbank vorhanden ist, kann Ihre Anwendung die Bereitstellung der Datenbank aufheben, die Daten in der Wiederherstellungsdatenbank und die Protokolldateien wiederherstellen und dann die Datenbank erneut einbinden.
  
Jeder Exchange 2013 Server ermöglicht jeweils nur die Bereitstellung einer Wiederherstellungsdatenbank. Der Server kann so viele wiederhergestellte Datenbanken enthalten, wie der Speicherplatz zulässt, aber nur einer kann als Wiederherstellungsdatenbank eingebunden werden. Die Datenbank, die als Wiederherstellungsdatenbank bereitgestellt wird, wird in der maximalen Anzahl von Datenbanken gezählt, die gleichzeitig eingebunden werden können. Eine wiederhergestellte Datenbank, die als Wiederherstellungsdatenbank eines Servers bereitgestellt wurde, ist nicht mit dem ursprünglichen Postfach in irgendeiner Weise verknüpft.
  
Zum Wiederherstellen in einer Wiederherstellungsdatenbank muss Ihre Anwendung die [setrestoreoptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) -Methode aufrufen und ein XML-Dokument bereitstellen, das die GUIDs der Quell-und Zieldatenbank angibt. Die Quell-GUIDs müssen mit denen des Sicherungssatzes übereinstimmen, und die Ziel-GUIDs müssen mit den Einträgen der Zieldatenbank in AD DS übereinstimmen. Die Sicherungsanwendung muss auch die [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode aufrufen, um den Verzeichnispfad anzugeben, in dem die Dateien wiederhergestellt werden. Wenn die Datenbankdateien umbenannt werden müssen, wird der Exchange-Writer die Datenbank während des [OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx) -Vorgangs umbenennen. Exchange erfordert, dass die Transaktionsprotokolldateien in einem Unterordner ( **_restoredLogs**) unterhalb des aktuellen Pfads der Transaktionsprotokolldatei wiederhergestellt werden. Wenn die Protokolldateien an einem anderen Speicherort wiederhergestellt werden, gibt der Exchange-Writer einen Fehler zurück. Da Datenbanken, die als Wiederherstellungsdatenbank bereitgestellt werden, nicht an Ihrem ursprünglichen Speicherort wiederhergestellt werden, müssen Sie vor der Bereitstellung in den Zustand Clean-Shutdown gebracht werden. Standardmäßig bringt der Exchange-Writer alle wiederhergestellten Datenbanken während der Post-Wiederherstellung in den Zustand Clean Shutdown. Wenn Ihre Sicherungsanwendung die [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) -Methode aufruft, werden die Protokolldateien vom Exchange-Writer nicht wiedergegeben, und der Administrator oder Ihre Sicherungsanwendung muss die Datenbank vor dem Bereitstellen der Datenbank in den Zustand "Clean Shutdown" umsetzen. 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Wiederherstellen von Exchange-Datenbanken auf einem Wiederherstellungsserver
<a name="bk_RecoveryServer"> </a>

In einigen Szenarien müssen Sie möglicherweise einen Sicherungssatzes auf einem anderen Server wiederherstellen. Beispielsweise müssen Sie möglicherweise nach einem katastrophalen Serverfehler wiederherstellen, indem Sie die Postfachdatenbank auf einen anderen Exchange 2013 Server in derselben Exchange-Organisation portieren oder auf einem dedizierten Server außerhalb der Produktionsumgebung wiederherstellen, um Postfachdaten und öffentliche Ordner-Daten wiederherzustellen. 
  
In diesen Szenarien unterscheiden sich die Dateipfade für die Zieldatenbank sowie deren Objekt-GUIDs von denen für die ursprüngliche Datenbank. Daher muss Ihre Anwendung die [setrestoreoptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) -Methode mit einem XML-Dokument aufrufen, das die Quell-und Ziel Datenbankinformationen angibt, und die [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) -Methode aufrufen, um die Verzeichnispfade anzugeben, in denen die Sicherungsdateien wiederhergestellt werden sollen. Für den Exchange-Writer ist diese Wiederherstellung identisch mit der Wiederherstellung in einer Wiederherstellungsdatenbank. Weitere Informationen finden Sie unter [Wiederherstellen von Exchange-Datenbanken in einer Wiederherstellungsdatenbank](restoring-exchange-2013-databases.md#bk_RecoveryDatabase) weiter oben in diesem Artikel. 
  
## <a name="see-also"></a>Siehe auch
<a name="bk_AdditionalResources"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Sichern und Wiederherstellen von Konzepten für Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md)
    

