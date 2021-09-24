---
title: Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Hier finden Sie Informationen zu den Komponenten und der Architektur von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013 sowie zu den Systemanforderungen für das Erstellen einer Sicherungs- und Wiederherstellungsanwendung.
ms.openlocfilehash: 590ac029e157196d370cbcbe54e5df75bc1a830b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513878"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Erstellen von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013

Hier finden Sie Informationen zu den Komponenten und der Architektur von Sicherungs- und Wiederherstellungsanwendungen für Exchange 2013 sowie zu den Systemanforderungen für das Erstellen einer Sicherungs- und Wiederherstellungsanwendung.
  
**Gilt für:** Exchange Server 2013 
  
Sie können den [Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS)](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) in Versionen von Windows Server ab Windows Server 2008 verwenden, um Anwendungen zu erstellen, die Exchange Server 2013-Daten sichern und wiederherstellen. VSS bietet eine Infrastruktur, mit der Sie Schattenkopien über Speicherverwaltungssysteme, Geschäftsanwendungen und Hardware von Drittanbietern hinweg erstellen und verwalten können. Sie können Lösungen basierend auf der VSS-Infrastruktur erstellen, die Schattenkopien verwenden, um eine oder mehrere Exchange 2013-Datenbanken zu sichern und wiederherzustellen. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Voraussetzungen für die Sicherung und Wiederherstellung der Anwendung
<a name="bk_systemrequirements"> </a>

Damit Ihre benutzerdefinierte Sicherungs- und Wiederherstellungsanwendung und VSS Exchange 2013-Datenbanken sichern und wiederherstellen können, muss Ihre Umgebung Folgendes enthalten:
  
- Eine Version von Windows Server ab Windows Server 2008 
    
- Exchange 2013
    
Wenn Sie eine Sicherungs- und Wiederherstellungsanwendung erstellen, sollten Sie außerdem die folgenden Einschränkungen für die Entwicklungsumgebung beachten:
  
- VSS ist eine nicht verwaltete COM-API, auf die über .NET Framework verwalteten Code über eine COM-Interopassembly zugegriffen werden kann.
    
- Die Exchange-Verwaltungsshell ist eine verwaltete Anwendung, auf die über .NET Framework verwalteten Code zugegriffen wird.
    
- Die CHKSGFILES-API, die mit Exchange 2013 bereitgestellt wird, ist eine 64-Bit-DLL mit systemeigenem Code. Die Verwendung der 32-Bit-CHKSGFILES-DLL Exchange 2007 mit Exchange 2013-Datenbanken wird nicht unterstützt.
    
## <a name="backup-and-restore-application-overview"></a>Übersicht über die Sicherung und Wiederherstellung der Anwendung
<a name="bk_components"> </a>

VSS koordiniert die Kommunikation zwischen den folgenden Komponenten: 
  
- Der VSS-Anforderer, bei dem es sich um Ihre Sicherungsanwendung handelt
    
- Der VSS Writer
    
- Der VSS-Anbieter, bei dem es sich um System-, Software- oder Hardwarekomponenten handelt, die die Schattenkopien erstellen
    
Um VSS zum Sichern Exchange 2013-Daten zu verwenden, muss ihre Sicherungsanwendung ein Exchange 2013-fähiger VSS-Anforderer sein. Exchange 2013 enthält einen VSS Writer, der als Microsoft Exchange Writer bezeichnet wird, für das Windows Serversicherungsprogramm; Der Exchange Writer sichert jedoch nur ganze Volumes. Einzelne Exchange 2013-Datenbanken werden nicht gesichert. Wenn Sie mehr Flexibilität benötigen, können Sie eine Sicherungsanwendung eines Drittanbieters verwenden, die über einen Exchange-fähigen VSS Writer verfügt, der mit einzelnen Exchange Datenbanken arbeiten kann, oder Sie können einen benutzerdefinierten VSS-Anforderer erstellen.
  
Bevor Ihre Anwendung VSS aufruft, um eine Sicherung zu initiieren, muss sie Informationen zur Speicherkonfiguration für das Exchange 2013-System abrufen, das gesichert wird. Diese Informationen werden in Active Directory Domain Services (AD DS) gespeichert. Ihre Sicherungsanwendung kann mithilfe Exchange Verwaltungsshell-Befehlen Exchange Speicherkonfigurationsdaten abrufen. Weitere Informationen finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell).](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
  
Exchange 2013-Sicherungsanwendungen rufen die VSS-COM-APIs auf, um vollständige, kopierende, differenzielle und inkrementelle Sicherungen von Exchange Datenbanken zu erstellen. Sie interagieren nicht direkt mit dem VSS Writer. Die Funktionalität der Datenbankverfügbarkeitsgruppe (Database Availability Group, DAG) in Exchange ermöglicht Ihrer Anwendung auch das Erstellen einer vollständig konsistenten Sicherung, auch wenn die anfängliche vollständige Sicherung und spätere inkrementelle Sicherungen von verschiedenen Servern in der DAG stammen. Nachdem VSS die Kopie der Exchange Daten erstellt hat, speichert Ihre Sicherungsanwendung die Daten auf den beabsichtigten Medien.
  
Zum Wiederherstellen einer Exchange 2013-Datenbank ruft die Wiederherstellungsanwendung die Datenbank und Protokolldateien von den Sicherungsmedien ab und speichert sie auf dem aktiven Datenträgerspeicher eines Exchange Servers. Einzelne Datenbanken sind keinem bestimmten Exchange Server zugeordnet. 
  
Sicherungs- und Wiederherstellungsanwendungen müssen eine Reihe von Exchange 2013-spezifischen Parametern angeben, um Vorgänge, die von VSS für Exchange 2013-Datenbanken ausgeführt werden, ordnungsgemäß zu steuern und zu verwalten. Da Exchange 2013 beispielsweise bis zu 100 gleichzeitig aktive Datenbanken unterstützt, muss die Sicherungsanwendung die Datenbankdatei, Transaktionsprotokolldateien und Datenbankkomponenten der Prüfpunktdatei korrekt angeben und verarbeiten.
  
Um eine Datenbank zu rekonstruieren, die seit dem letzten vollständigen Zurück Änderungen aufwies, erfordert ihre Wiederherstellungsanwendung Datenbank- und Protokolldateien aus verschiedenen Sicherungen. Es kann beispielsweise eine wöchentliche vollständige Sicherung und mindestens eine tägliche inkrementelle Sicherung erforderlich sein. In Exchange 2013-Systemen, die DAGs verwenden, kann Ihre Wiederherstellungsanwendung eine Datenbank mithilfe von Sicherungen aus verschiedenen Datenbankkopien auf verschiedenen Servern in derselben DAG neu erstellen. Die einzige unterstützte Methode zum Wiederherstellen einer DAG-Datenbank aus der Sicherung besteht jedoch darin, alle aktiven und passiven Kopien der Datenbank mit denselben Daten wiederherzustellen.
  
Nachdem alle Daten vorhanden sind, signalisiert die Wiederherstellungsanwendung Exchange, die Integrität der Datenbank und der Protokolldateien zu überprüfen. Wenn die Datenbank und die Protokolldateien ordnungsgemäß wiederhergestellt wurden, kann der Exchange Server die Datenbankprotokolldateien erneut wiedergeben, um die Datenbank auf dem neuesten Stand zu halten und sie zu einbinden. Wenn die Datenbank auf einem Server wiederhergestellt wurde, auf dem bereits eine aktive Kopie der bereitgestellten Datenbank vorhanden ist, wird die Datenbank als Wiederherstellungsdatenbank behandelt. Wenn die Datenbank auf einem anderen Server wiederhergestellt wurde, kann die Datenbank entweder unabhängig bereitgestellt oder dann der DAG hinzugefügt werden.
  
## <a name="backup-and-restore-system-architecture"></a>Sichern und Wiederherstellen der Systemarchitektur
<a name="bk_ExchangeVSS"> </a>

VSS kommuniziert mit dem Windows Serverdateisystem und mit dem Massenspeichergerätetreiber über einen Drittanbieter (oder benutzerdefinierten Anbieter). Der Hardwareanbieter bestimmt, wo die Schattenkopie erstellt wird. VSS abstrahiert die hardwarespezifische Schattenkopie, sodass Ihre Sicherungs- und Wiederherstellungsanwendung ohne Informationen zu den Hardwareimplementierungen auf die Schattenkopie zugreifen kann. Die folgende Abbildung zeigt, wie Ihre Sicherungs- und Wiederherstellungsanwendung mit Exchange 2013 und Windows Server interagiert.
  
**Abbildung 1. Sichern und Wiederherstellen der Systemarchitektur**

![Diagramm, das zeigt, wie eine Sicherungs- und Wiederherstellungsanwendung interagiert. Zwischen Exchange Windows Server und der Clientanwendung gibt es eine bidirektionale Kommunikation. Der Windows-Server fungiert auch als Massenspeichergerät oder Sicherungsmedium.](media/VSS_architecture_E2k7.gif)
  
Die Sicherungs- und Wiederherstellungsanwendung fungiert als VSS-Anforderer. Der Antragsteller kommuniziert mit VSS, um Informationen zu Exchange 2013 zu erhalten, die Erstellung von Schattenkopien zu initiieren und Zugriff auf die Daten für die Sicherung zu erhalten. 
  
Der Exchange Speicher ist eine Komponente von Exchange 2013 und greift über das Dateisystem Windows Server auf Exchange 2013-Datenbanken zu. Innerhalb des Dateisystems kann jeder Exchange Server gleichzeitig bis zu 100 Datenbanken mit den zugehörigen Datenbankdateien (.edb), Transaktionsprotokolldateien und einer Prüfpunktdatei bereitstellen.
  
Zur Unterstützung von VSS enthält Exchange 2013 einen Exchange Writer, der in den Exchange Speicher integriert ist. Der Exchange Writer koordiniert sich mit dem Exchange Speicher (der im Auftrag des Anforderers ausgeführt wird), um die Datenbank zu fixieren und die Bereitstellung aufzuheben, bevor sie gesichert wird, und die Datenbank nach Abschluss der Sicherung wieder freizugeben und einzuhängen. Während einer Wiederherstellung weist die Sicherungs- und Wiederherstellungsanwendung den Exchange Writer an, sich mit dem Exchange Speicher zu koordinieren, um die Bereitstellung der Datenbank zu aufheben, die Datenbankdateien zu ersetzen, die Datenbank einzuhängen und dann die Transaktionsprotokolle (nach Bedarf) wiederzugeben.
  
Während einer Wiederherstellung kommuniziert der Anforderer auch mit VSS, um das System für die Wiederherstellung vorzubereiten und die Daten dann wieder auf dem Massenspeichergerät zu speichern. Ihre Sicherungs- und Wiederherstellungsanwendung ist auch für die Arbeit mit Windows Server verantwortlich, um Daten aus dem Sicherungsspeichermedium zu lesen und in diese zu schreiben, sei es ein Bandarchiv, ein Speicherbereichsnetzwerk oder ein anderes Sicherungsmedium.
  
Die wiederhergestellte Datenbank kann entweder als reguläre, aktive Datenbank oder als Exchange 2013-Wiederherstellungsdatenbank bereitgestellt werden. Auf jedem Exchange Server kann nur eine bereitgestellte Datenbank als Wiederherstellungsdatenbank festgelegt werden.
  
Informationen, die zum erfolgreichen Abschließen von Sicherungs- und Wiederherstellungsvorgängen zwischen Exchange 2013, VSS und Ihrer Sicherungs- und Wiederherstellungsanwendung erforderlich sind, werden als Teil der Exchange Writer-Metadaten übertragen.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Wiederherstellen Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Sicherungsintegrität mithilfe der CHKSGFILES-API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Sicherungsintegrität mithilfe des Eseutil-Tools in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Sicherung und Wiederherstellung für Exchange](backup-and-restore-for-exchange-2013.md) 
- [CChkSGFiles-Klassenreferenz](cchksgfiles-class-reference.md) 
- [Volumeschattenkopie-Dienst](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

