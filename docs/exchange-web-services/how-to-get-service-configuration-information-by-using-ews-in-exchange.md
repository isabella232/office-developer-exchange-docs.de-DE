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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756893"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="1095b-103">Abrufen von Service-Konfigurationsinformationen mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1095b-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="1095b-104">Erfahren Sie, wie im Exchange Service-Konfigurationsinformationen für UM, Richtlinie verschieben, e-Mail-Infos und Regeln für den Schutz von EWS abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1095b-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="1095b-105">Funktioniert die EWS-Anwendung mit Unified Messaging (UM), Richtlinie verschieben, e-Mail-Infos oder Schutzregeln?</span><span class="sxs-lookup"><span data-stu-id="1095b-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="1095b-106">Wenn dies der Fall ist, müssen Ihre Anwendung rufen Sie den [Vorgang GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) um die Konfigurationsinformationen für den Dienst zu erhalten, die benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="1095b-106">If so, your application will need to call the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="1095b-107">Der Vorgang **GetServiceConfiguration** gibt Konfigurationsinformationen, die speziell für die einzelnen Features EWS. zurück.</span><span class="sxs-lookup"><span data-stu-id="1095b-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1095b-108">[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="1095b-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="1095b-109">**In Tabelle 1. Konfigurationsinformationen, die der Vorgang GetServiceConfiguration zurückgibt**</span><span class="sxs-lookup"><span data-stu-id="1095b-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="1095b-110">EWS-Funktion</span><span class="sxs-lookup"><span data-stu-id="1095b-110">EWS feature</span></span>|<span data-ttu-id="1095b-111">GetServiceConfiguration Vorgang gibt...</span><span class="sxs-lookup"><span data-stu-id="1095b-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="1095b-112">UM</span><span class="sxs-lookup"><span data-stu-id="1095b-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="1095b-113">Ein Wert, der angibt, ob UM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1095b-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="1095b-114">Ein Wert, der angibt, ob am Telefon wiedergeben aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1095b-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="1095b-115">Am Telefon Dial Zeichenfolge wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="1095b-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="1095b-116">Richtlinie verschieben</span><span class="sxs-lookup"><span data-stu-id="1095b-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="1095b-117">Richtlinie verschiebt für die Anzeige in Ihrem Client.</span><span class="sxs-lookup"><span data-stu-id="1095b-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="1095b-118">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="1095b-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="1095b-119">Ein Wert, der angibt, ob e-Mail-Infos aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1095b-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="1095b-120">Die maximale Anzahl von Empfängern pro Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1095b-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="1095b-121">Die maximale Nachrichtengröße.</span><span class="sxs-lookup"><span data-stu-id="1095b-121">The maximum message size.</span></span></li><li><span data-ttu-id="1095b-122">Der Schwellenwert für die große Benutzergruppe.</span><span class="sxs-lookup"><span data-stu-id="1095b-122">The large audience threshold.</span></span></li><li><span data-ttu-id="1095b-123">Ein Wert, der angibt, ob die Anzahl der externe Empfänger angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1095b-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="1095b-124">Eine Liste von internen Domänen.</span><span class="sxs-lookup"><span data-stu-id="1095b-124">A list of internal domains.</span></span></li><li><span data-ttu-id="1095b-125">Ein Wert, der angibt, ob richtlinientipps aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1095b-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="1095b-126">Die große Benutzergruppe Cap Schwellenwert für zurück, der angibt, ob Ihre e-Mails an eine große Anzahl von Empfängern betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="1095b-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="1095b-127">Regeln für den Schutz</span><span class="sxs-lookup"><span data-stu-id="1095b-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="1095b-128">Protection Rules-Setup für den Client.</span><span class="sxs-lookup"><span data-stu-id="1095b-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="1095b-129">Eine Liste der Domänen, die organisationsinterne sind.</span><span class="sxs-lookup"><span data-stu-id="1095b-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="1095b-130">Codebeispiel: Abrufen von Informationen der Dienstkonfiguration für e-Mail-Infos mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="1095b-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="1095b-131">Im folgenden Codebeispiel wird verwendet des [GetServiceConfiguration Vorgang](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) Anforderung Service-Konfigurationsinformationen für e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="1095b-131">The following code example uses the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="1095b-132">Sie können zusätzliche Informationen über Dienstkonfiguration durch Hinzufügen von [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) Elementen mit unterschiedlichen Werten anfordern.</span><span class="sxs-lookup"><span data-stu-id="1095b-132">You can request additional service configuration information by adding more [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
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

## <a name="next-steps"></a><span data-ttu-id="1095b-133">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1095b-133">Next steps</span></span>

<span data-ttu-id="1095b-134">Nachdem Sie Dienstkonfigurationsinformationen anfordern, verwenden Sie die [XmlDocument-Klasse](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) , die XML-Antwort geladen werden, damit Sie analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="1095b-134">After you request service configuration information, use the [XmlDocument class](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="1095b-135">Klicken Sie dann je nach Szenario Möglichkeiten eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="1095b-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="1095b-136">Verwenden Sie die [GetMailTips Vorgang](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) zum Abrufen von e-Mail-Infos für Clientanwendungen, die Benutzern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1095b-136">Use the [GetMailTips operation](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="1095b-137">Wenn UM aktiviert ist, [erhalten Sie Informationen zum Abspielen Postfachelemente](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) über Ihr Telefon.</span><span class="sxs-lookup"><span data-stu-id="1095b-137">If UM is enabled, [learn about how to play mailbox items](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1095b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1095b-138">See also</span></span>

- [<span data-ttu-id="1095b-139">Konfigurationsoptionen für EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1095b-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="1095b-140">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="1095b-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="1095b-141">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="1095b-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

