---
title: Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um Ihre Clientanwendung an den richtigen Exchange-Server weiterzuleiten.
localization_priority: Priority
ms.openlocfilehash: c1895fa0d2cce489467a726614e9457052624ef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527593"
---
# <a name="use-autodiscover-to-find-connection-points"></a><span data-ttu-id="c5fd9-103">Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten</span><span class="sxs-lookup"><span data-stu-id="c5fd9-103">Use Autodiscover to find connection points</span></span>

<span data-ttu-id="c5fd9-104">Erfahren Sie, wie Sie den AutoErmittlungsdienst verwenden, um Ihre Clientanwendung an den richtigen Exchange-Server weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-104">Find out how to use the Autodiscover service to direct your client application to the correct Exchange server.</span></span>
  
<span data-ttu-id="c5fd9-105">Der Exchange-AutoErmittlungsdienst stellt Ihrer Clientanwendung Konfigurationseinstellungen für e-Mail-Konten zur Verfügung, die auf Exchange Online gehostet werden, Exchange Online im Rahmen von Office 365 oder einem Exchange-Server, auf dem eine Exchange-Version mit Exchange 2013 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-105">The Exchange Autodiscover service provides your client application with configuration settings for email accounts that are hosted on Exchange Online, Exchange Online as part of Office 365, or an Exchange server running a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="c5fd9-106">Der AutoErmittlungsdienst ist ein Webdienst, der Konfigurationseinstellungen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-106">The Autodiscover service is a web service that provides configuration settings.</span></span> <span data-ttu-id="c5fd9-107">Der AutoErmittlungsdienst ist ein Webdienst, der Exchange Server-Konfigurationsinformationen für Ihre Clientanwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-107">The Autodiscover service is a web service that provides Exchange server configuration information to your client application.</span></span> <span data-ttu-id="c5fd9-108">Client Anwendungen verwenden AutoErmittlung, um den Endpunkt des AutoErmittlungsdiensts für ein bestimmtes Postfach zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-108">Client applications use Autodiscover to determine the endpoint of the Autodiscover service for a specific mailbox.</span></span> <span data-ttu-id="c5fd9-109">In diesem Artikel wird erläutert, wie Sie die Antworten von einem Exchange-Server zum Ermitteln des richtigen Endpunkts befolgten.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-109">This article explains how to follow the responses from an Exchange server to find the correct endpoint.</span></span> 
  
<span data-ttu-id="c5fd9-110">Informationen zum Abrufen von Konfigurationseinstellungen für e-Mail-Adressen finden Sie unter [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) und [Abrufen von Domäneneinstellungen von einem Exchange-Server](how-to-get-domain-settings-from-an-exchange-server.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-110">For information about how to get email address configuration settings, see [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and [Get domain settings from an Exchange server](how-to-get-domain-settings-from-an-exchange-server.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c5fd9-111">Der Vorgang zum Suchen des richtigen Endpunkts ist Teil der Anforderung für Benutzer-oder Domäneneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-111">The process for finding the correct endpoint is part of the request for user or domain settings.</span></span> <span data-ttu-id="c5fd9-112">Der AutoErmittlungsdienst verwendet eine Reihe von Umleitungsantworten, um die Clientanwendung an den richtigen Endpunkt für eine e-Mail-Adresse zu senden.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-112">The Autodiscover service uses a series of redirect responses to send the client application to the correct endpoint for an email address.</span></span> 
  
<span data-ttu-id="c5fd9-113">Sie können eine der folgenden Exchange-Entwicklungstechnologien für den Zugriff auf den AutoErmittlungsdienst verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5fd9-113">You can use one of the following Exchange development technologies to access the Autodiscover service:</span></span>

- <span data-ttu-id="c5fd9-114">Die verwaltete API der Exchange-Webdienste (Exchange Web Services, EWS)</span><span class="sxs-lookup"><span data-stu-id="c5fd9-114">The Exchange Web Services (EWS) Managed API</span></span>
    
- <span data-ttu-id="c5fd9-115">EWS</span><span class="sxs-lookup"><span data-stu-id="c5fd9-115">EWS</span></span>
    
<span data-ttu-id="c5fd9-116">Bei Verwendung von EWS können Sie die folgenden Methoden zum Abrufen von Benutzereinstellungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5fd9-116">If you are using EWS, you can use the following methods to retrieve user settings:</span></span>
    
- <span data-ttu-id="c5fd9-117">Den SOAP-basierten AutoErmittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="c5fd9-117">The SOAP-based Autodiscover service</span></span>
    
- <span data-ttu-id="c5fd9-118">Den XML-AutoErmittlungsdienst (POX)</span><span class="sxs-lookup"><span data-stu-id="c5fd9-118">The XML (POX) Autodiscover service</span></span>
    
- <span data-ttu-id="c5fd9-119">Einen automatisch vom SOAP- oder XML-AutoErmittlungdienst generierten Proxy</span><span class="sxs-lookup"><span data-stu-id="c5fd9-119">An autogenerated proxy generated from the SOAP or XML Autodiscover service</span></span>
    
<span data-ttu-id="c5fd9-120">Weitere Informationen zu diesen Methoden finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-120">For more information about these methods, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span>

<span data-ttu-id="c5fd9-121">Weitere Informationen zu diesen Exchange-Entwicklungstechnologien finden Sie unter [Explore the verwaltete EWS-API, EWS, and Webservices in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-121">For more information about these Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span> 

<span data-ttu-id="c5fd9-p103">Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit. Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden. Die verwaltete EWS-API-Schnittstelle ist besser für ein einfaches Objektmodell optimiert als der typische automatisch generierte Webdienstproxy.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-p103">The EWS Managed API provides an object-based interface for retrieving user settings. If your client application uses managed code, we recommend that you use the EWS Managed API. The EWS Managed API interface is better optimized for a simple object model than the typical autogenerated web service proxy.</span></span> 
  
<span data-ttu-id="c5fd9-125">Bei Verwendung von EWS empfehlen wir die Verwendung des SOAP-AutoErmittlungsdiensts, da dieser eine umfassendere Sammlung von Funktionen als der POX-AutoErmittlungsdienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-125">If you are using EWS, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span>
  
## <a name="prerequisites-for-finding-an-endpoint"></a><span data-ttu-id="c5fd9-126">Voraussetzungen für die Suche nach einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c5fd9-126">Prerequisites for finding an endpoint</span></span>
<span data-ttu-id="c5fd9-127"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="c5fd9-127"><a name="bk_Prereq"> </a></span></span>

<span data-ttu-id="c5fd9-128">Bevor Sie eine Clientanwendung erstellen können, die den AutoErmittlungsdienst verwendet, benötigen Sie Zugriff auf Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c5fd9-128">Before you can create a client application that uses the Autodiscover service, you need to have access to the following:</span></span>
  
- <span data-ttu-id="c5fd9-129">Exchange Online oder ein Server, auf dem eine Version von Exchange mit Exchange 2007 SP1 gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-129">Exchange Online or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> <span data-ttu-id="c5fd9-130">Wenn Sie den SOAP-basierten AutoErmittlungsdienst verwenden: Exchange Online oder eine Version von Exchange ab Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="c5fd9-130">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
- <span data-ttu-id="c5fd9-p105">Einen Exchange-Server, der Verbindungen von Ihrer Clientanwendung akzeptiert. Informationen zum Konfigurieren des Exchange-Servers finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-p105">An Exchange server that is configured to accept connections from your client application. For information about how to configure your Exchange server, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
- <span data-ttu-id="c5fd9-p106">Ein Konto, das berechtigt ist, EWS zu verwenden. Informationen zum Konfigurieren eines Kontos finden Sie unter [Steuern des Clientanwendungszugriffs auf EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-p106">An account that is authorized to use EWS. For information about how to configure an account, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="c5fd9-135">Wenn Sie die verwaltete EWS-API verwenden, müssen Sie in einigen Fällen einen Zertifikatüberprüfungsrückruf bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-135">If you are using the EWS Managed API, you must provide a certificate validation callback in some circumstances.</span></span> <span data-ttu-id="c5fd9-136">Auch bei einigen generierten Proxybibliotheken, wie den von Visual Studio erstellten, benötigen Sie möglicherweise einen Zertifikatüberprüfungsrückruf.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-136">You may also need a certificate validation callback with some generated proxy libraries, such as those created by Visual Studio.</span></span> <span data-ttu-id="c5fd9-137">Weitere Informationen finden Sie unter [Überprüfen eines Serverzertifikats für die verwaltete EWS-API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-137">For more information, see [Validate a server certificate for the EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> 
  
### <a name="core-concepts-for-finding-an-endpoint"></a><span data-ttu-id="c5fd9-138">Kernkonzepte für die Suche nach einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c5fd9-138">Core concepts for finding an endpoint</span></span>
<span data-ttu-id="c5fd9-139"><a name="bk_Core"> </a></span><span class="sxs-lookup"><span data-stu-id="c5fd9-139"><a name="bk_Core"> </a></span></span>

<span data-ttu-id="c5fd9-140">Bevor Sie die AutoErmittlung zum Auffinden eines Endpunkts verwenden, sollten Sie mit den in der folgenden Tabelle aufgelisteten Konzepten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-140">Before you use Autodiscover to find an endpoint, you should be familiar with the concepts listed in the following table.</span></span>
  
|<span data-ttu-id="c5fd9-141">**Konzept**</span><span class="sxs-lookup"><span data-stu-id="c5fd9-141">**Concept**</span></span>|<span data-ttu-id="c5fd9-142">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5fd9-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5fd9-143">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="c5fd9-143">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="c5fd9-144">Bietet eine Übersicht über die Funktionsweise des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-144">Provides an overview of how the Autodiscover service works.</span></span>  <br/> |
   
<span data-ttu-id="c5fd9-145">Wenn Sie die verwaltete EWS-API benutzen, verwenden Sie die Klasse [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) im Namespace [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx), um Ihre Verbindungen mit EWS zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-145">If you are using the EWS Managed API, you use the [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx) namespace to manage your connection to EWS.</span></span> <span data-ttu-id="c5fd9-146">Um die verwaltete EWS-API Codebeispiele in diesem Artikel zu verwenden, müssen Sie in Ihrem Code auf die folgenden Namespaces verweisen:</span><span class="sxs-lookup"><span data-stu-id="c5fd9-146">To use the EWS Managed API code samples in this article, you need to reference the following namespaces in your code:</span></span> 
  
- <span data-ttu-id="c5fd9-147">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="c5fd9-147">**System.Net**</span></span>
    
- <span data-ttu-id="c5fd9-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span><span class="sxs-lookup"><span data-stu-id="c5fd9-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span></span>
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a><span data-ttu-id="c5fd9-149">Suchen des richtigen Endpunkts mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="c5fd9-149">Find the correct endpoint by using the EWS Managed API</span></span>
<span data-ttu-id="c5fd9-150"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="c5fd9-150"><a name="bk_Managed"> </a></span></span>

<span data-ttu-id="c5fd9-151">Wenn Sie die verwaltete EWS-API verwenden, werden Aufrufe des AutoErmittlungsdiensts von der **Datei "ExchangeService** -Klasse verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-151">If you are using the EWS Managed API, calls to the Autodiscover service are handled by the **ExchangeService** class.</span></span> <span data-ttu-id="c5fd9-152">Um den richtigen Endpunkt für ein e-Mail-Konto zu ermitteln, rufen Sie die **AutodiscoverUrl** -Methode für ein **[Datei "ExchangeService]** -Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-152">To determine the correct endpoint for an email account, you call the **AutodiscoverUrl** method on an **[ExchangeService]** object.</span></span> <span data-ttu-id="c5fd9-153">Im folgenden Codebeispiel wird gezeigt, wie der EWS-Webdienstendpunkt für eine e-Mail-Adresse auf der Exchange. asmx-Datei auf dem richtigen Client Zugriffsserver mithilfe der verwaltete EWS-API festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-153">The following code example shows how to set the EWS web service endpoint for an email address to the Exchange.asmx file on the correct Client Access server by using the EWS Managed API.</span></span> 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a><span data-ttu-id="c5fd9-154">Suchen des richtigen Endpunkts mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="c5fd9-154">Find the correct endpoint by using EWS</span></span>
<span data-ttu-id="c5fd9-155"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="c5fd9-155"><a name="bk_SOAP"> </a></span></span>

<span data-ttu-id="c5fd9-156">Der SOAP-AutoErmittlungsdienst verwendet möglicherweise eine Reihe von Anforderungen und Antworten, um Ihre Anwendung an den richtigen Endpunkt für EWS weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-156">The SOAP Autodiscover service may use a series of requests and responses to direct your application to the correct endpoint for EWS.</span></span> <span data-ttu-id="c5fd9-157">Informationen zum Prozess zum Ermitteln des richtigen Endpunkts für ein e-Mail-Konto finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-157">For information about the process for determining the correct endpoint for an email account, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> <span data-ttu-id="c5fd9-158">Die folgenden XML-Beispiele zeigen die Reihe von Anforderungen und Antworten, die Sie bei der Suche nach dem richtigen Endpunkt für eine SOAP-Auto Ermittlungsanforderung erwarten können.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-158">The following XML examples show the series of requests and responses that you can expect when making a SOAP Autodiscover request to find the correct endpoint.</span></span>
  
### <a name="soap-autodiscover-endpoint-request"></a><span data-ttu-id="c5fd9-159">SOAP-Auto ermittlungsendpunkt-Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5fd9-159">SOAP Autodiscover endpoint request</span></span>

<span data-ttu-id="c5fd9-160">Das folgende Beispiel zeigt eine XML-Anforderung, die an den AutoErmittlungsdienst gesendet wird, um den richtigen Endpunkt zu finden.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-160">The following example shows an XML request that is sent to the Autodiscover service to find the correct endpoint.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

### <a name="soap-autodiscover-redirection-response"></a><span data-ttu-id="c5fd9-161">SOAP-AutoErmittlung-Umleitungsantwort</span><span class="sxs-lookup"><span data-stu-id="c5fd9-161">SOAP Autodiscover redirection response</span></span>

<span data-ttu-id="c5fd9-162">Der AutoErmittlungsdienst antwortet möglicherweise mit einer von zwei Umleitungsantworten: einer HTTP 302-Umleitung oder einer SOAP-Umleitungsantwort.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-162">The Autodiscover service may respond with one of two redirection responses: an HTTP 302 redirect, or a SOAP redirection response.</span></span> <span data-ttu-id="c5fd9-163">Wenn die Antwort vom Exchange-Server eine HTTP 302-Umleitung ist, sollte die Clientanwendung überprüfen, ob die Umleitungsadresse akzeptabel ist, und dann die Umleitungsantwort verfolgen.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-163">If the response from the Exchange server is an HTTP 302 redirect, the client application should validate that the redirection address is acceptable and then follow the redirection response.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c5fd9-164">Kriterien für die Validierung einer Umleitungsantwort finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="c5fd9-164">For criteria for validating a redirection response, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> 
  
<span data-ttu-id="c5fd9-165">Wenn der AutoErmittlungsdienst eine Umleitungsantwort zurückgibt, die durch das [errorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **User Response** -Elements angegeben wird, sollte Ihre Clientanwendung das **RedirectTarget** -Element verwenden, um eine neue Einstellungs Anforderung zu erstellen, die an den in der Umleitungsantwort angegebenen Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-165">If the Autodiscover service returns a redirection response, indicated by the [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element, your client application should use the **RedirectTarget** element to construct a new settings request that is sent to the server specified in the redirection response.</span></span> <span data-ttu-id="c5fd9-166">Das folgende Beispiel zeigt eine Umleitungsantwort vom Server.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-166">The following example shows a redirection response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="c5fd9-167">Nach einer Umleitung verwendet der Client die Umleitungs-URL, um eine weitere Anforderung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-167">After a redirection, the client uses the redirection URL to prepare another request.</span></span> <span data-ttu-id="c5fd9-168">Der folgende Code zeigt ein Beispiel für die Anforderung, die Sie aus der Umleitungsantwort erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-168">The following code shows an example of the request that you create from the redirection response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="c5fd9-169">Wenn die Clientanwendung an den richtigen Endpunkt für den AutoErmittlungsdienst umgeleitet wurde, sendet der Server eine Antwort, wobei das [errorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) -Element des **User Response** -Elements auf **noError** festgelegt und die angeforderten Benutzereinstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-169">When the client application has been directed to the correct endpoint for the Autodiscover service, the server will send a response with the [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element set to **NoError** and containing the requested user settings.</span></span> <span data-ttu-id="c5fd9-170">Nur die angeforderten Benutzereinstellungen **InternalEwsUrl** und **ExternalEwsUrl**werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-170">Only the requested user settings, **InternalEwsUrl** and **ExternalEwsUrl**, are returned.</span></span> <span data-ttu-id="c5fd9-171">Das folgende Beispiel zeigt die Antwort vom Server.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-171">The following example shows the response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

## <a name="next-steps"></a><span data-ttu-id="c5fd9-172">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c5fd9-172">Next steps</span></span>
<span data-ttu-id="c5fd9-173"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="c5fd9-173"><a name="bk_Next"> </a></span></span>

<span data-ttu-id="c5fd9-174">Durchsuchen des Endpunkts nach dem Auto Ermittlungsprozess werden die angeforderten Domänen-oder Benutzereinstellungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-174">Finding the endpoint by following the Autodiscover process returns the requested domain or user settings.</span></span> <span data-ttu-id="c5fd9-175">Informationen zum Erstellen einer Anforderung für bestimmte Einstellungen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="c5fd9-175">For information about making a request for specific settings, see the following articles:</span></span>
  
- [<span data-ttu-id="c5fd9-176">Abrufen von Domäneneinstellungen von einem Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="c5fd9-176">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)    
- [<span data-ttu-id="c5fd9-177">Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="c5fd9-177">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a><span data-ttu-id="c5fd9-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5fd9-178">See also</span></span>

- [<span data-ttu-id="c5fd9-179">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c5fd9-179">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="c5fd9-180">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="c5fd9-180">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="c5fd9-181">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="c5fd9-181">Autodiscover web service reference for Exchange</span></span>](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [<span data-ttu-id="c5fd9-182">EWS-Referenz für Exchange</span><span class="sxs-lookup"><span data-stu-id="c5fd9-182">EWS reference for Exchange</span></span>](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

