---
title: Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Erfahren Sie, wie Sie Dienstkonfigurationsinformationen für um, Richtlinien Anstöße, e-Mail-Tipps und Schutzregeln aus EWS in Exchange abrufen.
ms.openlocfilehash: 7546d9524f1e004eda2bdc55687fb44beafa44af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528006"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Dienstkonfigurationsinformationen für um, Richtlinien Anstöße, e-Mail-Tipps und Schutzregeln aus EWS in Exchange abrufen.
  
Funktioniert Ihre EWS-Anwendung mit Unified Messaging (um), Richtlinien Anstößen, e-Mail-Tipps oder Schutzregeln? Wenn dies der Fall ist, muss Ihre Anwendung den [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) aufrufen, um die erforderlichen Dienstkonfigurationsinformationen abzurufen. Der **GetServiceConfiguration** -Vorgang gibt Konfigurationsinformationen zurück, die für jedes dieser EWS-Features spezifisch sind. 
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
**Tabelle 1. Konfigurationsinformationen, die vom GetServiceConfiguration-Vorgang zurückgegeben werden**

|EWS-Feature|GetServiceConfiguration-Vorgang gibt zurück...|
|:-----|:-----|
|UM  <br/> | <ul><li>Ein Wert, der angibt, ob um aktiviert ist.</li><li>Ein Wert, der angibt, ob die Wiedergabe über Telefon aktiviert ist.</li><li>Die Wählzeichenfolge für Wiedergabe über Telefon.</li></ul> |
|Richtlinien Ausrichtung  <br/> | <ul><li>Richtlinien Anstöße für die Anzeige in Ihrem Client.</li></ul> |
|E-Mail-Info  <br/> | <ul><li>Ein Wert, der angibt, ob e-Mail-Tipps aktiviert sind.</li><li>Die maximale Anzahl von Empfängern pro Anforderung.</li><li>Die maximale Nachrichtengröße.</li><li>Der Schwellenwert für hohe Benutzergruppen.</li><li>Ein Wert, der angibt, ob die Anzahl der externen Empfänger angezeigt wird.</li><li>Eine Liste interner Domänen.</li><li>Ein Wert, der angibt, ob Richtlinien Tipps aktiviert sind.</li><li>Der Schwellenwert für große Zielgruppen für die Angabe, ob Ihre e-Mails als eine große Anzahl von Empfängern gelten.  </li></ul>|
|Schutzregeln  <br/> | <ul><li>Einrichten von Schutzregeln für Ihren Client.</li><li>Eine Liste der Domänen, die für Ihre Organisation intern sind.  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>Code Beispiel: Abrufen von Dienstkonfigurationsinformationen für e-Mail-Tipps mithilfe von EWS

Im folgenden Codebeispiel wird der [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) verwendet, um Dienstkonfigurationsinformationen für e-Mail-Tipps anzufordern. Sie können zusätzliche Dienstkonfigurationsinformationen anfordern, indem Sie weitere [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) -Elemente mit unterschiedlichen Werten hinzufügen. 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
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

Nachdem Sie Dienstkonfigurationsinformationen angefordert haben, verwenden Sie die [XmlDocument-Klasse](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) , um die XML-Antwort zu laden, damit Sie Sie analysieren können. Je nach Szenario können Sie dann eine der folgenden Aktionen ausführen: 
  
- Verwenden Sie den [GetMailTips-Vorgang](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) , um e-Mail-Tipps für Clientanwendungen anzuzeigen, die Benutzern angezeigt werden sollen. 
    
- Wenn um aktiviert ist, [erfahren Sie, wie Sie Postfachelemente](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) über Ihr Telefon wiedergeben. 
    
## <a name="see-also"></a>Siehe auch

- [Konfigurationsoptionen für EWS in Exchange](configuration-options-for-ews-in-exchange.md)    
- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

