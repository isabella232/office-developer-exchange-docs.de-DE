---
title: Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um die Clientanwendung an den richtigen Exchange-Server zu leiten.
ms.openlocfilehash: eb3fb3664e5789638c097a43cf48f757bb0713ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353980"
---
# <a name="use-autodiscover-to-find-connection-points"></a><span data-ttu-id="a9539-103">Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten</span><span class="sxs-lookup"><span data-stu-id="a9539-103">Use Autodiscover to find connection points</span></span>

<span data-ttu-id="a9539-104">Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um die Clientanwendung an den richtigen Exchange-Server zu leiten.</span><span class="sxs-lookup"><span data-stu-id="a9539-104">Find out how to use the Autodiscover service to direct your client application to the correct Exchange server.</span></span>
  
<span data-ttu-id="a9539-105">Der Exchange-AutoErmittlungsdienst stellt die Clientanwendung mit Konfigurationseinstellungen für e-Mail-Konten, die gehostet werden auf Exchange Online, Exchange Online als Teil von Office 365 oder Exchange-Server eine Version von Exchange beginnend mit Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="a9539-105">The Exchange Autodiscover service provides your client application with configuration settings for email accounts that are hosted on Exchange Online, Exchange Online as part of Office 365, or an Exchange server running a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="a9539-106">Der AutoErmittlungsdienst ist ein Webdienst, der Konfigurationseinstellungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a9539-106">The Autodiscover service is a web service that provides configuration settings.</span></span> <span data-ttu-id="a9539-107">Der AutoErmittlungsdienst ist ein Webdienst, der Exchange Server-Konfigurationsinformationen an die Clientanwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a9539-107">The Autodiscover service is a web service that provides Exchange server configuration information to your client application.</span></span> <span data-ttu-id="a9539-108">-Clientanwendungen verwenden AutoErmittlung, um den Endpunkt des AutoErmittlungsdiensts für ein bestimmtes Postfach zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a9539-108">Client applications use Autodiscover to determine the endpoint of the Autodiscover service for a specific mailbox.</span></span> <span data-ttu-id="a9539-109">In diesem Artikel wird erläutert, wie die Antworten von einem Exchange-Server den richtigen Endpunkt gefunden folgen.</span><span class="sxs-lookup"><span data-stu-id="a9539-109">This article explains how to follow the responses from an Exchange server to find the correct endpoint.</span></span> 
  
<span data-ttu-id="a9539-110">Informationen zum e-Mail-Adresse Konfigurationseinstellungen erhalten möchten finden Sie unter [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) [rufen](how-to-get-domain-settings-from-an-exchange-server.md)und domäneneinstellungen von einem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="a9539-110">For information about how to get email address configuration settings, see [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and [Get domain settings from an Exchange server](how-to-get-domain-settings-from-an-exchange-server.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a9539-111">Der Prozess für die Suche nach den richtigen Endpunkt ist Teil der Anforderung für Benutzer oder eine domäneneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a9539-111">The process for finding the correct endpoint is part of the request for user or domain settings.</span></span> <span data-ttu-id="a9539-112">Der AutoErmittlungsdienst verwendet eine Reihe von Antworten umleiten, um die Clientanwendung auf den richtigen Endpunkt für eine e-Mail-Adresse zu senden.</span><span class="sxs-lookup"><span data-stu-id="a9539-112">The Autodiscover service uses a series of redirect responses to send the client application to the correct endpoint for an email address.</span></span> 
  
<span data-ttu-id="a9539-113">Eines der folgenden Exchange-Entwicklungstechnologien können Sie den AutoErmittlungsdienst zugreifen:</span><span class="sxs-lookup"><span data-stu-id="a9539-113">You can use one of the following Exchange development technologies to access the Autodiscover service:</span></span>

- <span data-ttu-id="a9539-114">Die verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)</span><span class="sxs-lookup"><span data-stu-id="a9539-114">The Exchange Web Services (EWS) Managed API</span></span>
    
- <span data-ttu-id="a9539-115">EWS</span><span class="sxs-lookup"><span data-stu-id="a9539-115">EWS</span></span>
    
<span data-ttu-id="a9539-116">Bei Verwendung von EWS können Sie die folgenden Methoden zum Abrufen von Benutzereinstellungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="a9539-116">If you are using EWS, you can use the following methods to retrieve user settings:</span></span>
    
- <span data-ttu-id="a9539-117">Den SOAP-basierten AutoErmittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="a9539-117">The SOAP-based Autodiscover service</span></span>
    
- <span data-ttu-id="a9539-118">Den XML-AutoErmittlungsdienst (POX)</span><span class="sxs-lookup"><span data-stu-id="a9539-118">The XML (POX) Autodiscover service</span></span>
    
- <span data-ttu-id="a9539-119">Einen automatisch vom SOAP- oder XML-AutoErmittlungdienst generierten Proxy</span><span class="sxs-lookup"><span data-stu-id="a9539-119">An autogenerated proxy generated from the SOAP or XML Autodiscover service</span></span>
    
<span data-ttu-id="a9539-120">Weitere Informationen zu diesen Methoden finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-120">For more information about these methods, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span>

<span data-ttu-id="a9539-121">Weitere Informationen über diese Exchange-Entwicklungstechnologien finden Sie unter [Durchsuchen die EWS Managed API, EWS, und Web services im Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-121">For more information about these Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span> 

<span data-ttu-id="a9539-p103">Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit. Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden. Die verwaltete EWS-API-Schnittstelle ist besser für ein einfaches Objektmodell optimiert als der typische automatisch generierte Webdienstproxy.</span><span class="sxs-lookup"><span data-stu-id="a9539-p103">The EWS Managed API provides an object-based interface for retrieving user settings. If your client application uses managed code, we recommend that you use the EWS Managed API. The EWS Managed API interface is better optimized for a simple object model than the typical autogenerated web service proxy.</span></span> 
  
<span data-ttu-id="a9539-125">Bei Verwendung von EWS empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9539-125">If you are using EWS, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span>
  
## <a name="prerequisites-for-finding-an-endpoint"></a><span data-ttu-id="a9539-126">Erforderliche Komponenten für die Suche nach einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="a9539-126">Prerequisites for finding an endpoint</span></span>
<span data-ttu-id="a9539-127"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="a9539-127"></span></span>

<span data-ttu-id="a9539-128">Bevor Sie eine Clientanwendung, die den AutoErmittlungsdienst verwendet erstellen können, müssen Sie haben Zugriff auf die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a9539-128">Before you can create a client application that uses the Autodiscover service, you need to have access to the following:</span></span>
  
- <span data-ttu-id="a9539-129">Exchange Online oder einem Server, der eine Version von Exchange ausgeführt wird, beginnend mit Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="a9539-129">Exchange Online or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> <span data-ttu-id="a9539-130">Wenn Sie die SOAP-basierte AutoErmittlungsdienst, Exchange Online oder eine Version von Exchange, beginnend mit Exchange 2010 verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9539-130">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
- <span data-ttu-id="a9539-p105">Einen Exchange-Server, der Verbindungen von Ihrer Clientanwendung akzeptiert. Informationen zum Konfigurieren des Exchange-Servers finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-p105">An Exchange server that is configured to accept connections from your client application. For information about how to configure your Exchange server, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
- <span data-ttu-id="a9539-p106">Ein Konto, das berechtigt ist, EWS zu verwenden. Informationen zum Konfigurieren eines Kontos finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-p106">An account that is authorized to use EWS. For information about how to configure an account, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="a9539-135">[!HINWEIS] Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen einen Zertifikatüberprüfungsrückruf bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a9539-135">If you are using the EWS Managed API, you must provide a certificate validation callback in some circumstances.</span></span> <span data-ttu-id="a9539-136">Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise einen Zertifikatüberprüfungsrückruf.</span><span class="sxs-lookup"><span data-stu-id="a9539-136">You may also need a certificate validation callback with some generated proxy libraries, such as those created by Visual Studio.</span></span> <span data-ttu-id="a9539-137">Weitere Informationen finden Sie unter [Validate ein Serverzertifikat für die EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-137">For more information, see [Validate a server certificate for the EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> 
  
### <a name="core-concepts-for-finding-an-endpoint"></a><span data-ttu-id="a9539-138">Kernkonzepte für die Suche nach einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="a9539-138">Core concepts for finding an endpoint</span></span>
<span data-ttu-id="a9539-139"><a name="bk_Core"> </a></span><span class="sxs-lookup"><span data-stu-id="a9539-139"></span></span>

<span data-ttu-id="a9539-140">Bevor Sie AutoErmittlung verwenden, um einen Endpunkt zu ermitteln, sollten Sie mit den in der folgenden Tabelle aufgeführten Konzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a9539-140">Before you use Autodiscover to find an endpoint, you should be familiar with the concepts listed in the following table.</span></span>
  
|<span data-ttu-id="a9539-141">**Konzept**</span><span class="sxs-lookup"><span data-stu-id="a9539-141">**Concept**</span></span>|<span data-ttu-id="a9539-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9539-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9539-143">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="a9539-143">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="a9539-144">Bietet eine Übersicht über die Funktionsweise des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="a9539-144">Provides an overview of how the Autodiscover service works.</span></span>  <br/> |
   
<span data-ttu-id="a9539-145">Wenn Sie die verwaltete EWS-API benutzen, verwenden Sie die Klasse [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) im Namespace [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx), um Ihre Verbindungen mit EWS zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a9539-145">If you are using the EWS Managed API, you use the [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx) namespace to manage your connection to EWS.</span></span> <span data-ttu-id="a9539-146">Um die EWS Managed API-Codebeispiele in diesem Artikel zu verwenden, müssen Sie die folgenden Namespaces in Ihrem Code zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="a9539-146">To use the EWS Managed API code samples in this article, you need to reference the following namespaces in your code:</span></span> 
  
- <span data-ttu-id="a9539-147">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="a9539-147">**System.Net**</span></span>
    
- <span data-ttu-id="a9539-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span><span class="sxs-lookup"><span data-stu-id="a9539-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span></span>
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a><span data-ttu-id="a9539-149">Suchen Sie nach den richtigen Endpunkt mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="a9539-149">Find the correct endpoint by using the EWS Managed API</span></span>
<span data-ttu-id="a9539-150"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="a9539-150"></span></span>

<span data-ttu-id="a9539-151">Wenn Sie die EWS Managed API verwenden, werden Anrufe mit dem AutoErmittlungsdienst von der Klasse **ExchangeService** behandelt.</span><span class="sxs-lookup"><span data-stu-id="a9539-151">If you are using the EWS Managed API, calls to the Autodiscover service are handled by the **ExchangeService** class.</span></span> <span data-ttu-id="a9539-152">Um den richtigen Endpunkt für ein e-Mail-Konto zu bestimmen, rufen Sie die **AutodiscoverUrl** -Methode für ein Objekt **[ExchangeService]** .</span><span class="sxs-lookup"><span data-stu-id="a9539-152">To determine the correct endpoint for an email account, you call the **AutodiscoverUrl** method on an **[ExchangeService]** object.</span></span> <span data-ttu-id="a9539-153">Im folgenden Codebeispiel wird veranschaulicht, wie den EWS Webdienst-Endpunkt für eine e-Mail-Adresse an der Datei besteht, auf den entsprechenden Client Access Server festgelegt wird, wird die EWS Managed API.</span><span class="sxs-lookup"><span data-stu-id="a9539-153">The following code example shows how to set the EWS web service endpoint for an email address to the Exchange.asmx file on the correct Client Access server by using the EWS Managed API.</span></span> 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a><span data-ttu-id="a9539-154">Suchen Sie nach den richtigen Endpunkt mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="a9539-154">Find the correct endpoint by using EWS</span></span>
<span data-ttu-id="a9539-155"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="a9539-155"></span></span>

<span data-ttu-id="a9539-156">Der SOAP-AutoErmittlungsdienst kann eine Reihe von Anforderungen und-Antworten verwenden, um die Anwendung der richtigen Endpunkt für EWS.</span><span class="sxs-lookup"><span data-stu-id="a9539-156">The SOAP Autodiscover service may use a series of requests and responses to direct your application to the correct endpoint for EWS.</span></span> <span data-ttu-id="a9539-157">Informationen zu den Prozess zur Ermittlung des richtigen Endpunkts für ein e-Mail-Konto finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-157">For information about the process for determining the correct endpoint for an email account, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> <span data-ttu-id="a9539-158">Den folgenden XML-Beispielen, die Reihe von Anforderungen und Antworten, die Sie erwarten können, bei der eine AutoErmittlung SOAP-Anforderung an den richtigen Endpunkt finden.</span><span class="sxs-lookup"><span data-stu-id="a9539-158">The following XML examples show the series of requests and responses that you can expect when making a SOAP Autodiscover request to find the correct endpoint.</span></span>
  
### <a name="soap-autodiscover-endpoint-request"></a><span data-ttu-id="a9539-159">SOAP-Anforderung der AutoErmittlung-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="a9539-159">SOAP Autodiscover endpoint request</span></span>

<span data-ttu-id="a9539-160">Das folgende Beispiel zeigt eine XML-Anforderung, die mit dem AutoErmittlungsdienst gesendet wird, den richtigen Endpunkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9539-160">The following example shows an XML request that is sent to the Autodiscover service to find the correct endpoint.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a><span data-ttu-id="a9539-161">SOAP-Antwort der AutoErmittlung-Umleitung</span><span class="sxs-lookup"><span data-stu-id="a9539-161">SOAP Autodiscover redirection response</span></span>

<span data-ttu-id="a9539-162">Der AutoErmittlungsdienst reagiert mit einem von zwei Umleitungsantworten: eine HTTP 302-Umleitung oder SOAP-Antwort-Umleitung.</span><span class="sxs-lookup"><span data-stu-id="a9539-162">The Autodiscover service may respond with one of two redirection responses: an HTTP 302 redirect, or a SOAP redirection response.</span></span> <span data-ttu-id="a9539-163">Wenn die Antwort vom Exchange-Server eine HTTP 302-Umleitung ist, sollte die Clientanwendung überprüfen, ob die Umleitung Adresse zulässig ist, und führen Sie dann die Umleitung Antwort.</span><span class="sxs-lookup"><span data-stu-id="a9539-163">If the response from the Exchange server is an HTTP 302 redirect, the client application should validate that the redirection address is acceptable and then follow the redirection response.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a9539-164">Kriterien für eine Antwort Umleitung zu überprüfen finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a9539-164">For criteria for validating a redirection response, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> 
  
<span data-ttu-id="a9539-165">Wenn der AutoErmittlungsdienst eine Umleitung Antwort vom [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **UserResponse** -Elements angegeben zurückgibt sollten Ihre Client-Anwendung das **RedirectTarget** -Element verwenden, um eine neue Anforderung Einstellungen zu erstellen, die ist in der Antwort Umleitung angegebenen Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9539-165">If the Autodiscover service returns a redirection response, indicated by the [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element, your client application should use the **RedirectTarget** element to construct a new settings request that is sent to the server specified in the redirection response.</span></span> <span data-ttu-id="a9539-166">Das folgende Beispiel zeigt eine Umleitung Antwort vom Server.</span><span class="sxs-lookup"><span data-stu-id="a9539-166">The following example shows a redirection response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="a9539-167">Nach einer Umleitung verwendet der Client die umleitungs-URL, um eine weitere Anforderung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="a9539-167">After a redirection, the client uses the redirection URL to prepare another request.</span></span> <span data-ttu-id="a9539-168">Der folgende Code zeigt ein Beispiel der Anforderung, die Sie aus der Umleitung Antwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9539-168">The following code shows an example of the request that you create from the redirection response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="a9539-169">Wenn die Client-Anwendung an den richtigen Endpunkt für den AutoErmittlungsdienst geleitet wurde, sendet der Server eine Antwort mit dem [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **UserResponse** -Elements auf **NoError** festgelegt und die angeforderte enthält benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a9539-169">When the client application has been directed to the correct endpoint for the Autodiscover service, the server will send a response with the [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element set to **NoError** and containing the requested user settings.</span></span> <span data-ttu-id="a9539-170">Nur die angeforderten benutzereinstellungen für **InternalEwsUrl** und **"externalewsurl"**, zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9539-170">Only the requested user settings, **InternalEwsUrl** and **ExternalEwsUrl**, are returned.</span></span> <span data-ttu-id="a9539-171">Das folgende Beispiel zeigt die Antwort vom Server.</span><span class="sxs-lookup"><span data-stu-id="a9539-171">The following example shows the response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="a9539-172">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a9539-172">Next steps</span></span>
<span data-ttu-id="a9539-173"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="a9539-173"></span></span>

<span data-ttu-id="a9539-174">Suchen den Endpunkt gemäß der AutoErmittlung-Prozesses gibt die angeforderte Domäne oder benutzereinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="a9539-174">Finding the endpoint by following the Autodiscover process returns the requested domain or user settings.</span></span> <span data-ttu-id="a9539-175">Informationen zum Treffen einer Anforderung für spezielle Einstellungen finden Sie unter den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="a9539-175">For information about making a request for specific settings, see the following articles:</span></span>
  
- [<span data-ttu-id="a9539-176">Abrufen von domäneneinstellungen aus einem Exchange-server</span><span class="sxs-lookup"><span data-stu-id="a9539-176">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)    
- [<span data-ttu-id="a9539-177">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="a9539-177">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a><span data-ttu-id="a9539-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9539-178">See also</span></span>

- [<span data-ttu-id="a9539-179">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="a9539-179">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="a9539-180">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="a9539-180">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="a9539-181">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="a9539-181">Autodiscover web service reference for Exchange</span></span>](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [<span data-ttu-id="a9539-182">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="a9539-182">EWS reference for Exchange</span></span>](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

