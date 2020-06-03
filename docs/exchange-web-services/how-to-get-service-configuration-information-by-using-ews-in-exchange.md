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
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="891a3-103">Abrufen von Dienstkonfigurationsinformationen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="891a3-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="891a3-104">Erfahren Sie, wie Sie Dienstkonfigurationsinformationen für um, Richtlinien Anstöße, e-Mail-Tipps und Schutzregeln aus EWS in Exchange abrufen.</span><span class="sxs-lookup"><span data-stu-id="891a3-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="891a3-105">Funktioniert Ihre EWS-Anwendung mit Unified Messaging (um), Richtlinien Anstößen, e-Mail-Tipps oder Schutzregeln?</span><span class="sxs-lookup"><span data-stu-id="891a3-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="891a3-106">Wenn dies der Fall ist, muss Ihre Anwendung den [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) aufrufen, um die erforderlichen Dienstkonfigurationsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="891a3-106">If so, your application will need to call the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="891a3-107">Der **GetServiceConfiguration** -Vorgang gibt Konfigurationsinformationen zurück, die für jedes dieser EWS-Features spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="891a3-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="891a3-108">Die verwaltete EWS-API implementiert diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="891a3-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="891a3-109">**Tabelle 1. Konfigurationsinformationen, die vom GetServiceConfiguration-Vorgang zurückgegeben werden**</span><span class="sxs-lookup"><span data-stu-id="891a3-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="891a3-110">EWS-Feature</span><span class="sxs-lookup"><span data-stu-id="891a3-110">EWS feature</span></span>|<span data-ttu-id="891a3-111">GetServiceConfiguration-Vorgang gibt zurück...</span><span class="sxs-lookup"><span data-stu-id="891a3-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="891a3-112">UM</span><span class="sxs-lookup"><span data-stu-id="891a3-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="891a3-113">Ein Wert, der angibt, ob um aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="891a3-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="891a3-114">Ein Wert, der angibt, ob die Wiedergabe über Telefon aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="891a3-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="891a3-115">Die Wählzeichenfolge für Wiedergabe über Telefon.</span><span class="sxs-lookup"><span data-stu-id="891a3-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="891a3-116">Richtlinien Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="891a3-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="891a3-117">Richtlinien Anstöße für die Anzeige in Ihrem Client.</span><span class="sxs-lookup"><span data-stu-id="891a3-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="891a3-118">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="891a3-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="891a3-119">Ein Wert, der angibt, ob e-Mail-Tipps aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="891a3-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="891a3-120">Die maximale Anzahl von Empfängern pro Anforderung.</span><span class="sxs-lookup"><span data-stu-id="891a3-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="891a3-121">Die maximale Nachrichtengröße.</span><span class="sxs-lookup"><span data-stu-id="891a3-121">The maximum message size.</span></span></li><li><span data-ttu-id="891a3-122">Der Schwellenwert für hohe Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="891a3-122">The large audience threshold.</span></span></li><li><span data-ttu-id="891a3-123">Ein Wert, der angibt, ob die Anzahl der externen Empfänger angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="891a3-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="891a3-124">Eine Liste interner Domänen.</span><span class="sxs-lookup"><span data-stu-id="891a3-124">A list of internal domains.</span></span></li><li><span data-ttu-id="891a3-125">Ein Wert, der angibt, ob Richtlinien Tipps aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="891a3-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="891a3-126">Der Schwellenwert für große Zielgruppen für die Angabe, ob Ihre e-Mails als eine große Anzahl von Empfängern gelten.</span><span class="sxs-lookup"><span data-stu-id="891a3-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="891a3-127">Schutzregeln</span><span class="sxs-lookup"><span data-stu-id="891a3-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="891a3-128">Einrichten von Schutzregeln für Ihren Client.</span><span class="sxs-lookup"><span data-stu-id="891a3-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="891a3-129">Eine Liste der Domänen, die für Ihre Organisation intern sind.</span><span class="sxs-lookup"><span data-stu-id="891a3-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="891a3-130">Code Beispiel: Abrufen von Dienstkonfigurationsinformationen für e-Mail-Tipps mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="891a3-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="891a3-131">Im folgenden Codebeispiel wird der [GetServiceConfiguration-Vorgang](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) verwendet, um Dienstkonfigurationsinformationen für e-Mail-Tipps anzufordern.</span><span class="sxs-lookup"><span data-stu-id="891a3-131">The following code example uses the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="891a3-132">Sie können zusätzliche Dienstkonfigurationsinformationen anfordern, indem Sie weitere [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) -Elemente mit unterschiedlichen Werten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="891a3-132">You can request additional service configuration information by adding more [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
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

## <a name="next-steps"></a><span data-ttu-id="891a3-133">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="891a3-133">Next steps</span></span>

<span data-ttu-id="891a3-134">Nachdem Sie Dienstkonfigurationsinformationen angefordert haben, verwenden Sie die [XmlDocument-Klasse](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) , um die XML-Antwort zu laden, damit Sie Sie analysieren können.</span><span class="sxs-lookup"><span data-stu-id="891a3-134">After you request service configuration information, use the [XmlDocument class](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="891a3-135">Je nach Szenario können Sie dann eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="891a3-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="891a3-136">Verwenden Sie den [GetMailTips-Vorgang](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) , um e-Mail-Tipps für Clientanwendungen anzuzeigen, die Benutzern angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="891a3-136">Use the [GetMailTips operation](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="891a3-137">Wenn um aktiviert ist, [erfahren Sie, wie Sie Postfachelemente](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) über Ihr Telefon wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="891a3-137">If UM is enabled, [learn about how to play mailbox items](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="891a3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="891a3-138">See also</span></span>

- [<span data-ttu-id="891a3-139">Konfigurationsoptionen für EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="891a3-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="891a3-140">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="891a3-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="891a3-141">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="891a3-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

