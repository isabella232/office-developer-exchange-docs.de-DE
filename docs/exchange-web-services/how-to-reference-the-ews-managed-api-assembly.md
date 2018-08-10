---
title: Verweisen auf die EWS-verwaltete API-Assembly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: Informationen zum Verweisen auf die EWS-verwaltete API-Assembly.
ms.openlocfilehash: a08ce43d139440186f611049fa1e457ea44f0362
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353686"
---
# <a name="reference-the-ews-managed-api-assembly"></a>Verweisen auf die EWS-verwaltete API-Assembly

Informationen zum Verweisen auf die EWS-verwaltete API-Assembly.
  
Die EWS Managed API bietet eine einfache und umfassende Schnittstelle für die Entwicklung und Erweiterung von Anwendungen an, die Exchange-Webdienste (EWS) verwenden. Egal ob Sie zum Entwickeln Ihrer EWS Managed API-Anwendungen Visual Studio oder einen anderen Code-Editor verwenden, müssen Sie einen Verweis auf die Assembly-Webdienste erstellen. Wenn Sie die EWS Managed API noch nicht installiert haben, müssen Sie die [API herunterladen](http://aka.ms/ews-managed-api-readme).
  
> [!NOTE]
> Die verwaltete EWS-API steht nun als Ope -Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) zur Verfügung. Sie können die Open Source-Bibliothek für Folgendes verwenden: 
> - Implementieren von Programmfehlerbehebungen und Verbesserungen in die API 
> - Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind 
> - Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen
> 
>  Wir freuen uns über Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub. 
  
## <a name="referencing-the-assembly"></a>Verweisen auf die Assembly

Sie können einen Verweis am einfachsten mit Visual Studio erstellen. Wir sind uns dennoch bewusst, dass manche Entwickler andere Code-Editor bevorzugen. Deswegen stellen wir Anweisungen sowohl für den Befehlszeilencompiler als auch Visual Studio bereit. Ihnen ist sicherlich aufgefallen, dass in den beiden Beispielen unten dasselbe **using**-Argument verwendet wird. Der Unterschied zwischen den beiden Methoden ist, dass der Befehlszeilencompiler den Speicherort der Assemblydatei benötigt. In Visual Studio geschieht dies automatisch im Hintergrund. 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a>So fügen Sie mit Visual Studio einen Verweis hinzu:

1. Legen Sie die Dateien „Microsoft.Exchange.WebServices.dll" und „Microsoft.Exchange.WebServices.xml" in einem Ordner Ihrer Wahl ab. Standardmäßig liegen die Dateien im Ordner  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, aber Sie können die Dateien in einem beliebigem Speicherort auf Ihrem Computer abspeichern.
    
2. Klicken Sie im Bereich „Projektmappen-Explorer" in Visual Studio auf **Verweise** und klicken Sie dann auf **Verweis hinzufügen**. Damit öffnen Sie das Fenster „Verweis hinzufügen".
    
3. Rufen Sie nun die Registerkarte **Durchsuchen** auf, navigieren Sie zum Speicherort der Datei „Microsoft.Exchange.WebServices.dll", markieren Sie die Datei, und klicken Sie abschließend auf **OK**. 
    
4. Um die EWS Managed API in Ihrer Anwendung zu verwenden, fügen Sie dem **Microsoft.Exchange.WebServices.Data** -Namespace eine **using**-Anweisung hinzu. 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a>So fügen Sie einen Verweis mit dem Befehlszeilencompiler hinzu und erstellen Ihre Anwendung

1. Legen Sie die Datei „Microsoft.Exchange.WebServices.dll" in einem Ordner Ihrer Wahl ab. Dieser Ordner ist damit der Ausgabeordner für den Compiler.
    
2. Fügen Sie dem **Microsoft.Exchange.WebServices.Data** -Namespace in Ihrem Quellcode-Editor ein **using**-Argument hinzu. 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. Führen Sie den Befehlszeilencompiler aus, um ein Build Ihrer Anwendung zu erstellen. Der folgende Befehl nutzt .NET Framework C# zur Kompilierung der Windows-Anwendung, die in der Quellcodedatei „program.cs" angegeben wurde. Dabei wird davon ausgegangen, dass der Compiler im Standardinstallationsverzeichnis liegt und die Datei „Microsoft.Exchange.WebServices.dll" in einem Unterordner des „build"-Verzeichnisses.
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md)    
- [Einrichten der Umgebung der Exchange-Anwendungsentwicklung](setting-up-your-exchange-application-development-environment.md)   
- [Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

