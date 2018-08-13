---
title: Erste Schritte mit verwalteten EWS-API-Clientanwendungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: Entwickeln Sie eine einfache „Hello World“-E-Mail-Clientanwendung für Exchange mithilfe der verwalteten EWS-API.
ms.openlocfilehash: b4254ab80b4dfc2c8fadf90c79d57517c3a0bb16
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353987"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a><span data-ttu-id="8c243-103">Erste Schritte mit verwalteten EWS-API-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="8c243-103">Get started with EWS Managed API client applications</span></span>

<span data-ttu-id="8c243-104">Entwickeln Sie eine einfache „Hello World“-E-Mail-Clientanwendung für Exchange mithilfe der verwalteten EWS-API.</span><span class="sxs-lookup"><span data-stu-id="8c243-104">Develop a simple Hello World email client application for Exchange by using the EWS Managed API.</span></span> 
  
<span data-ttu-id="8c243-p101">Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) bietet ein intuitives, benutzerfreundliches Objektmodell zum Senden und Empfangen von Webdienstnachrichten von Clientanwendungen, Portalanwendungen und Dienstanwendungen. Mithilfe der verwalteten EWS-API können Sie auf fast alle Informationen zugreifen, die in einem Postfach von Exchange Online, Exchange Online als Teil von Office 365 oder Exchange Server gespeichert sind. Die Informationen in diesem Artikel unterstützen Sie bei der Entwicklung Ihrer ersten Clientanwendung mit der verwalteten EWS-API.</span><span class="sxs-lookup"><span data-stu-id="8c243-p101">The [EWS Managed API](http://aka.ms/ews-managed-api-readme) provides an intuitive, easy-to-use object model for sending and receiving web service messages from client applications, portal applications, and service applications. You can access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or an Exchange server mailbox by using the EWS Managed API. You can use the information in this article to help you develop your first EWS Managed API client application.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8c243-108">Die verwaltete EWS-API steht nun als Open-Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8c243-108">The EWS Managed API is now available as an open source project on  GitHub http://aka.ms/ews-managed-api-github . You can use the open source library to:</span></span> <span data-ttu-id="8c243-109">Sie können die Open Source-Bibliothek für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="8c243-109">You can use the open source library to:</span></span> 
> - <span data-ttu-id="8c243-110">Implementieren von Programmfehlerbehebungen und Verbesserungen in die API</span><span class="sxs-lookup"><span data-stu-id="8c243-110">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="8c243-111">Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="8c243-111">Get fixes and enhancements before they are available in an official release.</span></span> 
> - <span data-ttu-id="8c243-112">Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen</span><span class="sxs-lookup"><span data-stu-id="8c243-112">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span> 
>
>  <span data-ttu-id="8c243-113">Wir freuen uns über Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub.</span><span class="sxs-lookup"><span data-stu-id="8c243-113">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="8c243-114">Sie benötigen einen Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="8c243-114">You'll need an Exchange server</span></span>
<span data-ttu-id="8c243-115"><a name="NeedExchange"> </a></span><span class="sxs-lookup"><span data-stu-id="8c243-115"></span></span>

<span data-ttu-id="8c243-p103">Wenn Sie bereits über ein Exchange-Postfachkonto verfügen, können Sie diesen Abschnitt überspringen. Andernfalls können Sie mit einer der folgenden Methoden ein Exchange-Postfach für Ihre erste EWS-Clientanwendung einrichten:</span><span class="sxs-lookup"><span data-stu-id="8c243-p103">If you already have an Exchange mailbox account, you can skip this section. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS client application:</span></span>
  
- <span data-ttu-id="8c243-p104">Besorgen Sie sich eine [Office 365-Entwicklerwebsite](http://msdn.microsoft.com/de-DE/library/office/fp179924.aspx) (empfohlen). Dies ist die schnellste Methode zum Einrichten eines Exchange-Postfachs.</span><span class="sxs-lookup"><span data-stu-id="8c243-p104">Get an [Office 365 Developer Site](http://msdn.microsoft.com/de-DE/library/office/fp179924.aspx) (recommended). This is the quickest way for you to set up an Exchange mailbox.</span></span> 
    
- <span data-ttu-id="8c243-120">Laden Sie [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589) herunter.</span><span class="sxs-lookup"><span data-stu-id="8c243-120">Download [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>
    
<span data-ttu-id="8c243-p105">Nachdem Sie überprüft haben, dass Sie E-Mails senden und von Exchange empfangen können, können Sie Ihre Entwicklungsumgebung einrichten. Zum Überprüfen des E-Mail-Versands können Sie den Exchange-Webclient [Outlook Web App](http://technet.microsoft.com/de-DE/library/jj657718%28v=exchg.150%29.aspx) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c243-p105">After you have verified that you can send and receive email from Exchange, you are ready to set up your development environment. You can use the Exchange web client [Outlook Web App](http://technet.microsoft.com/de-DE/library/jj657718%28v=exchg.150%29.aspx) to verify that you can send email.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="8c243-123">Einrichten der Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="8c243-123">Set up your development environment</span></span>
<span data-ttu-id="8c243-124"><a name="Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="8c243-124"></span></span>

<span data-ttu-id="8c243-125">Stellen Sie sicher, dass Sie auf Folgendes zugreifen können:</span><span class="sxs-lookup"><span data-stu-id="8c243-125">Make sure that you have access to the following:</span></span>
  
- <span data-ttu-id="8c243-p106">Eine beliebige Version von [Visual Studio](http://www.visualstudio.com/de-DE/downloads/download-visual-studio-vs.aspx), die .NET Framework 4 unterstützt. Zwar ist Visual Studio technisch gesehen nicht erforderlich, da Sie einen beliebigen C#-Compiler verwenden können, die Verwendung dieser Anwendung wird jedoch empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8c243-p106">Any version of [Visual Studio](http://www.visualstudio.com/de-DE/downloads/download-visual-studio-vs.aspx) that supports the .NET Framework 4. Although technically, you don't need Visual Studio because you can use any C# compiler, we recommend that you use it.</span></span> 
    
- <span data-ttu-id="8c243-p107">Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme). Abhängig von Ihrem System können Sie entweder die 64-Bit- oder die 32-Bit-Version verwenden. Übernehmen Sie den standardmäßigen Installationsspeicherort.</span><span class="sxs-lookup"><span data-stu-id="8c243-p107">The [EWS Managed API](http://aka.ms/ews-managed-api-readme). You can use either the 64-bit or 32-bit version, depending on your system. Use the default installation location.</span></span> 
    
## <a name="create-your-first-ews-managed-api-application"></a><span data-ttu-id="8c243-131">Erstellen Ihrer ersten Anwendung mit der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8c243-131">Create your first EWS Managed API application</span></span>
<span data-ttu-id="8c243-132"><a name="Create"> </a></span><span class="sxs-lookup"><span data-stu-id="8c243-132"></span></span>

<span data-ttu-id="8c243-p108">Diese Schritte setzen voraus, dass Sie eine Office 365-Entwicklerwebsite eingerichtet haben. Wenn Sie Exchange heruntergeladen und installiert haben, müssen Sie auf dem Exchange-Server [ein gültiges Zertifikat installieren](http://technet.microsoft.com/de-DE/library/bb310769%28v=exchg.141%29.aspx) oder einen Rückruf zur [Zertifikatsüberprüfung](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) für ein selbstsigniertes Zertifikat implementieren, das standardmäßig bereitgestellt wird. Beachten Sie außerdem, dass diese Schritte abhängig von der verwendeten Visual Studio-Version ggf. geringfügig variieren.</span><span class="sxs-lookup"><span data-stu-id="8c243-p108">These steps assume that you set up an Office 365 Developer Site. If you downloaded and installed Exchange, you will need to [install a valid certificate](http://technet.microsoft.com/de-DE/library/bb310769%28v=exchg.141%29.aspx) on your Exchange server or [implement a certificate validation](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) callback for a self-signed certificate that is provided by default. Also note that these steps might vary slightly depending on the version of Visual Studio that you are using.</span></span> 
  
### <a name="step-1-create-a-project-in-visual-studio"></a><span data-ttu-id="8c243-136">Schritt 1: Erstellen eines Projekts in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8c243-136">Step 1: Create a project in Visual Studio</span></span>

1. <span data-ttu-id="8c243-p109">Wählen Sie in Visual Studio im Menü **Datei** die Option **Neu**, und wählen Sie dann ** Projekt**. Das Dialogfeld **Neues Projekt** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8c243-p109">In Visual Studio, on the **File** menu, choose **New**, and then choose **Project**. The **New Project** dialog box opens.</span></span> 
    
2. <span data-ttu-id="8c243-p110">Erstellen Sie eine **C#-Konsolenanwendung**. Wählen Sie im Fensterbereich **Vorlagen** die Option **Visual C#**, und wählen Sie dann **Konsolenanwendung**.</span><span class="sxs-lookup"><span data-stu-id="8c243-p110">Create a **C# Console Application**. From the **Templates** pane, choose **Visual C#**, and then choose **Console Application**.</span></span> 
    
3. <span data-ttu-id="8c243-141">Nennen Sie das Projekt „HelloWorld", und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c243-141">Name the project HelloWorld, and then choose **OK**.</span></span>
    
<span data-ttu-id="8c243-142">Visual Studio erstellt das Projekt und öffnet das Fenster des Codedokuments „Program.cs“.</span><span class="sxs-lookup"><span data-stu-id="8c243-142">Visual Studio creates the project and opens the Program.cs code document window.</span></span>

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a><span data-ttu-id="8c243-143">Schritt 2: Hinzufügen eines Verweises auf die verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="8c243-143">Step 2: Add a reference to the EWS Managed API</span></span>

1. <span data-ttu-id="8c243-p111">Wenn der **Projektmappen-Explorer** bereits geöffnet ist, überspringen Sie diesen Schritt, und fahren Sie mit Schritt 2 fort. Um den **Projektmappen-Explorer** zu öffnen, wählen Sie im Menü **Ansicht** die Option **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="8c243-p111">If the **Solution Explorer** window is already open, skip this step and proceed to step 2. To open the **Solution Explorer** window, on the **View** menu, choose **Solution Explorer**.</span></span> 
    
2. <span data-ttu-id="8c243-p112">Öffnen Sie im **Projektmappen-Explorer** und im **HelloWorld** -Projekt das Kontextmenü (Rechtsklick) für **Verweise**, und wählen Sie **Verweis hinzufügen** aus dem Kontextmenü. Ein Dialogfeld für die Verwaltung von Projektverweisen wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8c243-p112">In the **Solution Explorer** and the **HelloWorld** project, open the shortcut menu (right-click) for **References** and choose **Add Reference** from the context menu. A dialog box for managing project references will open.</span></span> 
    
3. <span data-ttu-id="8c243-p113">Wählen Sie die Option **Durchsuchen**. Navigieren Sie zu dem Speicherort, an dem Sie die DLL-Datei der verwalteten EWS-API installiert haben. Vom Installationsprogramm wird der folgende Standardpfad festgelegt: C:\Programme\Microsoft\Exchange\Web Services\<Version>\. Der Pfad variiert abhängig davon, ob Sie die 32- oder die 64-Bit-Version der Datei „Microsoft.Exchange.WebServices.dll" herunterladen. Wählen Sie **Microsoft.Exchange.WebServices.dll** und dann **OK** oder **Hinzufügen**. Hierdurch wird der Verweis auf die verwaltete EWS-API Ihrem Projekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8c243-p113">Choose the **Browse** option. Browse to the location where you installed the EWS Managed API DLL. The default path set by the installer is the following: C:\Program Files\Microsoft\Exchange\Web Services\<version>\. The path can vary based on whether you download the 32 or 64 bit version of the Microsoft.Exchange.WebServices.dll. Choose **Microsoft.Exchange.WebServices.dll** and select **OK** or **Add**. This adds the EWS Managed API reference to your project.</span></span> 
    
4. <span data-ttu-id="8c243-p114">Wenn Sie Verwaltete EWS-API 2.0 verwenden, ändern Sie das Ziel des HelloWorld-Projekts in .NET Framework 4. Andere Versionen der verwalteten EWS-API verwenden möglicherweise eine andere Zielversion von .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8c243-p114">If you are using EWS Managed API 2.0, change the HelloWorld project to target the .NET Framework 4. Other versions of the EWS Managed API might use a different target version of the .NET Framework.</span></span>
    
5. <span data-ttu-id="8c243-p115">Vergewissern Sie sich, dass Sie die richtige Zielversion von .NET Framework verwenden. Öffnen Sie das Kontextmenü (Rechtsklick) für Ihr **HelloWorld** -Projekt im **Projektmappen-Explorer**, und wählen Sie **Eigenschaften**. Überprüfen Sie, ob **.NET Framework 4** im Dropdown-Listenfeld **Zielframework** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="8c243-p115">Confirm that you are using the correct target version of the .NET Framework. Open the shortcut menu (right-click) for your **HelloWorld** project in the **Solution Explorer**, and choose **Properties**. Verify that the **.NET Framework 4** is selected in the **Target framework** drop-down box.</span></span> 
    
<span data-ttu-id="8c243-159">Nachdem Sie Ihr Projekt eingerichtet und einen Verweis auf die verwaltete EWS-API erstellt haben, können Sie Ihre erste Anwendung erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c243-159">Now that you have your project set up and you created a reference to the EWS Managed API, you are ready to create your first application.</span></span> <span data-ttu-id="8c243-160">Fügen Sie der Einfachheit halber Ihren Code zur Datei „Program.cs“ hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c243-160">To keep things simple, add your code to the Program.cs file.</span></span> <span data-ttu-id="8c243-161">Weitere Informationen über das Verweisen auf die verwaltete EWS-API finden Sie unter [ Verweisen auf die EWS-verwaltete API-Assembly](how-to-reference-the-ews-managed-api-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="8c243-161">Read [How to: Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md) for more information about referencing the EWS Managed API.</span></span> <span data-ttu-id="8c243-162">Im nächsten Schritt werden Sie den grundlegenden Code zum Schreiben der meisten EWS-verwalteten API-Clientanwendungen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="8c243-162">In the next step, you will develop the basic code to write most EWS Managed API client applications.</span></span> 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a><span data-ttu-id="8c243-163">Schritt 3: Einrichten der Überprüfung der URL-Umleitung für die AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="8c243-163">Step 3: Set up URL redirection validation for Autodiscover</span></span>

- <span data-ttu-id="8c243-p117">Fügen Sie die folgende Rückrufmethode zur Umleitungsüberprüfung nach der **Main(string[] args)** -Methode hinzu. Hierdurch wird überprüft, ob die umgeleiteten URLs, die von der [AutoErmittlung](autodiscover-for-exchange.md) zurückgegeben werden, einen HTTPS-Endpunkt darstellen.</span><span class="sxs-lookup"><span data-stu-id="8c243-p117">Add the following redirection validation callback method after the **Main(string[] args)** method. This validates whether redirected URLs returned by [Autodiscover](autodiscover-for-exchange.md) represent an HTTPS endpoint.</span></span> 
    
  ```cs
  private static bool RedirectionUrlValidationCallback(string redirectionUrl)
  {
     // The default for the validation callback is to reject the URL.
     bool result = false;
     Uri redirectionUri = new Uri(redirectionUrl);
     // Validate the contents of the redirection URL. In this simple validation
     // callback, the redirection URL is considered valid if it is using HTTPS
     // to encrypt the authentication credentials. 
     if (redirectionUri.Scheme == "https")
     {
        result = true;
     }
     return result;
  }
  ```

<span data-ttu-id="8c243-p118">Dieser Überprüfungsrückruf wird in Schritt 4 an das **ExchangeService** -Objekt übergeben. Sie benötigen ihn, damit Ihre Anwendung Umleitungen der AutoErmittlung vertraut und diesen folgt - die Ergebnisse der AutoErmittlungsumleitung stellen den EWS-Endpunkt für unsere Anwendung dar.</span><span class="sxs-lookup"><span data-stu-id="8c243-p118">This validation callback will be passed to the **ExchangeService** object in step 4. You need this so that your application will trust and follow Autodiscover redirects - the results of the Autodiscover redirect provides the EWS endpoint for our application.</span></span> 

### <a name="step-4-prepare-the-exchangeservice-object"></a><span data-ttu-id="8c243-168">Schritt 4: Vorbereiten des ExchangeService-Objekts</span><span class="sxs-lookup"><span data-stu-id="8c243-168">Step 4: Prepare the ExchangeService object</span></span>

1. <span data-ttu-id="8c243-p119">Fügen Sie der verwalteten EWS-API einen Verweis auf die **using**-Direktive hinzu. Fügen Sie den folgenden Code nach der letzten **using**-Direktive am Anfang der Datei „Program.cs" ein.</span><span class="sxs-lookup"><span data-stu-id="8c243-p119">Add a **using** directive reference to the EWS Managed API. Add the following code after the last **using** directive at the top of Program.cs.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. <span data-ttu-id="8c243-p120">Instanziieren Sie in der **Main** -Methode das [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt mit der gewünschten Dienstzielversion. Dieses Beispiel hat die früheste Version des EWS-Schemas als Ziel.</span><span class="sxs-lookup"><span data-stu-id="8c243-p120">In the **Main** method, instantiate the [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object with the service version you intend to target. This example targets the earliest version of the EWS schema.</span></span> 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. <span data-ttu-id="8c243-p121">Wenn Sie einen lokalen Exchange-Server als Ziel verwenden und Ihr Client der Domäne beigetreten ist, fahren Sie mit Schritt 4 fort. Wenn das Ziel Ihres Clients ein Postfach von Exchange Online oder einer Office 365-Entwicklerwebsite ist, müssen Sie explizite Anmeldeinformationen übergeben. Fügen Sie nach der Instanziierung des **ExchangeService** -Objekts den folgenden Code hinzu, und legen Sie die Anmeldeinformationen für das Postfachkonto fest. Der Benutzername muss der Benutzerprinzipalname sein. Fahren Sie mit Schritt 5 fort.</span><span class="sxs-lookup"><span data-stu-id="8c243-p121">If you are targeting an on-premises Exchange server and your client is domain joined, proceed to step 4. If you client is targeting an Exchange Online or Office 365 Developer Site mailbox, you have to pass explicit credentials. Add the following code after the instantiation of the **ExchangeService** object and set the credentials for your mailbox account. The user name should be the user principal name. Proceed to step 5.</span></span> 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. <span data-ttu-id="8c243-p122">Der Domäne beigetretene Clients mit einem lokalen Exchange-Server als Ziel können die standardmäßigen Anmeldeinformationen des angemeldeten Benutzers verwenden, vorausgesetzt, die Anmeldeinformationen sind einem Postfach zugeordnet. Fügen Sie nach der Instanziierung des **ExchangeService** -Objekts den folgenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c243-p122">Domain-joined clients that target an on-premises Exchange server can use the default credentials of the user who is logged on, assuming the credentials are associated with a mailbox. Add the following code after the instantiation of the **ExchangeService** object.</span></span> 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   <span data-ttu-id="8c243-p123">Wenn das Ziel Ihres Clients ein Postfach von Exchange Online oder einer Office 365-Entwicklerwebsite ist, überprüfen Sie, ob [UseDefaultCredentials](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) auf **false** (den Standardwert) festgelegt ist. Der Client kann nun den ersten Aufruf an den AutoErmittlungsdienst durchführen, um die Dienst-URL für Aufrufe an den EWS-Dienst abzurufen. .</span><span class="sxs-lookup"><span data-stu-id="8c243-p123">If your client targets an Exchange Online or Office 365 Developer Site mailbox, verify that [UseDefaultCredentials](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) is set to **false**, which is the default value. Your client is ready to make the first call to the Autodiscover service to get the service URL for calls to the EWS service.</span></span>
    
5. <span data-ttu-id="8c243-p124">Die **AutodiscoverUrl** -Methode für das **ExchangeService** -Objekt führt eine Reihe von Aufrufen an den AutoErmittlungsdienst durch, um die Dienst-URL abzurufen. Wenn dieser Methodenaufruf erfolgreich ist, wird die URL-Eigenschaft des **ExchangeService** -Objekts auf die Dienst-URL festgelegt. Übergeben Sie die E-Mail-Adresse des Benutzers und den **RedirectionUrlValidationCallback** an die **AutodiscoverUrl** -Methode. Fügen Sie den folgenden Code nach den in Schritt 3 oder 4 angegebenen Anmeldeinformationen hinzu. Ändern Sie  `user1@contoso.com` in Ihre E-Mail-Adresse, sodass der AutoErmittlungsdienst Ihren EWS-Endpunkt findet.</span><span class="sxs-lookup"><span data-stu-id="8c243-p124">The **AutodiscoverUrl** method on the **ExchangeService** object performs a series of calls to the Autodiscover service to get the service URL. If this method call is successful, the URL property on the **ExchangeService** object will be set with the service URL. Pass the user's email address and the **RedirectionUrlValidationCallback** to the **AutodiscoverUrl** method. Add the following code after the credentials have been specified in step 3 or 4. Change  `user1@contoso.com` to your email address so that the Autodiscover service finds your EWS endpoint.</span></span> 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

<span data-ttu-id="8c243-187">Ihr Client ist derzeit so eingerichtet, dass er zum Zugreifen auf Postfachdaten Aufrufe von EWS vornimmt.</span><span class="sxs-lookup"><span data-stu-id="8c243-187">At this point, your client is set up to make calls to EWS to access mailbox data.</span></span> <span data-ttu-id="8c243-188">Wenn Sie den Code jetzt ausführen, können Sie die Funktion des **AutodiscoverUrl** -Methodenaufrufs prüfen, indem Sie den Inhalt der [ExchangeService.Url](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="8c243-188">If you run your code now, you can verify that the **AutodiscoverUrl** method call worked by examining the contents of the [ExchangeService.Url](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="8c243-189">Wenn diese Eigenschaft eine URL enthält, war Ihr Aufruf erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8c243-189">If this property contains a URL, your call was a success!</span></span> <span data-ttu-id="8c243-190">Dies bedeutet, dass sich Ihre Anwendung erfolgreich beim Dienst authentifiziert und den EWS-Endpunkt für Ihr Postfach ermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="8c243-190">This means that your application successfully authenticated with the service and discovered the EWS endpoint for your mailbox.</span></span> <span data-ttu-id="8c243-191">Sie können nun Ihre ersten Aufrufe von EWS vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8c243-191">Now you are ready to make your first calls to EWS.</span></span> <span data-ttu-id="8c243-192">Weitere Informationen über das Festlegen der EWS-URL finden Sie unter [Festlegen der EWS-Dienst-URL mithilfe der verwalteten EWS-API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="8c243-192">Read [How to: Set the EWS service URL by using the EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) for more information about setting the EWS URL.</span></span> 

### <a name="step-6-create-your-first-hello-world-email-message"></a><span data-ttu-id="8c243-193">Schritt 6: Erstellen Ihrer ersten „Hello World“-E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8c243-193">Step 6: Create your first Hello World email message</span></span>

1. <span data-ttu-id="8c243-194">Instanziieren Sie nach dem **AutodiscoverUrl** -Methodenaufruf ein neues **EmailMessage** -Objekt, und übergeben Sie das erstellte Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="8c243-194">After the **AutodiscoverUrl** method call, instantiate a new **EmailMessage** object and pass in the service object you created.</span></span> 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   <span data-ttu-id="8c243-p126">Sie verfügen jetzt über eine E-Mail-Nachricht, für die die Dienstbindung festgelegt ist. Alle für das **EmailMessage** -Objekt initiierten Aufrufe haben den Dienst als Ziel.</span><span class="sxs-lookup"><span data-stu-id="8c243-p126">You now have an email message on which the service binding is set. Any calls initiated on the **EmailMessage** object will be targeted at the service.</span></span> 
    
2. <span data-ttu-id="8c243-p127">Legen Sie nun den Empfänger für die Zeile „An" der E-Mail-Nachricht fest. Ändern Sie hierzu  `user1@contoso.com` so, dass Ihre SMTP-Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c243-p127">Now set the To: line recipient of the email message. To do this, change  `user1@contoso.com` to use your SMTP address.</span></span> 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. <span data-ttu-id="8c243-199">Legen Sie den Betreff und den Text der E-Mail-Nachricht fest.</span><span class="sxs-lookup"><span data-stu-id="8c243-199">Set the subject and the body of the email message.</span></span>
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. <span data-ttu-id="8c243-200">Sie können nun Ihre erste E-Mail-Nachricht mit der verwalteten EWS-API senden.</span><span class="sxs-lookup"><span data-stu-id="8c243-200">You are now ready to send your first email message by using the EWS Managed API.</span></span> <span data-ttu-id="8c243-201">Die **Send**-Methode ruft den Dienst auf und übermittelt die E-Mail-Nachricht zur Zustellung.</span><span class="sxs-lookup"><span data-stu-id="8c243-201">The **Send** method will call the service and submit the email message for delivery.</span></span> <span data-ttu-id="8c243-202">Informationen zu anderen Methoden, die Sie zur Kommunikation mit Exchange verwenden können, finden Sie unter [Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="8c243-202">Read [How to: Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) to learn about other methods you can use to communicate with Exchange.</span></span> 
    
   ```cs
    email.Send();
   ```

5. <span data-ttu-id="8c243-p129">Sie können die „Hello World"-Anwendung jetzt ausführen. Drücken Sie in Visual Studio **F5**. Ein leeres Konsolenfenster wird geöffnet. Im Konsolenfenster wird nichts angezeigt, während Ihre Anwendung die Authentifizierung durchführt, Umleitungen der AutoErmittlung folgt und anschließend den ersten Aufruf ausführt, um eine E-Mail-Nachricht zu erstellen, die Sie an sich selbst senden. Wenn die durchgeführten Aufrufe angezeigt werden sollen, fügen Sie vor dem Aufruf der **AutodiscoverUrl** -Methode die folgenden zwei Codezeilen hinzu. Drücken Sie dann F5. Hierdurch wird die [Ablaufverfolgung der EWS-Anforderungen und -Antworten](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) im Konsolenfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c243-p129">You are ready to run your Hello World application. In Visual Studio, select **F5**. A blank console window will open. You will not see anything in the console window while your application authenticates, follows Autodiscover redirections, and then makes its first call to create an email message that you send to yourself. If you want to see the calls being made, add the following two lines of code before the **AutodiscoverUrl** method is called. Then press F5. This will [trace out the EWS requests and responses](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) to the console window.</span></span> 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

<span data-ttu-id="8c243-p130">Sie verfügen jetzt über eine funktionsfähige verwaltete EWS-API-Clientanwendung. Der Einfachheit halber zeigt das folgende Beispiel den gesamten Code, den Sie zum Erstellen Ihrer „Hello World“-Anwendung zur Datei „Program.cs“ hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="8c243-p130">You now have a working EWS Managed API client application. For your convenience, the following example shows all the code that you added to Program.cs to create your Hello World application.</span></span>

```cs
using System;
using Microsoft.Exchange.WebServices.Data;
namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
      service.Credentials = new WebCredentials("user1@contoso.com", "password");
      service.TraceEnabled = true;
      service.TraceFlags = TraceFlags.All;
      service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
      EmailMessage email = new EmailMessage(service);
      email.ToRecipients.Add("user1@contoso.com");
      email.Subject = "HelloWorld";
      email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API");
      email.Send();
    }
    private static bool RedirectionUrlValidationCallback(string redirectionUrl)
    {
      // The default for the validation callback is to reject the URL.
      bool result = false;
      Uri redirectionUri = new Uri(redirectionUrl);
      // Validate the contents of the redirection URL. In this simple validation
      // callback, the redirection URL is considered valid if it is using HTTPS
      // to encrypt the authentication credentials. 
      if (redirectionUri.Scheme == "https")
      {
        result = true;
      }
      return result;
    }
  }
}
```

## <a name="next-steps"></a><span data-ttu-id="8c243-212">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8c243-212">Next steps</span></span>
<span data-ttu-id="8c243-213"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="8c243-213"></span></span>

<span data-ttu-id="8c243-214">Wenn Sie weitere Aktionen mit Ihrer ersten verwalteten EWS-API-Clientanwendung ausführen möchten, erkunden Sie das folgende Informationsmaterial:</span><span class="sxs-lookup"><span data-stu-id="8c243-214">If you're ready to do more with your first EWS Managed API client application, explore the following resources:</span></span>
  
- [<span data-ttu-id="8c243-215">Exchange 2013: 101-Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="8c243-215">Exchange 2013: 101 code samples</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)   
- [<span data-ttu-id="8c243-216">Ordner und Elemente</span><span class="sxs-lookup"><span data-stu-id="8c243-216">Folders and items</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="8c243-217">EWSEditor</span><span class="sxs-lookup"><span data-stu-id="8c243-217">EWSEditor</span></span>](http://ewseditor.codeplex.com/)
    
<span data-ttu-id="8c243-218">Falls Probleme mit der Anwendung auftreten, [veröffentlichen Sie eine Frage oder einen Kommentar im Forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (und vergessen Sie nicht, den aktuellsten Beitrag zu lesen).</span><span class="sxs-lookup"><span data-stu-id="8c243-218">If you run into any issues with your application, [try posting a question or comment in the forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (and don't forget to read the top post).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8c243-219">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="8c243-219">In this section</span></span>
<span data-ttu-id="8c243-220"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="8c243-220"></span></span>

- [<span data-ttu-id="8c243-221">Verweisen auf die EWS-verwaltete API-Assembly</span><span class="sxs-lookup"><span data-stu-id="8c243-221">How to: Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)   
- [<span data-ttu-id="8c243-222">Festlegen der EWS-Dienst-URL mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8c243-222">How to: Set the EWS service URL by using the EWS Managed API</span></span>](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)   
- [<span data-ttu-id="8c243-223">Kommunizieren mit EWS unter Verwendung der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8c243-223">How to: Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a><span data-ttu-id="8c243-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c243-224">See also</span></span>

- [<span data-ttu-id="8c243-225">Verwenden von Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="8c243-225">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)    
- [<span data-ttu-id="8c243-226">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="8c243-226">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)    
- [<span data-ttu-id="8c243-227">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="8c243-227">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)   
- [<span data-ttu-id="8c243-228">Ablaufverfolgungsanforderungen und -antworten zur Problembehandlung bei EWS-verwalteten API-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8c243-228">How to: Trace requests and responses to troubleshoot EWS Managed API applications</span></span>](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

