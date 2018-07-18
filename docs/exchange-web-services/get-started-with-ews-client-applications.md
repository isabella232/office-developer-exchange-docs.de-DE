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
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756849"
---
# <a name="get-started-with-ews-client-applications"></a>Erste Schritte mit EWS-Clientanwendungen

Erstellen Sie Ihre erste Anwendung mithilfe von Exchange-Webdienste (EWS) in Exchange.
  
EWS ist ein umfassender Dienst, mit dem Anwendungen auf fast alle Informationen zugreifen können, die in einem Postfach unter Exchange Online, Exchange Online als Teil von Office 365 oder lokalen Versionen von Exchange gespeichert sind. EWS stellt den Zugriff auf Exchange-Server über standardmäßige Webprotokolle her. Bibliotheken wie die [verwaltete EWS-API](get-started-with-ews-managed-api-client-applications.md) enthalten die EWS-Vorgänge zum Bereitstellen einer objektorientierten Oberfläche. Nachdem Sie die Beispiele in diesem Artikel ausgeführt haben, verfügen Sie über ein grundlegendes Verständnis der Möglichkeiten von EWS. 
  
Sie können EWS-Vorgänge unter jedem Betriebssystem und in jeder Sprache aufrufen, da die EWS-Anforderungen und -Antworten das SOAP-Protokoll verwenden. Die Beispiele in diesem Artikel sind in C# geschrieben und verwenden die .NET Framework-Objekte [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) und [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) ; die wichtigen Teile des Codes sind jedoch der XML-Code zum Durchführen der EWS-Anforderung und die vom Server zurückgegebene XML-Antwort. Die Codebeispiele konzentrieren sich auf die XML-Transaktionen, und nicht auf die Verarbeitung des XML-Codes. 
  
## <a name="youll-need-an-exchange-server"></a>Sie benötigen einen Exchange-Server

Wenn Sie bereits über ein Exchange-Postfachkonto verfügen, können Sie diesen Schritt überspringen. Andernfalls können Sie mit einer der folgenden Methoden ein Exchange-Postfach für Ihre erste EWS-Anwendung einrichten:
  
- [Besorgen Sie sich eine Office 365-Entwicklerwebsite ](http://msdn.microsoft.com/de-DE/library/office/fp179924.aspx)(empfohlen). Dies ist die schnellste Methode zum Erhalten eines Exchange-Postfachs.
    
- Laden Sie [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589) herunter.
    
Nachdem Sie sichergestellt haben, dass Sie E-Mails von Ihrem Exchange-Server senden und empfangen können, sind Sie zum Einrichten der Entwicklungsumgebung bereit. Sie können Outlook Web App verwenden, um zu überprüfen, ob Sie E-Mails senden können.
  
Sie müssen außerdem die URL des EWS-Endpunkts für Ihren Server kennen. Verwenden Sie in einer Produktionsumgebung die [AutoErmittlung](autodiscover-for-exchange.md) zur Ermittlung der EWS-URL. Die Beispiele in diesem Artikel verwenden die Office 365-EWS-Endpunkt-URL "https://outlook.office365.com/EWS/Exchange.asmx". Im Abschnitt [Nächste Schritte](#bk_next) finden Sie Links zu weiteren Informationen über die AutoErmittlung, wenn Sie bereit sind. 
  
Wenn Sie Ihre Anwendung mit einem Exchange-Server testen, der über das selbstsignierte Standardzertifikat verfügt, müssen Sie eine [Zertifikatüberprüfungsmethode](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) erstellen, die die Sicherheitsanforderungen Ihrer Organisation erfüllt. 
  
## <a name="set-up-your-development-environment"></a>Einrichten der Entwicklungsumgebung

Welche Tools Sie zum Erstellen Ihrer ersten EWS-Anwendung verwenden, hängt vom Betriebssystem und von der Sprache ab, mit dem bzw. der Sie arbeiten; die Entscheidung ist hauptsächlich eine Frage der Vorliebe. Wenn Sie die C#-Beispiele in diesem Artikel nachvollziehen möchten, benötigen Sie Folgendes: 
  
- Eine beliebige Version von Visual Studio, die .NET Framework 4.0 unterstützt 
    
- Eine Internetverbindung, über die der Entwicklungscomputer den Exchange-Server kontaktieren kann. Wenn Sie Outlook Web App verwenden und die Verbindung mit dem Exchange-Server über einen DNS-Namen statt über eine IP-Adresse herstellen, müssen Sie keine weiteren Schritte ausführen.
    
## <a name="create-your-first-ews-application"></a>Erstellen der ersten EWS-Anwendung

Die EWS-Anwendung, die Sie erstellen werden, zeigt zwei typische Szenarien für die Verwendung von EWS:
  
1. Abrufen von Informationen aus einem Exchange-Postfach und Anzeigen dieser Informationen für den Benutzer
    
2. Durchführen einer Aktion, z. B. Senden einer E-Mail, und Überprüfen der Antwort, um festzustellen, ob der Vorgang erfolgreich war
    
Lassen Sie uns beginnen.
  
### <a name="set-up-the-solution"></a>Einrichten der Lösung

Erstellen Sie zuerst eine neue Konsolenanwendungslösung unter Verwendung von Visual Studio. Wenn die Lösung bereit ist, erstellen Sie ein neues Objekt namens "Tracing.cs". Verwenden Sie dieses Objekt, um Informationen in die Konsole und in eine Protokolldatei zu schreiben, damit Sie die Ergebnisse überprüfen können, nachdem Sie den Code ausgeführt haben. Fügen Sie den folgenden Code in die Datei "Tracing.cs" ein.
  
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

Öffnen Sie dann die Datei "Program.cs". Fügen Sie den restlichen Code für das Beispiel in diese Datei ein.
  
Richten Sie zuerst die Shell des Programms ein. Das Programm führt folgende Aufgaben aus: 
  
1. Erstellen einer Protokolldatei, sodass die Anforderung und die Antwort für spätere Untersuchungen auf Datenträger geschrieben werden können
    
2. Abrufen der E-Mail-Adresse und des Kennworts des Kontos, auf das Sie zugreifen
    
3. Aufrufen der Beispielmethoden
    
Ersetzen Sie die  `Main`-Methode in der Datei "Program.cs" durch den folgenden Code. 
  
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

Als Letztes müssen Sie die statische  `GetPasswordFromConsole`-Methode hinzufügen. Diese Methode gibt ein [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) -Objekt mit einem Kennwort zurück, das an der Konsole eingegeben wurde. 
  
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

### <a name="get-the-number-of-new-messages-in-an-inbox"></a>Abrufen der Anzahl neuer Nachrichten im Posteingang

Ein gängiger Vorgang in einer EWS-Anwendung ist das Abrufen von Informationen über E-Mail-Nachrichten, Termine, Besprechungen und die Ordner, in denen diese Elemente gespeichert sind. In diesem Beispiel wird die Anzahl der Nachrichten im Posteingang eines Kontos abgerufen; außerdem werden die Gesamtanzahl der Nachrichten und die Anzahl der ungelesenen Nachrichten angezeigt. Das Beispiel veranschaulicht die folgenden gängigen Aktionen für EWS-Anwendungen:
  
- Durchführen einer EWS-Anforderung an den Exchange-Server
    
- Analysieren der zurückgegebenen XML-Antwort im Hinblick auf die angeforderten Informationen
    
- Behandeln von allgemeinen Ausnahmen und Fehlermeldungen
    
Fügen Sie der  `ShowNumberOfMessagesInInbox`-Methode, die als Stub nach der main-Methode vorliegt, den folgenden Code hinzu. Wenn Sie die Anwendung ausführen, werden die Anzahl der Nachrichten im Posteingang des Kontos und die Anzahl der ungelesenen Nachrichten im Posteingang ausgegeben. Nachdem Sie die Anwendung ausgeführt haben, können Sie die Datei "GetStartedWithEWS.log" öffnen, um die XML-Anforderung anzuzeigen, die an den Exchange-Server gesendet wurde, sowie die vom Server zurückgegebene Antwort. 
  
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

### <a name="send-an-email-message"></a>Senden einer E-Mail-Nachricht

Ein weiterer gängiger Vorgang für eine EWS-Anwendung ist das Senden von E-Mail-Nachrichten oder Besprechungsanfragen. Dieses Beispiel erstellt und sendet eine E-Mail-Nachricht unter Verwendung der zuvor eingegebenen Anmeldeinformationen. Die folgenden gängigen EWS-Anwendungsaufgaben werden veranschaulicht:
  
- Erstellen und Senden einer E-Mail
    
- Analysieren der zurückgegebenen XML-Antwort, um zu bestimmen, ob die E-Mail ordnungsgemäß gesendet wurde
    
- Behandeln von allgemeinen Ausnahmen und Fehlermeldungen
    
Fügen Sie der SendTestEmail-Methode, die als Stub nach der main-Methode vorliegt, den folgenden Code hinzu. Nachdem Sie die Anwendung ausgeführt haben, können Sie die Datei "GetStartedWithEWS.log" öffnen, um die XML-Anforderung anzuzeigen, die an den Exchange-Server gesendet wurde, sowie die vom Server zurückgegebene Antwort.
  
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

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Ihre erste EWS-Anwendung geschrieben haben, können Sie weitere Möglichkeiten zum Verwenden von EWS erkunden. Hier sind einige Ideen für die ersten Schritte:
  
- Implementieren Sie die [AutoErmittlung](autodiscover-for-exchange.md) in die Anwendung, sodass die Anwendung auf Basis der E-Mail-Adresse des Benutzer eine Verbindung mit dem richtigen Exchange-Server herstellt. Sehen Sie sich hierzu auch das Beispiel [Exchange 2013: Abrufen von Benutzereinstellungen mit AutoErmittlung](http://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) an. 
    
- Holen Sie sich in der [EWS-Referenz](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) weitere Informationen über EWS. 
    
- Unter [EWS-Vorgänge](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) finden Sie Informationen über die verfügbaren Vorgänge. 
    
- Verwenden Sie den [EWS-Editor](http://ewseditor.codeplex.com/), um den SOAP-Datenverkehr anzuzeigen, der zum und vom Server gesendet wird. 
    
Falls Probleme mit der Anwendung auftreten, [veröffentlichen Sie eine Frage oder einen Kommentar im Forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (und vergessen Sie nicht, den ersten Beitrag zu lesen). 
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)   
- [Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)  
- [Erste Schritte mit verwalteten EWS-API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md)
    

