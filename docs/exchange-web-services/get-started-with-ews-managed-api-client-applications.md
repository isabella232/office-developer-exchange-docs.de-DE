---
title: Erste Schritte mit verwalteten EWS-API-Clientanwendungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: Entwickeln Sie eine einfache „Hello World-E-Mail-Clientanwendung für Exchange mithilfe der verwalteten EWS-API.
ms.openlocfilehash: dafc8cbbf172ad725ab83c93553464ba96ef33b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756852"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a>Erste Schritte mit verwalteten EWS-API-Clientanwendungen

Entwickeln Sie eine einfache „Hello World"-E-Mail-Clientanwendung für Exchange mithilfe der verwalteten EWS-API. 
  
Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme) bietet ein intuitives, benutzerfreundliches Objektmodell zum Senden und Empfangen von Webdienstnachrichten von Clientanwendungen, Portalanwendungen und Dienstanwendungen. Mithilfe der verwalteten EWS-API können Sie auf fast alle Informationen zugreifen, die in einem Postfach von Exchange Online, Exchange Online als Teil von Office 365 oder Exchange Server gespeichert sind. Die Informationen in diesem Artikel unterstützen Sie bei der Entwicklung Ihrer ersten Clientanwendung mit der verwalteten EWS-API. 
  
> [!NOTE]
> [!HINWEIS]  Die verwaltete EWS-API ist jetzt als Open Source-Projekt auf [GitHub](https://github.com/officedev/ews-managed-api) verfügbar. Sie können die Open Source-Bibliothek für Folgendes verwenden: >  Implementieren von Programmfehlerbehebungen und Verbesserungen in die API >  Abrufen von Fehlerbehebungen und Verbesserungen, bevor diese in einer offiziellen Version verfügbar sind >  Zugreifen auf die umfassendste und aktuellste Implementierung der API, um sie als Referenz zu verwenden oder neue Bibliotheken auf neuen Plattformen zu erstellen >  Wir freuen uns auf Ihre [Beiträge](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) über GitHub. 
  
## <a name="youll-need-an-exchange-server"></a>Sie benötigen einen Exchange-Server
<a name="NeedExchange"> </a>

Wenn Sie bereits über ein Exchange-Postfachkonto verfügen, können Sie diesen Abschnitt überspringen. Andernfalls können Sie mit einer der folgenden Methoden ein Exchange-Postfach für Ihre erste EWS-Clientanwendung einrichten:
  
- Besorgen Sie sich eine [Office 365-Entwicklerwebsite](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx) (empfohlen). Dies ist die schnellste Methode zum Einrichten eines Exchange-Postfachs. 
    
- Laden Sie [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589) herunter.
    
Nachdem Sie überprüft haben, dass Sie E-Mails senden und von Exchange empfangen können, können Sie Ihre Entwicklungsumgebung einrichten. Zum Überprüfen des E-Mail-Versands können Sie den Exchange-Webclient [Outlook Web App](http://technet.microsoft.com/en-us/library/jj657718%28v=exchg.150%29.aspx) verwenden. 
  
## <a name="set-up-your-development-environment"></a>Einrichten der Entwicklungsumgebung
<a name="Setup"> </a>

Stellen Sie sicher, dass Sie auf Folgendes zugreifen können:
  
- Eine beliebige Version von [Visual Studio](http://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx), die .NET Framework 4 unterstützt. Zwar ist Visual Studio technisch gesehen nicht erforderlich, da Sie einen beliebigen C#-Compiler verwenden können, die Verwendung dieser Anwendung wird jedoch empfohlen. 
    
- Die [verwaltete EWS-API](http://aka.ms/ews-managed-api-readme). Abhängig von Ihrem System können Sie entweder die 64-Bit- oder die 32-Bit-Version verwenden. Übernehmen Sie den standardmäßigen Installationsspeicherort. 
    
## <a name="create-your-first-ews-managed-api-application"></a>Erstellen Ihrer ersten Anwendung mit der verwalteten EWS-API
<a name="Create"> </a>

Diese Schritte setzen voraus, dass Sie eine Office 365-Entwicklerwebsite eingerichtet haben. Wenn Sie Exchange heruntergeladen und installiert haben, müssen Sie auf dem Exchange-Server [ein gültiges Zertifikat installieren](http://technet.microsoft.com/en-us/library/bb310769%28v=exchg.141%29.aspx) oder einen Rückruf zur [Zertifikatsüberprüfung](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) für ein selbstsigniertes Zertifikat implementieren, das standardmäßig bereitgestellt wird. Beachten Sie außerdem, dass diese Schritte abhängig von der verwendeten Visual Studio-Version ggf. geringfügig variieren. 
  
### <a name="step-1-create-a-project-in-visual-studio"></a>Schritt 1: Erstellen eines Projekts in Visual Studio

1. In Visual Studio im Menü **Datei** die Option **neu**, und wählen Sie dann auf **Projekt**. Das Dialogfeld **Neues Projekt** wird geöffnet. 
    
2. Erstellen Sie eine **C#-Konsolenanwendung**. Wählen Sie im Fensterbereich **Vorlagen** die Option **Visual C#**, und wählen Sie dann **Konsolenanwendung**. 
    
3. Nennen Sie das Projekt „HelloWorld", und wählen Sie dann **OK**.
    
Visual Studio erstellt das Projekt und öffnet das Fenster des Codedokuments „Program.cs".

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a>Schritt 2: Hinzufügen eines Verweises auf die verwaltete EWS-API

1. Wenn der **Projektmappen-Explorer** bereits geöffnet ist, überspringen Sie diesen Schritt, und fahren Sie mit Schritt 2 fort. Um den **Projektmappen-Explorer** zu öffnen, wählen Sie im Menü **Ansicht** die Option **Projektmappen-Explorer**. 
    
2. Öffnen Sie im **Projektmappen-Explorer** und im **HelloWorld** -Projekt das Kontextmenü (Rechtsklick) für **Verweise**, und wählen Sie **Verweis hinzufügen** aus dem Kontextmenü. Ein Dialogfeld für die Verwaltung von Projektverweisen wird geöffnet. 
    
3. Wählen Sie die Option **Durchsuchen**. Navigieren Sie zu dem Speicherort, an dem Sie die DLL-Datei der verwalteten EWS-API installiert haben. Vom Installationsprogramm wird der folgende Standardpfad festgelegt: C:\Programme\Microsoft\Exchange\Web Services\<Version>\. Der Pfad variiert abhängig davon, ob Sie die 32- oder die 64-Bit-Version der Datei „Microsoft.Exchange.WebServices.dll" herunterladen. Wählen Sie **Microsoft.Exchange.WebServices.dll** und dann **OK** oder **Hinzufügen**. Hierdurch wird der Verweis auf die verwaltete EWS-API Ihrem Projekt hinzugefügt. 
    
4. Wenn Sie Verwaltete EWS-API 2.0 verwenden, ändern Sie das Ziel des HelloWorld-Projekts in .NET Framework 4. Andere Versionen der verwalteten EWS-API verwenden möglicherweise eine andere Zielversion von .NET Framework.
    
5. Vergewissern Sie sich, dass Sie die richtige Zielversion von .NET Framework verwenden. Öffnen Sie das Kontextmenü (Rechtsklick) für Ihr **HelloWorld** -Projekt im **Projektmappen-Explorer**, und wählen Sie **Eigenschaften**. Überprüfen Sie, ob **.NET Framework 4** im Dropdown-Listenfeld **Zielframework** ausgewählt ist. 
    
Nachdem Sie Ihr Projekt eingerichtet und einen Verweis auf die verwaltete EWS-API erstellt haben, können Sie Ihre erste Anwendung erstellen. Der Einfachheit halber fügen Sie Ihren Code der Datei „Program.cs" hinzu. Lesen Sie weitere Informationen zum Verweisen auf die EWS Managed API [Verweis die EWS Managed API-Assembly](how-to-reference-the-ews-managed-api-assembly.md) . Im nächsten Schritt entwickeln Sie den Basiscode zum Schreiben der meisten verwalteten EWS-API-Anwendungen. 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a>Schritt 3: Einrichten der Überprüfung der URL-Umleitung für die AutoErmittlung

- Fügen Sie die folgende Rückrufmethode zur Umleitungsüberprüfung nach der **Main(string[] args)** -Methode hinzu. Hierdurch wird überprüft, ob die umgeleiteten URLs, die von der [AutoErmittlung](autodiscover-for-exchange.md) zurückgegeben werden, einen HTTPS-Endpunkt darstellen. 
    
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

Dieser Überprüfungsrückruf wird in Schritt 4 an das **ExchangeService** -Objekt übergeben. Sie benötigen ihn, damit Ihre Anwendung Umleitungen der AutoErmittlung vertraut und diesen folgt - die Ergebnisse der AutoErmittlungsumleitung stellen den EWS-Endpunkt für unsere Anwendung dar. 

### <a name="step-4-prepare-the-exchangeservice-object"></a>Schritt 4: Vorbereiten des ExchangeService-Objekts

1. Fügen Sie der verwalteten EWS-API einen Verweis auf die **using**-Direktive hinzu. Fügen Sie den folgenden Code nach der letzten **using**-Direktive am Anfang der Datei „Program.cs" ein. 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. Instanziieren Sie in der **Main** -Methode das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt mit der gewünschten Dienstzielversion. Dieses Beispiel hat die früheste Version des EWS-Schemas als Ziel. 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. Wenn Sie einen lokalen Exchange-Server als Ziel verwenden und Ihr Client der Domäne beigetreten ist, fahren Sie mit Schritt 4 fort. Wenn das Ziel Ihres Clients ein Postfach von Exchange Online oder einer Office 365-Entwicklerwebsite ist, müssen Sie explizite Anmeldeinformationen übergeben. Fügen Sie nach der Instanziierung des **ExchangeService** -Objekts den folgenden Code hinzu, und legen Sie die Anmeldeinformationen für das Postfachkonto fest. Der Benutzername muss der Benutzerprinzipalname sein. Fahren Sie mit Schritt 5 fort. 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. Der Domäne beigetretene Clients mit einem lokalen Exchange-Server als Ziel können die standardmäßigen Anmeldeinformationen des angemeldeten Benutzers verwenden, vorausgesetzt, die Anmeldeinformationen sind einem Postfach zugeordnet. Fügen Sie nach der Instanziierung des **ExchangeService** -Objekts den folgenden Code hinzu. 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   Wenn das Ziel Ihres Clients ein Postfach von Exchange Online oder einer Office 365-Entwicklerwebsite ist, überprüfen Sie, ob [UseDefaultCredentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) auf **false** (den Standardwert) festgelegt ist. Der Client kann nun den ersten Aufruf an den AutoErmittlungsdienst durchführen, um die Dienst-URL für Aufrufe an den EWS-Dienst abzurufen. .
    
5. Die **AutodiscoverUrl** -Methode für das **ExchangeService** -Objekt führt eine Reihe von Aufrufen an den AutoErmittlungsdienst durch, um die Dienst-URL abzurufen. Wenn dieser Methodenaufruf erfolgreich ist, wird die URL-Eigenschaft des **ExchangeService** -Objekts auf die Dienst-URL festgelegt. Übergeben Sie die E-Mail-Adresse des Benutzers und den **RedirectionUrlValidationCallback** an die **AutodiscoverUrl** -Methode. Fügen Sie den folgenden Code nach den in Schritt 3 oder 4 angegebenen Anmeldeinformationen hinzu. Ändern Sie  `user1@contoso.com` in Ihre E-Mail-Adresse, sodass der AutoErmittlungsdienst Ihren EWS-Endpunkt findet. 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

An diesem Punkt ist der Client für EWS-Aufrufe zum Zugreifen auf Postfachdaten eingerichtet. Wenn Sie den Code jetzt ausführen, können Sie die Funktion des **AutodiscoverUrl** -Methodenaufrufs prüfen, indem Sie den Inhalt der [ExchangeService.Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaft untersuchen. Wenn diese Eigenschaft eine URL enthält, war Ihr Aufruf erfolgreich. Dies bedeutet, dass sich Ihre Anwendung erfolgreich beim Dienst authentifiziert und den EWS-Endpunkt für Ihr Postfach ermittelt hat. Nun können Sie Ihre ersten EWS-Aufrufe durchführen. [Legen Sie die Exchange-Webdienste-URL mithilfe der EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) für Weitere Informationen zum Festlegen der EWS-URL gelesen. 

### <a name="step-6-create-your-first-hello-world-email-message"></a>Schritt 6: Erstellen Ihrer ersten „Hello World"-E-Mail-Nachricht

1. Instanziieren Sie nach dem **AutodiscoverUrl** -Methodenaufruf ein neues **EmailMessage** -Objekt, und übergeben Sie das erstellte Dienstobjekt. 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   Sie verfügen jetzt über eine E-Mail-Nachricht, für die die Dienstbindung festgelegt ist. Alle für das **EmailMessage** -Objekt initiierten Aufrufe haben den Dienst als Ziel. 
    
2. Legen Sie nun den Empfänger für die Zeile „An" der E-Mail-Nachricht fest. Ändern Sie hierzu  `user1@contoso.com` so, dass Ihre SMTP-Adresse verwendet wird. 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. Legen Sie den Betreff und den Text der E-Mail-Nachricht fest.
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. Sie können nun Ihre erste E-Mail-Nachricht mit der verwalteten EWS-API senden. Die **Send** -Methode ruft den Dienst auf und sendet die E-Mail-Nachricht zur Übermittlung. Lesen Sie die [Kommunikation mit Exchange-Webdienste mithilfe der EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) , um Informationen zu anderen Methoden zu erhalten, die Sie verwenden können, um die Kommunikation mit Exchange. 
    
   ```cs
    email.Send();
   ```

5. Sie können die „Hello World"-Anwendung jetzt ausführen. Drücken Sie in Visual Studio **F5**. Ein leeres Konsolenfenster wird geöffnet. Im Konsolenfenster wird nichts angezeigt, während Ihre Anwendung die Authentifizierung durchführt, Umleitungen der AutoErmittlung folgt und anschließend den ersten Aufruf ausführt, um eine E-Mail-Nachricht zu erstellen, die Sie an sich selbst senden. Wenn die durchgeführten Aufrufe angezeigt werden sollen, fügen Sie vor dem Aufruf der **AutodiscoverUrl** -Methode die folgenden zwei Codezeilen hinzu. Drücken Sie dann F5. Hierdurch wird die [Ablaufverfolgung der EWS-Anforderungen und -Antworten](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) im Konsolenfenster angezeigt. 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

Sie verfügen jetzt über eine funktionsfähige verwaltete EWS-API-Clientanwendung. Der Einfachheit halber zeigt das folgende Beispiel den gesamten Code, den Sie zum Erstellen Ihrer „Hello World"-Anwendung zur Datei „Program.cs" hinzugefügt haben.

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

## <a name="next-steps"></a>Nächste Schritte
<a name="Next"> </a>

Wenn Sie weitere Aktionen mit Ihrer ersten verwalteten EWS-API-Clientanwendung ausführen möchten, erkunden Sie das folgende Informationsmaterial:
  
- [Exchange 2013: 101-Codebeispiele](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)
    
- [Ordner und Elemente](folders-and-items-in-ews-in-exchange.md)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
Falls Probleme mit der Anwendung auftreten, [veröffentlichen Sie eine Frage oder einen Kommentar im Forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (und vergessen Sie nicht, den aktuellsten Beitrag zu lesen). 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="Next"> </a>

- [Verweisen auf die Assembly EWS Managed API](how-to-reference-the-ews-managed-api-assembly.md)
    
- [Legen Sie die Exchange-Webdienste-URL mithilfe der EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)
    
- [Kommunizieren Sie mit Exchange-Webdienste mithilfe der EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a>Siehe auch

- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)   
- [TRACE-Anfragen und-Antworten EWS Managed API behandeln](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

