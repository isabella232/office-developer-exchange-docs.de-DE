---
title: Erste Schritte mit EWS-Clientanwendungen
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e6fd5c23-0ba5-4a7b-bdde-4a553447069f
description: Erstellen Sie Ihre erste Anwendung mithilfe von Exchange-Webdienste (EWS) in Exchange.
ms.openlocfilehash: 911495c74f4c74114a86b1a3a98c9200db338b34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756849"
---
# <a name="get-started-with-ews-client-applications"></a><span data-ttu-id="9e574-103">Erste Schritte mit EWS-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="9e574-103">Get started with EWS client applications</span></span>

<span data-ttu-id="9e574-104">Erstellen Sie Ihre erste Anwendung mithilfe von Exchange-Webdienste (EWS) in Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e574-104">Create your first application by using Exchange Web Services (EWS) in Exchange.</span></span>
  
<span data-ttu-id="9e574-p101">EWS ist ein umfassender Dienst, mit dem Anwendungen auf fast alle Informationen zugreifen können, die in einem Postfach unter Exchange Online, Exchange Online als Teil von Office 365 oder lokalen Versionen von Exchange gespeichert sind. EWS stellt den Zugriff auf Exchange-Server über standardmäßige Webprotokolle her. Bibliotheken wie die [verwaltete EWS-API](get-started-with-ews-managed-api-client-applications.md) enthalten die EWS-Vorgänge zum Bereitstellen einer objektorientierten Oberfläche. Nachdem Sie die Beispiele in diesem Artikel ausgeführt haben, verfügen Sie über ein grundlegendes Verständnis der Möglichkeiten von EWS.</span><span class="sxs-lookup"><span data-stu-id="9e574-p101">EWS is a comprehensive service that your applications can use to access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or Exchange on-premises mailbox. EWS uses standard web protocols to provide access to an Exchange server; libraries like the [EWS Managed API](get-started-with-ews-managed-api-client-applications.md) wrap the EWS operations to provide an object-oriented interface. After you've run the examples in this article, you will have a basic understanding of what you can do with EWS.</span></span> 
  
<span data-ttu-id="9e574-p102">Sie können EWS-Vorgänge unter jedem Betriebssystem und in jeder Sprache aufrufen, da die EWS-Anforderungen und -Antworten das SOAP-Protokoll verwenden. Die Beispiele in diesem Artikel sind in C# geschrieben und verwenden die .NET Framework-Objekte [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) und [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) ; die wichtigen Teile des Codes sind jedoch der XML-Code zum Durchführen der EWS-Anforderung und die vom Server zurückgegebene XML-Antwort. Die Codebeispiele konzentrieren sich auf die XML-Transaktionen, und nicht auf die Verarbeitung des XML-Codes.</span><span class="sxs-lookup"><span data-stu-id="9e574-p102">You can call EWS operations from any operating system or language, because the EWS requests and responses use the SOAP protocol. The examples in this article are written using C# and make use of the .NET Framework [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) and [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) objects; however, the important part of the code is the XML used to make the EWS request and the XML response returned from the server. The code examples emphasize the XML transactions and not processing the XML.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="9e574-111">Sie benötigen einen Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="9e574-111">You'll need an Exchange server</span></span>

<span data-ttu-id="9e574-p103">Wenn Sie bereits über ein Exchange-Postfachkonto verfügen, können Sie diesen Schritt überspringen. Andernfalls können Sie mit einer der folgenden Methoden ein Exchange-Postfach für Ihre erste EWS-Anwendung einrichten:</span><span class="sxs-lookup"><span data-stu-id="9e574-p103">If you already have an Exchange mailbox account, you can skip this step. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS application:</span></span>
  
- <span data-ttu-id="9e574-p104">[Besorgen Sie sich eine Office 365-Entwicklerwebsite ](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx)(empfohlen). Dies ist die schnellste Methode zum Erhalten eines Exchange-Postfachs.</span><span class="sxs-lookup"><span data-stu-id="9e574-p104">[Get an Office 365 Developer Site ](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx)(recommended). This is the quickest way for you to get an Exchange mailbox.</span></span>
    
- <span data-ttu-id="9e574-116">Laden Sie [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589) herunter.</span><span class="sxs-lookup"><span data-stu-id="9e574-116">Download [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>
    
<span data-ttu-id="9e574-p105">Nachdem Sie sichergestellt haben, dass Sie E-Mails von Ihrem Exchange-Server senden und empfangen können, sind Sie zum Einrichten der Entwicklungsumgebung bereit. Sie können Outlook Web App verwenden, um zu überprüfen, ob Sie E-Mails senden können.</span><span class="sxs-lookup"><span data-stu-id="9e574-p105">After you've verified that you can send and receive email from your Exchange server you are ready to set up your development environment. You can use Outlook Web App to verify that you can send email.</span></span>
  
<span data-ttu-id="9e574-p106">Sie müssen außerdem die URL des EWS-Endpunkts für Ihren Server kennen. Verwenden Sie in einer Produktionsumgebung die [AutoErmittlung](autodiscover-for-exchange.md) zur Ermittlung der EWS-URL. Die Beispiele in diesem Artikel verwenden die Office 365-EWS-Endpunkt-URL "https://outlook.office365.com/EWS/Exchange.asmx". Im Abschnitt [Nächste Schritte](#bk_next) finden Sie Links zu weiteren Informationen über die AutoErmittlung, wenn Sie bereit sind.</span><span class="sxs-lookup"><span data-stu-id="9e574-p106">You'll also need to know the URL of the EWS endpoint for your server. In a production application, you'd use [Autodiscover](autodiscover-for-exchange.md) to determine the EWS URL. The examples in this article use the Office 365 EWS endpoint URL, https://outlook.office365.com/EWS/Exchange.asmx. The [Next steps](#bk_next) section has links to more information about Autodiscover when you're ready.</span></span> 
  
<span data-ttu-id="9e574-123">Wenn Sie Ihre Anwendung mit einem Exchange-Server testen, der über das selbstsignierte Standardzertifikat verfügt, müssen Sie eine [Zertifikatüberprüfungsmethode](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) erstellen, die die Sicherheitsanforderungen Ihrer Organisation erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9e574-123">If you are testing your application using an Exchange server that has the default self-signed certificate, you'll need to create a [certificate validation method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) that meets the security requirements of your organization.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="9e574-124">Einrichten der Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="9e574-124">Set up your development environment</span></span>

<span data-ttu-id="9e574-p107">Welche Tools Sie zum Erstellen Ihrer ersten EWS-Anwendung verwenden, hängt vom Betriebssystem und von der Sprache ab, mit dem bzw. der Sie arbeiten; die Entscheidung ist hauptsächlich eine Frage der Vorliebe. Wenn Sie die C#-Beispiele in diesem Artikel nachvollziehen möchten, benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e574-p107">The tools that you use to create your first EWS application depend on the operating system and language that you use, and are mostly a matter of taste. If you want to follow along with the C# examples in this article, you'll need:</span></span> 
  
- <span data-ttu-id="9e574-127">Eine beliebige Version von Visual Studio, die .NET Framework 4.0 unterstützt</span><span class="sxs-lookup"><span data-stu-id="9e574-127">Any version of Visual Studio that supports the .NET Framework 4.0.</span></span> 
    
- <span data-ttu-id="9e574-p108">Eine Internetverbindung, über die der Entwicklungscomputer den Exchange-Server kontaktieren kann. Wenn Sie Outlook Web App verwenden und die Verbindung mit dem Exchange-Server über einen DNS-Namen statt über eine IP-Adresse herstellen, müssen Sie keine weiteren Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e574-p108">An Internet connection that your development machine can use to contact your Exchange server. If you can use Outlook Web App with a DNS name rather than an IP address to connect to your Exchange server, you are set up.</span></span>
    
## <a name="create-your-first-ews-application"></a><span data-ttu-id="9e574-130">Erstellen der ersten EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9e574-130">Create your first EWS application</span></span>

<span data-ttu-id="9e574-131">Die EWS-Anwendung, die Sie erstellen werden, zeigt zwei typische Szenarien für die Verwendung von EWS:</span><span class="sxs-lookup"><span data-stu-id="9e574-131">The EWS application that you will create shows two typical scenarios for using EWS:</span></span>
  
1. <span data-ttu-id="9e574-132">Abrufen von Informationen aus einem Exchange-Postfach und Anzeigen dieser Informationen für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="9e574-132">Get information from an Exchange mailbox and display that information to the user.</span></span>
    
2. <span data-ttu-id="9e574-133">Durchführen einer Aktion, z. B. Senden einer E-Mail, und Überprüfen der Antwort, um festzustellen, ob der Vorgang erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="9e574-133">Perform an action, such as sending an email, and check the response to see if the action succeeded.</span></span>
    
<span data-ttu-id="9e574-134">Lassen Sie uns beginnen.</span><span class="sxs-lookup"><span data-stu-id="9e574-134">Let's get started.</span></span>
  
### <a name="set-up-the-solution"></a><span data-ttu-id="9e574-135">Einrichten der Lösung</span><span class="sxs-lookup"><span data-stu-id="9e574-135">Set up the solution</span></span>

<span data-ttu-id="9e574-p109">Erstellen Sie zuerst eine neue Konsolenanwendungslösung unter Verwendung von Visual Studio. Wenn die Lösung bereit ist, erstellen Sie ein neues Objekt namens "Tracing.cs". Verwenden Sie dieses Objekt, um Informationen in die Konsole und in eine Protokolldatei zu schreiben, damit Sie die Ergebnisse überprüfen können, nachdem Sie den Code ausgeführt haben. Fügen Sie den folgenden Code in die Datei "Tracing.cs" ein.</span><span class="sxs-lookup"><span data-stu-id="9e574-p109">First, create a new console application solution using Visual Studio. When the solution is ready, create a new object called Tracing.cs. Use this object to write information to both the console and a log file so that you can review the results after you run your code. Paste the following code into the Tracing.cs file.</span></span>
  
```cs
using System;
using System.IO;
namespace Microsoft.Exchange.Samples.EWS
{
  class Tracing
  {
    private static TextWriter logFileWriter = null;
    public static void OpenLog(string fileName)
    {
      logFileWriter = new StreamWriter(fileName);
    }
    public static void Write(string format, params object[] args)
    {
      Console.Write(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.Write(format, args);
      }
    }
    public static void WriteLine(string format, params object[] args)
    {
      Console.WriteLine(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.WriteLine(format, args);
      }
    }
    public static void CloseLog()
    {
      logFileWriter.Flush();
      logFileWriter.Close();
    }
  }
}
```

<span data-ttu-id="9e574-p110">Öffnen Sie dann die Datei "Program.cs". Fügen Sie den restlichen Code für das Beispiel in diese Datei ein.</span><span class="sxs-lookup"><span data-stu-id="9e574-p110">Next, open the Program.cs file. You will put the rest of the code for the example in this file.</span></span>
  
<span data-ttu-id="9e574-p111">Richten Sie zuerst die Shell des Programms ein. Das Programm führt folgende Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="9e574-p111">First, set up the shell of the program. The program will:</span></span> 
  
1. <span data-ttu-id="9e574-144">Erstellen einer Protokolldatei, sodass die Anforderung und die Antwort für spätere Untersuchungen auf Datenträger geschrieben werden können</span><span class="sxs-lookup"><span data-stu-id="9e574-144">Create a log file so that the request and response can be written to disk for later study.</span></span>
    
2. <span data-ttu-id="9e574-145">Abrufen der E-Mail-Adresse und des Kennworts des Kontos, auf das Sie zugreifen</span><span class="sxs-lookup"><span data-stu-id="9e574-145">Get the email address and password of the account that you'll access.</span></span>
    
3. <span data-ttu-id="9e574-146">Aufrufen der Beispielmethoden</span><span class="sxs-lookup"><span data-stu-id="9e574-146">Call the sample methods.</span></span>
    
<span data-ttu-id="9e574-147">Ersetzen Sie die  `Main`-Methode in der Datei "Program.cs" durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="9e574-147">Replace the  `Main` method in the Program.cs with the following code.</span></span> 
  
```cs
    static void Main(string[] args)
    {
      // Start tracing to console and a log file.
      Tracing.OpenLog("./GetStartedWithEWS.log");
      Tracing.WriteLine("EWS sample application started.");
      var isValidEmailAddress = false;
      Console.Write("Enter an email address: ");
      var emailAddress = Console.ReadLine();
      
        isValidEmailAddress = (emailAddress.Contains("@") &amp;&amp; emailAddress.Contains("."));
      if (!isValidEmailAddress)
      {
        Tracing.WriteLine("Email address " + emailAddress + " is not a valid SMTP address. Closing program.");
        return;
      }
      SecureString password = GetPasswordFromConsole();
      if (password.Length == 0)
      {
        Tracing.WriteLine("Password empty, closing program.");
      }
      NetworkCredential userCredentials = new NetworkCredential(emailAddress, password);
      // These are the sample methods that demonstrate using EWS.
      // ShowNumberOfMessagesInInbox(userCredentials);
      // SendTestEmail(userCredentials);
     
      Tracing.WriteLine("EWS sample application ends.");
      Tracing.CloseLog();
      Console.WriteLine("Press enter to exit: ");
      Console.ReadLine();
    }
    // These method stubs will be filled in later.
    private static void ShowNumberOfMessagesInInbox(NetworkCredential userCredentials)
    {
    }
    private static void SendTestEmail(NetworkCredential userCredentials)
    {
    }
```

<span data-ttu-id="9e574-p112">Als Letztes müssen Sie die statische  `GetPasswordFromConsole`-Methode hinzufügen. Diese Methode gibt ein [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) -Objekt mit einem Kennwort zurück, das an der Konsole eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9e574-p112">The last thing that you need to do is add the  `GetPasswordFromConsole` static method. This method returns a [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) object that contains a password typed at the console.</span></span> 
  
```cs
    private static SecureString GetPasswordFromConsole()
    {
      SecureString password = new SecureString();
      bool readingPassword = true;
      Console.Write("Enter password: ");
      while (readingPassword)
      {
        ConsoleKeyInfo userInput = Console.ReadKey(true);
        switch (userInput.Key)
        {
          case (ConsoleKey.Enter):
            readingPassword = false;
            break;
          case (ConsoleKey.Escape):
            password.Clear();
            readingPassword = false;
            break;
          case (ConsoleKey.Backspace):
            if (password.Length > 0)
            {
              password.RemoveAt(password.Length - 1);
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
              Console.Write(" ");
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
            }
            break;
          default:
            if (userInput.KeyChar != 0)
            {
              password.AppendChar(userInput.KeyChar);
              Console.Write("*");
            }
            break;
        }
      }
      Console.WriteLine();
      password.MakeReadOnly();
      return password;
    }
```

### <a name="get-the-number-of-new-messages-in-an-inbox"></a><span data-ttu-id="9e574-150">Abrufen der Anzahl neuer Nachrichten im Posteingang</span><span class="sxs-lookup"><span data-stu-id="9e574-150">Get the number of new messages in an Inbox</span></span>

<span data-ttu-id="9e574-p113">Ein gängiger Vorgang in einer EWS-Anwendung ist das Abrufen von Informationen über E-Mail-Nachrichten, Termine, Besprechungen und die Ordner, in denen diese Elemente gespeichert sind. In diesem Beispiel wird die Anzahl der Nachrichten im Posteingang eines Kontos abgerufen; außerdem werden die Gesamtanzahl der Nachrichten und die Anzahl der ungelesenen Nachrichten angezeigt. Das Beispiel veranschaulicht die folgenden gängigen Aktionen für EWS-Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="9e574-p113">A common operation in an EWS application is to get information about email messages, appointments, meetings, and the folders that store them. This example gets the number of messages in an account's Inbox and displays the total number of messages and the number of unread messages. It demonstrates the following common actions for EWS applications:</span></span>
  
- <span data-ttu-id="9e574-154">Durchführen einer EWS-Anforderung an den Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="9e574-154">Making an EWS request to the Exchange server.</span></span>
    
- <span data-ttu-id="9e574-155">Analysieren der zurückgegebenen XML-Antwort im Hinblick auf die angeforderten Informationen</span><span class="sxs-lookup"><span data-stu-id="9e574-155">Parsing the returned XML response for the requested information.</span></span>
    
- <span data-ttu-id="9e574-156">Behandeln von allgemeinen Ausnahmen und Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="9e574-156">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="9e574-p114">Fügen Sie der  `ShowNumberOfMessagesInInbox`-Methode, die als Stub nach der main-Methode vorliegt, den folgenden Code hinzu. Wenn Sie die Anwendung ausführen, werden die Anzahl der Nachrichten im Posteingang des Kontos und die Anzahl der ungelesenen Nachrichten im Posteingang ausgegeben. Nachdem Sie die Anwendung ausgeführt haben, können Sie die Datei "GetStartedWithEWS.log" öffnen, um die XML-Anforderung anzuzeigen, die an den Exchange-Server gesendet wurde, sowie die vom Server zurückgegebene Antwort.</span><span class="sxs-lookup"><span data-stu-id="9e574-p114">Add the following code to the  `ShowNumberOfMessagesInInbox` method that was stubbed out after the main method. When you run the application, it will print the number of messages in the account's Inbox and the number of unread messages in the Inbox. After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span> 
  
```cs
      /// This is the XML request that is sent to the Exchange server.
      var getFolderSOAPRequest =
"<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
"<soap:Envelope xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
"   xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"<soap:Header>\n" +
"    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
"  </soap:Header>\n" +
"  <soap:Body>\n" +
"    <GetFolder xmlns=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
"               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"      <FolderShape>\n" +
"        <t:BaseShape>Default</t:BaseShape>\n" +
"      </FolderShape>\n" +
"      <FolderIds>\n" +
"        <t:DistinguishedFolderId Id=\"inbox\"/>\n" +
"      </FolderIds>\n" +
"    </GetFolder>\n" +
"  </soap:Body>\n" +
"</soap:Envelope>\n";
      // Write the get folder operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(getFolderSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(getFolderSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{http://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            // Process the response.
            IEnumerable<XElement> folders = from folderElement in
                                              responseEnvelope.Descendants
                                              ("{http://schemas.microsoft.com/exchange/services/2006/messages}Folders")
                                            select folderElement;
            foreach (var folder in folders)
            {
              Tracing.Write("Folder name:     ");
              var folderName = from folderElement in
                                 folder.Descendants
                                 ("{http://schemas.microsoft.com/exchange/services/2006/types}DisplayName")
                               select folderElement.Value;
              Tracing.WriteLine(folderName.ElementAt(0));
              Tracing.Write("Total messages:  ");
              var totalCount = from folderElement in
                                 folder.Descendants
                                   ("{http://schemas.microsoft.com/exchange/services/2006/types}TotalCount")
                               select folderElement.Value;
              Tracing.WriteLine(totalCount.ElementAt(0));
              Tracing.Write("Unread messages: ");
              var unreadCount = from folderElement in
                                 folder.Descendants
                                   ("{http://schemas.microsoft.com/exchange/services/2006/types}UnreadCount")
                               select folderElement.Value;
              Tracing.WriteLine(unreadCount.ElementAt(0));
            }
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }

```

### <a name="send-an-email-message"></a><span data-ttu-id="9e574-160">Senden einer E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9e574-160">Send an email message</span></span>

<span data-ttu-id="9e574-p115">Ein weiterer gängiger Vorgang für eine EWS-Anwendung ist das Senden von E-Mail-Nachrichten oder Besprechungsanfragen. Dieses Beispiel erstellt und sendet eine E-Mail-Nachricht unter Verwendung der zuvor eingegebenen Anmeldeinformationen. Die folgenden gängigen EWS-Anwendungsaufgaben werden veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="9e574-p115">Another common operation for an EWS application is to send email messages or meeting requests. This example creates and sends an email message using the user credentials that were entered earlier. It demonstrates these common EWS application tasks:</span></span>
  
- <span data-ttu-id="9e574-164">Erstellen und Senden einer E-Mail</span><span class="sxs-lookup"><span data-stu-id="9e574-164">Creating and sending an email.</span></span>
    
- <span data-ttu-id="9e574-165">Analysieren der zurückgegebenen XML-Antwort, um zu bestimmen, ob die E-Mail ordnungsgemäß gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="9e574-165">Parsing the returned XML response to determine if the email was correctly sent.</span></span>
    
- <span data-ttu-id="9e574-166">Behandeln von allgemeinen Ausnahmen und Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="9e574-166">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="9e574-p116">Fügen Sie der SendTestEmail-Methode, die als Stub nach der main-Methode vorliegt, den folgenden Code hinzu. Nachdem Sie die Anwendung ausgeführt haben, können Sie die Datei "GetStartedWithEWS.log" öffnen, um die XML-Anforderung anzuzeigen, die an den Exchange-Server gesendet wurde, sowie die vom Server zurückgegebene Antwort.</span><span class="sxs-lookup"><span data-stu-id="9e574-p116">Add the following code to the SendTestEmail method that was stubbed out after the main method. After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span>
  
```cs
var createItemSOAPRequest =
      "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
      "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" \n" +
      "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\" \n" +
      "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
      "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\">\n" +
      "  <soap:Header>\n" +
      "    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
      "  </soap:Header>\n" +
      "  <soap:Body>\n" +
      "    <m:CreateItem MessageDisposition=\"SendAndSaveCopy\">\n" +
      "      <m:SavedItemFolderId>\n" +
      "        <t:DistinguishedFolderId Id=\"sentitems\" />\n" +
      "      </m:SavedItemFolderId>\n" +
      "      <m:Items>\n" +
      "        <t:Message>\n" +
      "          <t:Subject>Company Soccer Team</t:Subject>\n" +
      "          <t:Body BodyType=\"HTML\">Are you interested in joining?</t:Body>\n" +
      "          <t:ToRecipients>\n" +
      "            <t:Mailbox>\n" +
      "              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>\n" +
      "              </t:Mailbox>\n" +
      "          </t:ToRecipients>\n" +
      "        </t:Message>\n" +
      "      </m:Items>\n" +
      "    </m:CreateItem>\n" +
      "  </soap:Body>\n" +
      "</soap:Envelope>\n";
      // Write the create item operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(createItemSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(createItemSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{http://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            Tracing.WriteLine("Message sent successfully.");
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }
```

<a name="bk_next"></a>

## <a name="next-steps"></a><span data-ttu-id="9e574-169">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9e574-169">Next steps</span></span>

<span data-ttu-id="9e574-p117">Nachdem Sie Ihre erste EWS-Anwendung geschrieben haben, können Sie weitere Möglichkeiten zum Verwenden von EWS erkunden. Hier sind einige Ideen für die ersten Schritte:</span><span class="sxs-lookup"><span data-stu-id="9e574-p117">Now that you've written your first EWS application, you're ready to discover other ways to use EWS. Here are some ideas to get you started:</span></span>
  
- <span data-ttu-id="9e574-p118">Implementieren Sie die [AutoErmittlung](autodiscover-for-exchange.md) in die Anwendung, sodass die Anwendung auf Basis der E-Mail-Adresse des Benutzer eine Verbindung mit dem richtigen Exchange-Server herstellt. Sehen Sie sich hierzu auch das Beispiel [Exchange 2013: Abrufen von Benutzereinstellungen mit AutoErmittlung](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) an.</span><span class="sxs-lookup"><span data-stu-id="9e574-p118">Implement [Autodiscover](autodiscover-for-exchange.md) in your application so that your application will connect to the correct Exchange server based on the user's email address. See also the [Exchange 2013: Get user settings with Autodiscover](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) sample.</span></span> 
    
- <span data-ttu-id="9e574-174">Holen Sie sich in der [EWS-Referenz](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) weitere Informationen über EWS.</span><span class="sxs-lookup"><span data-stu-id="9e574-174">Look at the [EWS reference](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) for more information about EWS.</span></span> 
    
- <span data-ttu-id="9e574-175">Unter [EWS-Vorgänge](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) finden Sie Informationen über die verfügbaren Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9e574-175">See the [EWS operations](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) for information about the operations that are available.</span></span> 
    
- <span data-ttu-id="9e574-176">Verwenden Sie den [EWS-Editor](http://ewseditor.codeplex.com/), um den SOAP-Datenverkehr anzuzeigen, der zum und vom Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e574-176">Use [EWS Editor](http://ewseditor.codeplex.com/) to see the SOAP traffic sent to and from the server.</span></span> 
    
<span data-ttu-id="9e574-177">Falls Probleme mit der Anwendung auftreten, [veröffentlichen Sie eine Frage oder einen Kommentar im Forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (und vergessen Sie nicht, den ersten Beitrag zu lesen).</span><span class="sxs-lookup"><span data-stu-id="9e574-177">If you run into any issues with your application, [try posting a question or comment in the forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (and don't forget to read the first post).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e574-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e574-178">See also</span></span>

- [<span data-ttu-id="9e574-179">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e574-179">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)   
- [<span data-ttu-id="9e574-180">Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e574-180">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [<span data-ttu-id="9e574-181">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="9e574-181">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="9e574-182">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="9e574-182">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)  
- [<span data-ttu-id="9e574-183">Erste Schritte mit verwalteten EWS-API-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="9e574-183">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)
    

