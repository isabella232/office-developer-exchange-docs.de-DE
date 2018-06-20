---
title: Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Hier finden Sie Informationen zu den Komponenten und der Sicherung und Wiederherstellung von Anwendungen für Exchange 2013-Architektur und die Systemanforderungen für das Erstellen einer Sicherung und Wiederherstellung Anwendung.
ms.openlocfilehash: e85a5364c40c472c9e1ea9d1d3b4e89329b1676f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756812"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Erstellen von Sicherung und Wiederherstellen von Anwendungen für Exchange 2013

Hier finden Sie Informationen zu den Komponenten und der Sicherung und Wiederherstellung von Anwendungen für Exchange 2013-Architektur und die Systemanforderungen für das Erstellen einer Sicherung und Wiederherstellung Anwendung.
  
**Gilt für:** Exchange Server 2013 
  
Können den [Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS)](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) in Versionen von Windows Server beginnend mit Windows Server 2008 um zu erstellen, das Sichern und Wiederherstellen von Exchange Server 2013-Daten. VSS stellt eine Infrastruktur, die die ermöglicht Ihnen das Erstellen und Verwalten von Schattenkopien über Drittanbieter-Speicher-Management-Systemen, Geschäftsanwendungen und Hardware. Sie können Lösungen auf Grundlage der VSS-Infrastruktur erstellen, die Schattenkopien zum Sichern und Wiederherstellen von Datenbanken für eine oder mehrere Exchange 2013 verwenden. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Sicherung und Wiederherstellung Anwendung erforderliche Komponenten
<a name="bk_systemrequirements"> </a>

In der Reihenfolge für Ihre benutzerdefinierte Sicherung und Wiederherstellung und VSS zum Sichern und Wiederherstellen von Exchange 2013-Datenbanken muss die Umgebung Folgendes umfassen:
  
- Eine Version von Windows Server beginnend mit Windows Server 2008 
    
- Exchange 2013
    
Darüber hinaus, wenn Sie eine Sicherung erstellen und Anwendung wiederherstellen, sollten Sie die folgenden Einschränkungen auf die Entwicklungsumgebung beachten:
  
- VSS wird von einer nicht verwalteten COM-API, die vom verwalteten .NET Framework-Code über eine COM-Interop-Assembly zugegriffen werden kann.
    
- Die Exchange-Verwaltungsshell ist einer verwalteten Anwendung, die über verwalteten .NET Framework-Code zugegriffen werden kann.
    
- Die CHKSGFILES-API, die bereitgestellt wird, mit Exchange 2013 ist eine 64-Bit-DLL systemeigenem Code. Verwenden der Exchange 2007-32-Bit-CHKSGFILES DLL mit Exchange 2013-Datenbanken wird nicht unterstützt.
    
## <a name="backup-and-restore-application-overview"></a>Übersicht über Sicherung und Wiederherstellung
<a name="bk_components"> </a>

VSS koordiniert die Kommunikation zwischen den folgenden Komponenten: 
  
- Der VSS-Requester, die Ihre backup-Anwendung ist
    
- Der VSS-writer
    
- Der VSS-Anbieter, der ist das System, Software oder Hardware-Komponenten, die die Schattenkopien erstellen
    
Zur Verwendung von VSS zum Sichern von Exchange 2013-Daten muss Ihre backup-Anwendung ein Exchange 2013-fähigen VSS-Requester. Exchange 2013 umfasst einen VSS-Writer, die Microsoft Exchange-Writer für Windows Server backup-Programm aufgerufen. Allerdings sichert der Exchange Writer nur ganze Volumes. Es werden nicht gesichert einzelne Exchange 2013 Datenbanken. Wenn Sie mehr Flexibilität benötigen, können Sie eine Drittanbieter-backup-Anwendung, die einen Exchange-fähige VSS Writer verfügt, die mit den einzelnen Exchange-Datenbanken können, oder Sie können eine benutzerdefinierte VSS anfordernde Person erstellen.
  
Bevor Sie die Anwendung zum Initiieren einer Sicherung VSS aufruft, benötigen sie Informationen über die Speicherkonfiguration für Exchange 2013 System, die sie sichern. Diese Informationen werden in Active Directory-Domänendienste (AD DS) gespeichert. Exchange-Speicher-Konfigurationsdaten erhalten Ihre backup-Anwendung mithilfe der Exchange-Verwaltungsshell-Befehle. Weitere Informationen finden Sie unter [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Backup Exchange 2013-Anwendungen rufen die VSS COM-APIs für das Erstellen voll ist, kopieren, differenzielle und inkrementelle Sicherungen von Exchange-Datenbanken. Sie interagieren nicht direkt mit der VSS-Writer. Die Database Availability Group (DAG)-Funktionalität in Exchange kann auch die Anwendung zum Erstellen einer Sicherungskopie vollständig konsistenten, selbst wenn die erste vollständige Sicherung und später inkrementelle Sicherungen von verschiedenen Servern in der DAG stammen. Nachdem VSS die Kopie des Exchange-Daten erstellt hat, werden Ihre backup-Anwendung die Daten auf den vorgesehenen Datenträger gespeichert.
  
Zum Wiederherstellen einer Datenbank Exchange 2013 Ihrer wiederherstellungsanwendung die Datenbank- und Protokolldateien Dateien vom Sicherungsmedium abgerufen, und speichert diese in den aktiven Datenträgerspeicher eines Exchange-Servers. Einzelne Datenbanken werden nicht mit einem bestimmten Exchange-Server verbunden sind. 
  
Sicherung und Wiederherstellung Applikationen müssen eine Anzahl von Exchange 2013-spezifischen Parametern ordnungsgemäß Steuerung und Verwaltung durch VSS in Exchange 2013-Datenbanken auszuführen, Vorgänge angeben. Beispielsweise, da Exchange 2013 bis zu 100 gleichzeitig aktive Datenbanken unterstützt, muss die backup-Anwendung ordnungsgemäß angeben und Verarbeiten der Datenbankdatei, Transaktionsprotokolldateien und Prüfpunkt Datei Datenbankkomponenten.
  
Um eine Datenbank wiederherzustellen, die Änderungen seit der letzten vollständigen Sicherung haben, erfordert die wiederherstellungsanwendung Datenbank- und Protokolldateien Dateien aus verschiedenen Sicherungen. Beispielsweise könnte eine wöchentliche vollständige Sicherung und täglich inkrementelle Sicherungen erforderlich. In Exchange kann 2013-Systeme, die DAGs verwenden, Ihre wiederherstellungsanwendung eine Datenbank neu erstellen mithilfe von Sicherungen von verschiedenen Datenbankkopien auf unterschiedlichen Servern in derselben DAG. Es ist jedoch die einzige Möglichkeit zum Wiederherstellen einer DAG-Datenbank aus einer Sicherung alle aktive und passive Kopien der Datenbank mit denselben Daten wiederherstellen.
  
Nachdem alle Daten ist, signalisiert Ihrer wiederherstellungsanwendung Exchange so überprüfen Sie die Integrität der Datenbank- und Protokolldateien. Wenn die Datenbank und-Protokolldateien ordnungsgemäß wiederhergestellt wurden, kann der Exchange-Server klicken Sie dann Protokolldateien der Datenbank, um die Datenbank auf dem aktuellen Stand zu bringen, und stellen Sie es. Wenn die Datenbank auf einem Server, die bereits eine aktive Kopie der Datenbank bereitgestellt wiederhergestellt wurde, wird die Datenbank als Datenbank wiederherstellen behandelt. Wenn die Datenbank auf einem anderen Server wiederhergestellt wurde, die Datenbank kann entweder unabhängig voneinander bereitgestellt oder dieses Replikat kann in der DAG hinzugefügt werden.
  
## <a name="backup-and-restore-system-architecture"></a>Sicherung und Wiederherstellung Systemarchitektur
<a name="bk_ExchangeVSS"> </a>

VSS kommuniziert mit dem Dateisystem Windows Server und mit den Gerätetreiber Massenspeichergerät über einen Anbieter von Drittanbietern (oder Benutzerdefiniert). Der Hardwareanbieter bestimmt, in dem die Schattenkopie erstellt wird. VSS abstrahiert die Hardware-spezifischen Shadow Copy, damit die Anwendung sichern und Wiederherstellen die Schattenkopie ohne Informationen über die Hardware Implementierungsdetails zugreifen können. Die folgende Abbildung zeigt, wie die Anwendung sichern und Wiederherstellen von Exchange 2013 und Windows Server interagiert.
  
**Abbildung 1. Sicherung und Wiederherstellung Systemarchitektur**

![Diagramm, das zeigt, wie eine Sicherungs- und Wiederherstellungsanwendung interagiert. Zwischen Exchange Windows Server und der Clientanwendung gibt es eine bidirektionale Kommunikation. Der Windows-Server fungiert auch als Massenspeichergerät oder Sicherungsmedium.](media/VSS_architecture_E2k7.gif)
  
Die Sicherung und Wiederherstellung Anwendung fungiert als den VSS-anforderer. Die anfordernde Person kommuniziert mit VSS erhalten Sie Informationen zu Exchange 2013, um die Erstellung von Schattenkopien zu initiieren und den Zugriff auf die Daten für die Sicherung. 
  
Exchange-Speicher ist eine Komponente von Exchange 2013 und Exchange 2013-Datenbanken über das Windows Server File System zugreift. Dateisystem kann jeder Exchange-Server gleichzeitig bis zu 100 Datenbanken mit ihren zugehörigen Datenbankdateien (EDB), Transaktionsprotokolldateien und einer Prüfpunktdatei bereitstellen.
  
Zur Unterstützung der VSS enthält Exchange 2013 einen Exchange-Writer, der in der Exchange-Speicher integriert ist. Der Exchange-Writer in Koordination mit dem Exchange-Speicher (in Betrieb im Namen der anfordernden Person) fixieren und Bereitstellung der Datenbank aufzuheben, bevor sie Sie sichern, und klicken Sie dann zum aufzuheben und binden Sie die Datenbank nach der Sicherung ist abgeschlossen. Während einer Wiederherstellung weist die Anwendung sichern und Wiederherstellen den Exchange-Writer Koordination mit dem Exchange-Informationsspeicher, um die Bereitstellung der Datenbank aufzuheben, ersetzen Sie die Datenbankdateien, binden Sie die Datenbank, und klicken Sie dann die Transaktionsprotokolle einspielen, (nach Bedarf).
  
Während einer Wiederherstellung die anfordernden Person kommuniziert auch mit VSS zum Vorbereiten des Systems für die Wiederherstellung, und platzieren, um die Daten wieder auf das Massenspeichergerät. Die Sicherung und Wiederherstellung-Anwendung ist auch für die Arbeit mit Windows Server zum Lesen von Daten aus und Schreiben von Daten in die Sicherungskopie Speichermedium, gibt an, ob ein Band archivieren, ein Storage Area Network oder anderen Sicherungsmedium verantwortlich.
  
Die wiederhergestellte Datenbank kann entweder als regulären, aktive Datenbank oder als der Wiederherstellungsdatenbank Exchange 2013 bereitgestellt werden. Als Wiederherstellungsdatenbank auf jedem Exchange-Server kann nur eine eingebundene Datenbank festgelegt werden.
  
Informationen erforderlich, um erfolgreich ausführen von sicherungs- und Wiederherstellungsvorgängen mit Exchange 2013 VSS, und Ihre Anwendung sichern und Wiederherstellen als Teil der Exchange-Writer-Metadaten übertragen.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Arten von Sicherungsvorgängen für Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Wiederherstellen von Exchange 2013-Datenbanken](restoring-exchange-2013-databases.md)
    
- [Überprüfen der Integrität mithilfe der API für CHKSGFILES in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Überprüfen der Integrität mithilfe des Dienstprogramms Eseutil in Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Sicherung und Wiederherstellung für Exchange](backup-and-restore-for-exchange-2013.md) 
- [Referenz für die CChkSGFiles](cchksgfiles-class-reference.md) 
- 
  [Volumeschattenkopie-Dienst](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

