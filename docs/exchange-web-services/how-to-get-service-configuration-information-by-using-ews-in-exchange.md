---
title: Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Erfahren Sie, wie Sie Dienstkonfigurationsinformationen für UM, Richtlinien-Nudges, E-Mail-Tipps und Schutzregeln von EWS in Exchange abrufen.
ms.openlocfilehash: 30d4058104726c79f473a88a09398689675b988d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513171"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a>Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Dienstkonfigurationsinformationen für UM, Richtlinien-Nudges, E-Mail-Tipps und Schutzregeln von EWS in Exchange abrufen.
  
Funktioniert Ihre EWS-Anwendung mit Unified Messaging (UM), Richtlinien-Nudges, E-Mail-Tipps oder Schutzregeln? Wenn ja, muss Ihre Anwendung den [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) aufrufen, um die benötigten Dienstkonfigurationsinformationen abzurufen. Der **GetServiceConfiguration-Vorgang** gibt Konfigurationsinformationen zurück, die für jedes dieser EWS-Features spezifisch sind. 
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
**Tabelle 1. Konfigurationsinformationen, die der GetServiceConfiguration-Vorgang zurückgibt**

|EWS-Feature|GetServiceConfiguration-Vorgang gibt...|
|:-----|:-----|
|UM  <br/> | <ul><li>Ein Wert, der angibt, ob UM aktiviert ist.</li><li>Ein Wert, der angibt, ob die Wiedergabe auf dem Telefon aktiviert ist.</li><li>Die Wiedergabe der Telefonwählzeichenfolge.</li></ul> |
|Richtlinien-Nudges  <br/> | <ul><li>Richtlinien-Nudges für die Anzeige in Ihrem Client.</li></ul> |
|E-Mail-Info  <br/> | <ul><li>Ein Wert, der angibt, ob E-Mail-Tipps aktiviert sind.</li><li>Die maximale Anzahl von Empfängern pro Anforderung.</li><li>Die maximale Nachrichtengröße.</li><li>Der Schwellenwert für große Zielgruppen.</li><li>Ein Wert, der angibt, ob die Anzahl der externen Empfänger angezeigt wird.</li><li>Eine Liste der internen Domänen.</li><li>Ein Wert, der angibt, ob Richtlinientipps aktiviert sind.</li><li>Der Grenzwert für große Zielgruppen, der angibt, ob Ihre E-Mails als eine große Anzahl von Empfängern betrachtet werden.  </li></ul>|
|Schutzregeln  <br/> | <ul><li>Einrichten von Schutzregeln für Ihren Client.</li><li>Eine Liste der Domänen, die in Ihrer Organisation intern sind.  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a>Codebeispiel: Abrufen von Dienstkonfigurationsinformationen für E-Mail-Tipps mithilfe von EWS

Im folgenden Codebeispiel wird der [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) verwendet, um Dienstkonfigurationsinformationen für E-Mail-Tipps anzufordern. Sie können zusätzliche Dienstkonfigurationsinformationen anfordern, indem Sie weitere [ConfigurationName-Elemente](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) mit unterschiedlichen Werten hinzufügen. 
  
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

Nachdem Sie Dienstkonfigurationsinformationen angefordert haben, verwenden Sie die [XmlDocument-Klasse,](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) um die Antwort-XML zu laden, damit Sie sie analysieren können. Je nach Szenario können Sie dann eine der folgenden Aktionen ausführen: 
  
- Verwenden Sie den [GetMailTips-Vorgang,](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) um E-Mail-Tipps für Clientanwendungen abzurufen, die Benutzern angezeigt werden sollen. 
    
- Wenn UM aktiviert ist, [erfahren Sie, wie Sie Postfachelemente](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) über Ihr Telefon wiedergeben. 
    
## <a name="see-also"></a>Siehe auch

- [Konfigurationsoptionen für EWS in Exchange](configuration-options-for-ews-in-exchange.md)    
- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

