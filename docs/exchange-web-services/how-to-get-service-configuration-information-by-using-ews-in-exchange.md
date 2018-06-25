---
title: Abrufen von Service-Konfigurationsinformationen mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Erfahren Sie, wie im Exchange Service-Konfigurationsinformationen für UM, Richtlinie verschieben, e-Mail-Infos und Regeln für den Schutz von EWS abgerufen.
ms.openlocfilehash: e84a563bb094a2fe03e08f8e1a81b2b054d45850
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756893"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>Abrufen von Service-Konfigurationsinformationen mithilfe der EWS in Exchange

Erfahren Sie, wie im Exchange Service-Konfigurationsinformationen für UM, Richtlinie verschieben, e-Mail-Infos und Regeln für den Schutz von EWS abgerufen.
  
Funktioniert die EWS-Anwendung mit Unified Messaging (UM), Richtlinie verschieben, e-Mail-Infos oder Schutzregeln? Wenn dies der Fall ist, müssen Ihre Anwendung rufen Sie den [Vorgang GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) um die Konfigurationsinformationen für den Dienst zu erhalten, die benötigt werden. Der Vorgang **GetServiceConfiguration** gibt Konfigurationsinformationen, die speziell für die einzelnen Features EWS. zurück. 
  
> [!NOTE]
> [!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
**In Tabelle 1. Konfigurationsinformationen, die der Vorgang GetServiceConfiguration zurückgibt**

|EWS-Funktion|GetServiceConfiguration Vorgang gibt...|
|:-----|:-----|
|UM  <br/> | <ul><li>Ein Wert, der angibt, ob UM aktiviert ist.</li><li>Ein Wert, der angibt, ob am Telefon wiedergeben aktiviert ist.</li><li>Am Telefon Dial Zeichenfolge wiedergeben.</li></ul> |
|Richtlinie verschieben  <br/> | <ul><li>Richtlinie verschiebt für die Anzeige in Ihrem Client.</li></ul> |
|E-Mail-Infos  <br/> | <ul><li>Ein Wert, der angibt, ob e-Mail-Infos aktiviert sind.</li><li>Die maximale Anzahl von Empfängern pro Anforderung.</li><li>Die maximale Nachrichtengröße.</li><li>Der Schwellenwert für die große Benutzergruppe.</li><li>Ein Wert, der angibt, ob die Anzahl der externe Empfänger angezeigt wird.</li><li>Eine Liste von internen Domänen.</li><li>Ein Wert, der angibt, ob richtlinientipps aktiviert sind.</li><li>Die große Benutzergruppe Cap Schwellenwert für zurück, der angibt, ob Ihre e-Mails an eine große Anzahl von Empfängern betrachtet werden.  </li></ul>|
|Regeln für den Schutz  <br/> | <ul><li>Protection Rules-Setup für den Client.</li><li>Eine Liste der Domänen, die organisationsinterne sind.  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>Codebeispiel: Abrufen von Informationen der Dienstkonfiguration für e-Mail-Infos mithilfe von EWS

Im folgenden Codebeispiel wird verwendet des [GetServiceConfiguration Vorgang](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) Anforderung Service-Konfigurationsinformationen für e-Mail-Infos. Sie können zusätzliche Informationen über Dienstkonfiguration durch Hinzufügen von [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) Elementen mit unterschiedlichen Werten anfordern. 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
    "               xmlns:xs=\"http://www.w3.org/2001/XMLSchema\">\n" +
    "  <soap:Header>\n" +
    "    <t:RequestServerVersion Version=\"Exchange2013\" />\n" +
    "  </soap:Header>\n" +
    "  <soap:Body>\n" +
    "    <m:GetServiceConfiguration>\n" +
    "      <m:ActingAs>\n" +
    "        <t:EmailAddress>user1@contoso.com</t:EmailAddress>\n" +
    "        <t:RoutingType>SMTP</t:RoutingType>\n" +
    "      </m:ActingAs>\n" +
    "      <m:RequestedConfiguration>\n" +
    "        <m:ConfigurationName>MailTips</m:ConfigurationName>\n" +
    "      </m:RequestedConfiguration>\n" +
    "    </m:GetServiceConfiguration>\n" +
    "  </soap:Body>\n" +
    "</soap:Envelope>";
  // Encoded GetServiceConfiguration operation request.
  byte[] payload = System.Text.Encoding.UTF8.GetBytes(getServiceConfigurationRequest);
  try
  {
    HttpWebRequest request = (HttpWebRequest)WebRequest.Create(service.Url);
    request.AllowAutoRedirect = false;
    request.Credentials = creds;
    request.Method = "POST";
    request.ContentType = "text/xml";
    Stream requestStream = request.GetRequestStream();
    requestStream.Write(payload, 0, payload.Length);
    requestStream.Close();
    HttpWebResponse response = (HttpWebResponse)request.GetResponse();
    if (response.StatusCode == HttpStatusCode.OK)
    {
      Stream responseStream = response.GetResponseStream();
      StreamReader reader = new StreamReader(responseStream);
      string responseFromServer = reader.ReadToEnd();
      Console.WriteLine("You will need to parse this response to get the configuration information:\n\n" + responseFromServer);
      reader.Close();
      responseStream.Close();
    }
    else
      throw new WebException(response.StatusDescription);
          
  }
  catch (WebException e)
  {
    Console.WriteLine(e.Message);
  }
}

```

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie Dienstkonfigurationsinformationen anfordern, verwenden Sie die [XmlDocument-Klasse](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) , die XML-Antwort geladen werden, damit Sie analysiert werden können. Klicken Sie dann je nach Szenario Möglichkeiten eine der folgenden: 
  
- Verwenden Sie die [GetMailTips Vorgang](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) zum Abrufen von e-Mail-Infos für Clientanwendungen, die Benutzern angezeigt. 
    
- Wenn UM aktiviert ist, [erhalten Sie Informationen zum Abspielen Postfachelemente](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) über Ihr Telefon. 
    
## <a name="see-also"></a>Siehe auch

- [Konfigurationsoptionen für EWS in Exchange](configuration-options-for-ews-in-exchange.md)    
- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

