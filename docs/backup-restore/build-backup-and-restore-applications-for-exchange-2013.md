---
title: Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Hier finden Sie Informationen zu den Komponenten und der Architektur von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013 und die Systemanforderungen zum Erstellen einer Sicherungs-und Wiederherstellungsanwendung.
ms.openlocfilehash: f8a332d0816792f8888c97a8394886b026f5204b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455272"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Erstellen von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013

Hier finden Sie Informationen zu den Komponenten und der Architektur von Sicherungs-und Wiederherstellungsanwendungen für Exchange 2013 und die Systemanforderungen zum Erstellen einer Sicherungs-und Wiederherstellungsanwendung.
  
**Gilt für:** Exchange Server 2013 
  
Sie können den [Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS)](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) in Versionen von Windows Server beginnend mit Windows Server 2008 verwenden, um Anwendungen zu erstellen, mit denen Exchange Server 2013 Daten gesichert und wiederhergestellt werden. VSS stellt eine Infrastruktur zur Verfügung, mit der Sie Schattenkopien für Speicher Verwaltungssysteme von Drittanbietern, Geschäftsanwendungen und Hardware erstellen und verwalten können. Sie können Lösungen basierend auf der VSS-Infrastruktur erstellen, die Schattenkopien verwendet, um eine oder mehrere Exchange 2013 Datenbanken zu sichern und wiederherzustellen. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Voraussetzungen für Sicherungs-und Wiederherstellungsanwendungen
<a name="bk_systemrequirements"> </a>

Damit Ihre benutzerdefinierte Sicherungs-und Wiederherstellungsanwendung und VSS Exchange 2013 Datenbanken sichern und wiederherstellen können, muss Ihre Umgebung Folgendes umfassen:
  
- Eine Version von Windows Server, beginnend mit Windows Server 2008 
    
- Exchange 2013
    
Wenn Sie außerdem eine Sicherungs-und Wiederherstellungsanwendung erstellen, sollten Sie die folgenden Einschränkungen für die Entwicklungsumgebung beachten:
  
- VSS ist eine nicht verwaltete COM-API, auf die über eine COM-Interop-Assembly von .NET Framework verwaltetem Code aus zugegriffen werden kann.
    
- Der Exchange-Verwaltungsshell ist eine verwaltete Anwendung, auf die über .NET Framework verwalteter Code zugegriffen wird.
    
- Die CHKSGFILES-API, die mit Exchange 2013 bereitgestellt wird, ist eine 64-Bit-DLL mit systemeigenem Code. Die Verwendung der Exchange 2007 32-Bit-CHKSGFILES-dll mit Exchange 2013 Datenbanken wird nicht unterstützt.
    
## <a name="backup-and-restore-application-overview"></a>Übersicht über die Anwendungssicherung und-Wiederherstellung
<a name="bk_components"> </a>

VSS koordiniert die Kommunikation zwischen den folgenden Komponenten: 
  
- Die VSS-anfordernde, die Ihre Sicherungsanwendung ist
    
- Der VSS-Writer
    
- Der VSS-Anbieter, bei dem es sich um die System-, Software-oder Hardwarekomponenten handelt, die die Schattenkopien erstellen
    
Damit VSS zum Sichern von Exchange 2013 Daten verwendet werden kann, muss die Sicherungsanwendung ein Exchange 2013 fähiger VSS-Anforderer sein. Exchange 2013 enthält einen VSS-Writer, der als Microsoft Exchange Writer bezeichnet wird, für das Windows Server-Sicherungsprogramm; Allerdings sichert der Exchange-Writer nur ganze Volumes. Einzelne Exchange 2013 Datenbanken werden nicht gesichert. Wenn Sie mehr Flexibilität benötigen, können Sie eine Sicherungsanwendung eines Drittanbieters verwenden, die über einen Exchange-fähigen VSS-Writer verfügt, der mit einzelnen Exchange-Datenbanken verwendet werden kann, oder Sie können eine benutzerdefinierte VSS-Anforderung erstellen.
  
Bevor die Anwendung VSS aufruft, um eine Sicherung zu initiieren, muss Sie Informationen zur Speicherkonfiguration für das Exchange 2013 System erhalten, das Sie sichert. Diese Informationen werden in Active Directory-Domänendienste (AD DS) gespeichert. Ihre Sicherungsanwendung kann Exchange-Speicher Konfigurationsdaten mithilfe von Exchange-Verwaltungsshell Befehlen abrufen. Weitere Informationen finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Exchange 2013-Sicherungsanwendungen rufen die VSS-com-APIs auf, um vollständige, Kopie-, differenzielle und inkrementelle Sicherungen von Exchange-Datenbanken zu erstellen. Sie interagieren nicht direkt mit dem VSS-Writer. Die DAG-Funktionalität (Database Availability Group) in Exchange ermöglicht es Ihrer Anwendung auch, eine vollständig konsistente Sicherung zu erstellen, auch wenn die anfängliche vollständige Sicherung und spätere inkrementelle Sicherungen von verschiedenen Servern in der DAG stammen. Nachdem VSS die Kopie der Exchange-Daten erstellt hat, speichert Ihre Sicherungsanwendung die Daten auf den vorgesehenen Medien.
  
Zum Wiederherstellen einer Exchange 2013 Datenbank Ruft die Wiederherstellungsanwendung die Datenbank-und Protokolldateien von den Sicherungsmedien ab und speichert Sie auf dem aktiven Datenträgerspeicher eines Exchange-Servers. Einzelne Datenbanken sind keinem bestimmten Exchange-Server zugeordnet. 
  
Sicherungs-und Wiederherstellungsanwendungen müssen eine Reihe von Exchange 2013 spezifischen Parametern angeben, um die von VSS ausgeführten Vorgänge für Exchange 2013 Datenbanken ordnungsgemäß zu steuern und zu verwalten. Da Exchange 2013 beispielsweise bis zu 100 gleichzeitig aktive Datenbankenunter stützt, muss die Sicherungsanwendung die Datenbankdatei, die Transaktionsprotokolldateien und die Prüfpunktdatei-Datenbankkomponenten ordnungsgemäß angeben und verarbeiten.
  
Zum Rekonstruieren einer Datenbank mit Änderungen seit der letzten vollständigen Wiederherstellung erfordert die Wiederherstellungsanwendung Datenbank-und Protokolldateien aus unterschiedlichen Sicherungen. Es kann beispielsweise eine wöchentliche vollständige Sicherung und eine oder mehrere tägliche inkrementelle Sicherungen erforderlich sein. In Exchange 2013 Systemen, die DAGs verwenden, kann Ihre Wiederherstellungsanwendung eine Datenbank mithilfe von Sicherungen aus unterschiedlichen Datenbankkopien auf unterschiedlichen Servern in derselben DAG neu erstellen. Die einzige unterstützte Möglichkeit zum Wiederherstellen einer DAG-Datenbank aus einer Sicherung besteht jedoch darin, alle aktiven und passiven Kopien der Datenbank mithilfe der gleichen Daten wiederherzustellen.
  
Nachdem alle Daten vorhanden sind, signalisiert Ihre Wiederherstellungsanwendung Exchange, um die Integrität der Datenbank-und Protokolldateien zu überprüfen. Wenn die Datenbank-und Protokolldateien ordnungsgemäß wiederhergestellt wurden, kann der Exchange-Server die Datenbankprotokolldateien wiedergeben, um die Datenbank auf den neuesten Stand zu bringen und Sie bereitzustellen. Wenn die Datenbank auf einem Server wiederhergestellt wurde, auf dem bereits eine aktive Kopie der Datenbank installiert ist, wird die Datenbank als Wiederherstellungsdatenbank behandelt. Wenn die Datenbank auf einem anderen Server wiederhergestellt wurde, kann die Datenbank entweder unabhängig eingebunden werden, oder das Replikat kann dann der DAG hinzugefügt werden.
  
## <a name="backup-and-restore-system-architecture"></a>Systemarchitektur für Sicherung und Wiederherstellung
<a name="bk_ExchangeVSS"> </a>

VSS kommuniziert mit dem Windows Server-Dateisystem und mit dem Massenspeicher-Gerätetreiber über einen Drittanbieter (oder benutzerdefinierten). Der Hardwareanbieter bestimmt, wo die Schattenkopie erstellt wird. VSS abstrahiert die hardwarespezifische Shadow Copy, sodass Ihre Sicherungs-und Wiederherstellungsanwendung ohne Informationen zu den Details zur Hardware Implementierung auf die Schattenkopie zugreifen kann. In der folgenden Abbildung wird gezeigt, wie die Sicherungs-und Wiederherstellungsanwendung mit Exchange 2013 und Windows Server interagiert.
  
**Abbildung 1. Systemarchitektur für Sicherung und Wiederherstellung**

![Diagramm, das zeigt, wie eine Sicherungs- und Wiederherstellungsanwendung interagiert. Zwischen Exchange Windows Server und der Clientanwendung gibt es eine bidirektionale Kommunikation. Der Windows-Server fungiert auch als Massenspeichergerät oder Sicherungsmedium.](media/VSS_architecture_E2k7.gif)
  
Die Sicherungs-und Wiederherstellungsanwendung fungiert als VSS-Anforderer. Der Anforderer kommuniziert mit VSS, um Informationen über Exchange 2013 zu erhalten, um die Erstellung von Schattenkopien zu initiieren und um Zugriff auf die Daten für die Sicherung zu erhalten. 
  
Das Exchange-Informationsspeicher ist eine Komponente von Exchange 2013 und greift über das Windows Server-Dateisystem auf Exchange 2013 Datenbanken zu. Innerhalb des Dateisystems kann jeder Exchange-Server gleichzeitig bis zu 100-Datenbanken mit den zugehörigen Datenbankdateien (EDB), Transaktionsprotokolldateien und einer Prüfpunktdatei einbinden.
  
Zur Unterstützung von VSS enthält Exchange 2013 einen Exchange-Writer, der in der Exchange-Informationsspeicher integriert ist. Der Exchange-Writer koordiniert mit dem Exchange-Informationsspeicher (im Auftrag des anfordernden Betriebs), um die Datenbank vor dem sichern zu fixieren und aufzuheben und anschließend das Einfrieren und Einbinden der Datenbank nach Abschluss der Sicherung aufzuheben. Während einer Wiederherstellung weist die Sicherungs-und Wiederherstellungsanwendung den Exchange-Writer an, sich mit dem Exchange-Informationsspeicher zu koordinieren, um die Bereitstellung der Datenbank aufzuheben, die Datenbankdateien zu ersetzen, die Datenbank bereitzustellen und dann die Transaktionsprotokolle wiederzugeben (je nach Bedarf).
  
Während einer Wiederherstellung kommuniziert die anfordernde Person auch mit VSS, um das System für die Wiederherstellung vorzubereiten und dann die Daten wieder auf das Massenspeichergerät zurückzusetzen. Die Sicherungs-und Wiederherstellungsanwendung ist außerdem für die Zusammenarbeit mit Windows Server zum Lesen von Daten aus und zum Schreiben von Daten auf den Sicherungsspeicher Medien zuständig, unabhängig davon, ob es sich um ein Bandarchiv, ein Speicherbereichsnetzwerk oder ein anderes Sicherungsmedium handelt.
  
Die wiederhergestellte Datenbank kann entweder als reguläre, aktive Datenbank oder als Exchange 2013 Wiederherstellungsdatenbank bereitgestellt werden. Es kann nur eine bereitgestellte Datenbank auf jedem Exchange-Server als Wiederherstellungsdatenbank festgelegt werden.
  
Informationen, die zum erfolgreichen Abschließen von Sicherungs-und Wiederherstellungsvorgängen zwischen Exchange 2013, VSS und der Sicherungs-und Wiederherstellungsanwendung erforderlich sind, werden als Teil der Exchange-Writer-Metadaten übertragen.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Wiederherstellen Exchange 2013 Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Integrität der Sicherung mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Integrität der Sicherung mithilfe des Tools "Eseutil" in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Sicherung und Wiederherstellung für Exchange](backup-and-restore-for-exchange-2013.md) 
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md) 
- [Volumeschattenkopie-Dienst](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

