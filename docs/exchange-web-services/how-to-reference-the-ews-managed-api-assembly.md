---
title: Verweisen auf die Assembly EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: Informationen zum Verweisen auf die EWS Managed API-Assembly.
ms.openlocfilehash: af7b1ec449c24e7fa4db89abb30e5ebc9f8d329e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756987"
---
# <a name="reference-the-ews-managed-api-assembly"></a><span data-ttu-id="eba5b-103">Verweisen auf die Assembly EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="eba5b-103">Reference the EWS Managed API assembly</span></span>

<span data-ttu-id="eba5b-104">Informationen zum Verweisen auf die EWS Managed API-Assembly.</span><span class="sxs-lookup"><span data-stu-id="eba5b-104">Find information about how to reference the EWS Managed API assembly.</span></span>
  
<span data-ttu-id="eba5b-p101">Die EWS Managed API bietet eine einfache und umfassende Schnittstelle für die Entwicklung und Erweiterung von Anwendungen an, die Exchange-Webdienste (EWS) verwenden. Egal ob Sie zum Entwickeln Ihrer EWS Managed API-Anwendungen Visual Studio oder einen anderen Code-Editor verwenden, müssen Sie einen Verweis auf die Assembly-Webdienste erstellen. Wenn Sie die EWS Managed API noch nicht installiert haben, müssen Sie die [API herunterladen](http://aka.ms/ews-managed-api-readme).</span><span class="sxs-lookup"><span data-stu-id="eba5b-p101">The EWS Managed API provides a simple and full-featured interface for developing and extending applications that use Exchange Web Services (EWS). Whether you are using Visual Studio or another code editor to develop your EWS Managed API application, you will need to make a reference to the EWS Managed API assembly. If you haven't installed the EWS Managed API already, be sure to [download the API](http://aka.ms/ews-managed-api-readme).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="eba5b-p102">[!HINWEIS]  Die EWS Managed API ist jetzt als Open Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) verfügbar. Sie können die Open Source-Bibliothek für Folgendes verwenden: >  Implementieren von Programmfehlerbehebungen und Verbesserungen der API >  Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind >  Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen >  Wir freuen uns auf Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub.</span><span class="sxs-lookup"><span data-stu-id="eba5b-p102">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api). You can use the open source library to: >  Contribute bug fixes and enhancements to the API. >  Get fixes and enhancements before they are available in an official release. >  Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms. >  We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="referencing-the-assembly"></a><span data-ttu-id="eba5b-113">Verweisen auf die Assembly</span><span class="sxs-lookup"><span data-stu-id="eba5b-113">Referencing the assembly</span></span>

<span data-ttu-id="eba5b-p103">Sie können einen Verweis am einfachsten mit Visual Studio erstellen. Wir sind uns dennoch bewusst, dass manche Entwickler andere Code-Editor bevorzugen. Deswegen stellen wir Anweisungen sowohl für den Befehlszeilencompiler als auch Visual Studio bereit. Ihnen ist sicherlich aufgefallen, dass in den beiden Beispielen unten dasselbe **using**-Argument verwendet wird. Der Unterschied zwischen den beiden Methoden ist, dass der Befehlszeilencompiler den Speicherort der Assemblydatei benötigt. In Visual Studio geschieht dies automatisch im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="eba5b-p103">The most common way to add a reference is to use Visual Studio. We know that some developers out there like to use other editors, so we are including instructions for using the command-line compiler as well as instructions for using Visual Studio. You might notice that the code examples that follow have the same **using** statements. The difference between the two methods is that the command-line compiler needs the location of the assembly file. The Visual Studio reference handles this for you behind the scenes.</span></span> 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a><span data-ttu-id="eba5b-119">So fügen Sie mit Visual Studio einen Verweis hinzu:</span><span class="sxs-lookup"><span data-stu-id="eba5b-119">To add a reference by using Visual Studio</span></span>

1. <span data-ttu-id="eba5b-p104">Legen Sie die Dateien „Microsoft.Exchange.WebServices.dll" und „Microsoft.Exchange.WebServices.xml" in einem Ordner Ihrer Wahl ab. Standardmäßig liegen die Dateien im Ordner  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, aber Sie können die Dateien in einem beliebigem Speicherort auf Ihrem Computer abspeichern.</span><span class="sxs-lookup"><span data-stu-id="eba5b-p104">Put the Microsoft.Exchange.WebServices.dll file and the Microsoft.Exchange.WebServices.xml file into a folder of your choice. By default, the files are installed in  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, but you can store the files anywhere on your computer.</span></span>
    
2. <span data-ttu-id="eba5b-p105">Klicken Sie im Bereich „Projektmappen-Explorer" in Visual Studio auf **Verweise** und klicken Sie dann auf **Verweis hinzufügen**. Damit öffnen Sie das Fenster „Verweis hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="eba5b-p105">In the Solution Explorer pane in Visual Studio, select **References**, and then choose **Add Reference**. This opens the Add Reference window.</span></span>
    
3. <span data-ttu-id="eba5b-124">Rufen Sie nun die Registerkarte **Durchsuchen** auf, navigieren Sie zum Speicherort der Datei „Microsoft.Exchange.WebServices.dll", markieren Sie die Datei, und klicken Sie abschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="eba5b-124">In the Add Reference window, navigate to the **Browse** tab, browse to the location of the Microsoft.Exchange.WebServices.dll file, select that file, and then select **OK**.</span></span> 
    
4. <span data-ttu-id="eba5b-125">Um die EWS Managed API in Ihrer Anwendung zu verwenden, fügen Sie dem **Microsoft.Exchange.WebServices.Data** -Namespace eine **using**-Anweisung hinzu.</span><span class="sxs-lookup"><span data-stu-id="eba5b-125">To use the EWS Managed API in your application, add a **using** statement for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a><span data-ttu-id="eba5b-126">So fügen Sie einen Verweis mit dem Befehlszeilencompiler hinzu und erstellen Ihre Anwendung</span><span class="sxs-lookup"><span data-stu-id="eba5b-126">To add a reference and build your application with the command-line compiler</span></span>

1. <span data-ttu-id="eba5b-p106">Legen Sie die Datei „Microsoft.Exchange.WebServices.dll" in einem Ordner Ihrer Wahl ab. Dieser Ordner ist damit der Ausgabeordner für den Compiler.</span><span class="sxs-lookup"><span data-stu-id="eba5b-p106">Put the Microsoft.Exchange.WebServices.dll file into a folder of your choice. This folder will be the output folder for the compiler.</span></span>
    
2. <span data-ttu-id="eba5b-129">Fügen Sie dem **Microsoft.Exchange.WebServices.Data** -Namespace in Ihrem Quellcode-Editor ein **using**-Argument hinzu.</span><span class="sxs-lookup"><span data-stu-id="eba5b-129">In your source code editor, add a **using** statement to the source code for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. <span data-ttu-id="eba5b-p107">Führen Sie den Befehlszeilencompiler aus, um ein Build Ihrer Anwendung zu erstellen. Der folgende Befehl nutzt .NET Framework C# zur Kompilierung der Windows-Anwendung, die in der Quellcodedatei „program.cs" angegeben wurde. Dabei wird davon ausgegangen, dass der Compiler im Standardinstallationsverzeichnis liegt und die Datei „Microsoft.Exchange.WebServices.dll" in einem Unterordner des „build"-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="eba5b-p107">Run the command-line compiler to build the application. The following command uses the .NET Framework C# compiler to build the Windows application defined in the source code file "program.cs". It assumes that the compiler is located in the default installation directory and that the Microsoft.Exchange.WebServices.dll file is in a subdirectory of the current directory named "build".</span></span>
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a><span data-ttu-id="eba5b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eba5b-133">See also</span></span>

- [<span data-ttu-id="eba5b-134">Erste Schritte mit verwalteten EWS-API-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="eba5b-134">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)    
- [<span data-ttu-id="eba5b-135">Einrichten der Entwicklungsumgebung für Exchange-Anwendung</span><span class="sxs-lookup"><span data-stu-id="eba5b-135">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="eba5b-136">Kommunizieren Sie mit Exchange-Webdienste mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="eba5b-136">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
