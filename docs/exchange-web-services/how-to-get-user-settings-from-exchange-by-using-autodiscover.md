---
title: Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6d90c305-4802-4e18-8d52-f60349feaa8d
description: Hier erfahren Sie, wie benutzerkonfigurationseinstellungen von einem Exchange-Server durch Verwendung der AutoErmittlung abgerufen.
ms.openlocfilehash: f37de55d6681bcdef381561b166adf209d3919a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756898"
---
# <a name="get-user-settings-from-exchange-by-using-autodiscover"></a><span data-ttu-id="ab517-103">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="ab517-103">Get user settings from Exchange by using Autodiscover</span></span>

<span data-ttu-id="ab517-104">Hier erfahren Sie, wie benutzerkonfigurationseinstellungen von einem Exchange-Server durch Verwendung der AutoErmittlung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ab517-104">Learn how to get user configuration settings from an Exchange server by using Autodiscover.</span></span>
  
<span data-ttu-id="ab517-105">AutoErmittlung vereinfacht Anwendungskonfiguration durch den einfachen Zugriff auf Informationen aus der Benutzerkonfiguration mit nur die e-Mail-Adresse des Benutzers und-Kennwort an.</span><span class="sxs-lookup"><span data-stu-id="ab517-105">Autodiscover simplifies application configuration by providing easy access to user configuration information using only the user's email address and password.</span></span> <span data-ttu-id="ab517-106">Eine [Anzahl von Konfigurationseinstellungen für die Benutzer](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) sind über AutoErmittlung, wie des Benutzers Anzeigename oder externen Webdienst-URL verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab517-106">A [number of user configuration settings](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) are available via Autodiscover, such as the user's display name or external web service URL.</span></span> 
  
<span data-ttu-id="ab517-107">Eines der folgenden Entwicklungstechnologien können Sie benutzereinstellungen aus den AutoErmittlungsdienst abzurufen:</span><span class="sxs-lookup"><span data-stu-id="ab517-107">You can use one of the following development technologies to retrieve user settings from the Autodiscover service:</span></span>
  
- <span data-ttu-id="ab517-108">Der [Erste Schritte mit EWS Managed API-Clientanwendungen](get-started-with-ews-managed-api-client-applications.md)</span><span class="sxs-lookup"><span data-stu-id="ab517-108">The [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md)</span></span>
    
- <span data-ttu-id="ab517-109">Der [AutoErmittlung für SOAP-Webdienst](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab517-109">The [SOAP Autodiscover web service](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)</span></span>
    
- <span data-ttu-id="ab517-110">Der [Webdienst POX AutoErmittlung](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab517-110">The [POX Autodiscover web service](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)</span></span>
    
<span data-ttu-id="ab517-111">Die verwaltete EWS-API stellt eine objektbasierte Schnittstelle für das Abrufen von Benutzereinstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="ab517-111">The EWS Managed API provides an object-based interface for retrieving user settings.</span></span> <span data-ttu-id="ab517-112">Wenn die Clientanwendung verwalteten Code verwendet, wird empfohlen, die verwaltete EWS-API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-112">If your client application uses managed code, we recommend that you use the EWS Managed API.</span></span> <span data-ttu-id="ab517-113">Wenn Sie die EWS Managed API verwenden, bestimmen Sie, ob die Einstellungen, die Sie in der [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx) -Aufzählung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ab517-113">If you are using the EWS Managed API, determine whether the settings that you need are available in the [Microsoft.Exchange.WebServices.Autodiscover.UserSettingName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=EXCHG.80%29.aspx) enumeration.</span></span> <span data-ttu-id="ab517-114">Wenn sie nicht möchten, empfiehlt es sich, die SOAP- oder POX AutoErmittlung-Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-114">If they aren't, you might want to use the SOAP or POX Autodiscover services.</span></span> 
  
<span data-ttu-id="ab517-115">Wenn Sie einen Webdienst verwenden, empfehlen wir, dass Sie den SOAP-AutoErmittlungsdienst verwenden, da es eine umfangreichere Features als POX AutoErmittlungsdienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab517-115">If you are using a web service, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span> <span data-ttu-id="ab517-116">Wenn der SOAP-AutoErmittlungsdienst nicht verfügbar ist, ist der POX AutoErmittlungsdienst eine gute Alternative.</span><span class="sxs-lookup"><span data-stu-id="ab517-116">If the SOAP Autodiscover service isn't available, the POX Autodiscover service is a good alternative.</span></span>
  
## <a name="set-up-to-get-user-settings"></a><span data-ttu-id="ab517-117">Einrichten von benutzereinstellungen abrufen</span><span class="sxs-lookup"><span data-stu-id="ab517-117">Set up to get user settings</span></span>
<span data-ttu-id="ab517-118"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="ab517-118"></span></span>

<span data-ttu-id="ab517-119">Bevor Sie benutzereinstellungen abrufen, indem Sie den AutoErmittlungsdienst, stellen Sie sicher, dass Sie Zugriff auf die folgenden haben:</span><span class="sxs-lookup"><span data-stu-id="ab517-119">Before you get user settings by using the Autodiscover service, make sure that you have access to the following:</span></span>
  
- <span data-ttu-id="ab517-120">Wenn Sie die EWS Managed API oder POX-basierte AutoErmittlungsdienst, Exchange Online, Exchange Online als Teil von Office 365 oder einen Server mit einer Version von Exchange, beginnend mit Exchange 2007 SP1 verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-120">If you are using the EWS Managed API or the POX-based Autodiscover service, Exchange Online, Exchange Online as part of Office 365, or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> 
    
- <span data-ttu-id="ab517-121">Wenn Sie die SOAP-basierte AutoErmittlungsdienst, Exchange Online oder eine Version von Exchange, beginnend mit Exchange 2010 verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-121">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ab517-122">Wenn Sie die EWS Managed API verwenden, müssen Sie unter Umständen [eine Rückrufmethode des Zertifikat-Validierung bereitstellen](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) .</span><span class="sxs-lookup"><span data-stu-id="ab517-122">If you are using the EWS Managed API, you will need to [provide a certificate validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) in some circumstances.</span></span> <span data-ttu-id="ab517-123">Möglicherweise benötigen Sie auch eine Zertifikat Validierung Rückrufmethode mit einigen generierten Proxys Bibliotheken, beispielsweise von Visual Studio erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab517-123">You might also need a certificate validation callback method with some generated proxy libraries, such as those created by Visual Studio.</span></span> 
  
## <a name="get-user-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="ab517-124">Rufen Sie benutzereinstellungen ab, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="ab517-124">Get user settings by using the EWS Managed API</span></span>
<span data-ttu-id="ab517-125"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="ab517-125"></span></span>

<span data-ttu-id="ab517-126">Die [GetUserSettings](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) -Methode können Sie die Konfigurationsinformationen für einen Benutzer abrufen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ab517-126">You can use the [GetUserSettings](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) method to retrieve configuration information for a user, as shown in the following example.</span></span> <span data-ttu-id="ab517-127">In diesem Beispiel können Sie ein Array von benutzereinstellungen zurückzugebenden (aus den verfügbaren in der [UserSettingName](http://msdn.microsoft.com/de-de/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) -Enumeration) angeben, und die Methode vor, Umleitungsantworten vom Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="ab517-127">In this example, you can specify an array of user settings to return (from those available in the [UserSettingName](http://msdn.microsoft.com/de-de/library/exchange/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) enumeration), and the method will follow redirection responses from the Exchange server.</span></span> 
  
```cs
using System;
using System.Net;
using Microsoft.Exchange.WebServices.Autodiscover;
public static GetUserSettingsResponse GetUserSettings(
    AutodiscoverService service,
    string emailAddress,
    int maxHops,
    params UserSettingName[] settings)
{
    Uri url = null;
    GetUserSettingsResponse response = null;
    for (int attempt = 0; attempt < maxHops; attempt++)
    {
        service.Url = url;
        service.EnableScpLookup = (attempt < 2);
        response = service.GetUserSettings(emailAddress, settings);
        if (response.ErrorCode == AutodiscoverErrorCode.RedirectAddress)
        {
            url = new Uri(response.RedirectTarget);
        }
        else if (response.ErrorCode == AutodiscoverErrorCode.RedirectUrl)
        {
            url = new Uri(response.RedirectTarget);
        }
        else
        {
            return response;
        }
    }
    throw new Exception("No suitable Autodiscover endpoint was found.");
}
```

<span data-ttu-id="ab517-128">Sie können jedes Schlüssel/Wert-Paar im Array Einstellungen Benutzer Zugriff auf zurückgegebene Auflistung analysieren.</span><span class="sxs-lookup"><span data-stu-id="ab517-128">You can parse the collection returned to access each key/value pair in the user settings array.</span></span> <span data-ttu-id="ab517-129">Das folgende Beispiel zeigt, wie Sie die einzelnen zurückgegebenen Elemente analysieren und den Namen und Wert der einzelnen Schlüssel-Wert-Paare anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ab517-129">The following example shows how to parse through each returned element and display the name and value of each key/value pair.</span></span>
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
// userresponse is a GetUserSettingsResonse object.
foreach (KeyValuePair<UserSettingName, Object> usersetting in userresponse.Settings)
{
    Console.WriteLine(usersetting.Key.ToString() + ": " + usersetting.Value);
}
```

<span data-ttu-id="ab517-130">Alternativ können Sie den Wert einer bestimmten Einstellung abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab517-130">Alternatively, you can obtain the value of a specific setting.</span></span> <span data-ttu-id="ab517-131">Die Einstellung **UserDisplayName** werden im folgenden Beispiel angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab517-131">In the following example, the **UserDisplayName** setting is to be displayed.</span></span> 
  
```cs
// Display a specific setting, such as UserDisplayName.
Console.WriteLine(userresponse.Settings[UserSettingName.UserDisplayName]);
```

## <a name="get-user-settings-by-using-soap-autodiscover"></a><span data-ttu-id="ab517-132">Abrufen von benutzereinstellungen unter Verwendung von SOAP-AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="ab517-132">Get user settings by using SOAP Autodiscover</span></span>
<span data-ttu-id="ab517-133"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="ab517-133"></span></span>

<span data-ttu-id="ab517-134">Wenn Sie nicht die EWS Managed API verwenden, wird empfohlen, dass Sie den AutoErmittlung SOAP-Webdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-134">If you're not using the EWS Managed API, we recommend that you use the SOAP Autodiscover web service.</span></span> <span data-ttu-id="ab517-135">Verwenden Sie nur den POX AutoErmittlung-Webdienst auf, wenn der AutoErmittlung SOAP-Webdienst treten Fehler auf oder nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab517-135">Only use the POX Autodiscover web service if the SOAP Autodiscover web service fails or is not available.</span></span> 
  
<span data-ttu-id="ab517-136">Wenn Sie benutzereinstellungen erhalten möchten, verwenden Sie die [GetUserSettings-Vorgang (SOAP)](http://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab517-136">To get user settings, use the [GetUserSettings operation (SOAP)](http://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx).</span></span> <span data-ttu-id="ab517-137">Die angeforderten Einstellungen werden als [UserSetting Elemente](http://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab517-137">The requested settings are returned as [UserSetting elements](http://msdn.microsoft.com/library/aac6dc31-edd2-49d7-b845-1df4d77da58c%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="ab517-138">Das folgende Beispiel zeigt eine AutoErmittlung SOAP-Anforderung an benutzereinstellungen vom Server abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ab517-138">The following example shows a SOAP Autodiscover request to get user settings from the server.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>mara@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>PublicFolderServer</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>ExternalMailboxServer</a:Setting>
          <a:Setting>EcpDeliveryReportUrlFragment</a:Setting>
          <a:Setting>EcpPublishingUrlFragment</a:Setting>
          <a:Setting>EcpTextMessagingUrlFragment</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
          <a:Setting>GroupingInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ab517-139">Das folgende Beispiel zeigt die SOAP-Antwort, die vom Server zurückgegeben wird, nachdem die Anforderung vom Client analysiert.</span><span class="sxs-lookup"><span data-stu-id="ab517-139">The following example shows the SOAP response that is returned by the server after it parses the request from the client.</span></span> <span data-ttu-id="ab517-140">Die Antwort enthält nur die Einstellungen, die angefordert werden, sofern sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ab517-140">The response contains only the settings that are requested, if they exist.</span></span>
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
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
                <Name>UserDisplayName</Name>
                <Value>Mara Whitley</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=mara</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>649d50b8-a1ce-4bac-8ace-2321   e463f701</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>15.01.0160.004</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007, Exchange2007_SP1, Exchange2010, Exchange2010_SP1, Exchange2010_SP2, Exchange2013</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>dc.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=microsoft/ou=Exchange Administrative Group 
                  (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=mail.contoso.com/cn=Contoso Private MDB</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>PublicFolderServer</Name>
                <Value>public.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpDeliveryReportUrlFragment</Name>
                <Value>PersonalSettings/DeliveryReport.aspx?exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpTextMessagingUrlFragment</Name>
                <Value>?p=sms/textmessaging.slab&amp;amp;exsvurl=1</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EcpPublishingUrlFragment</Name>
                <Value>customize/calendarpublishing.slab?exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://mail.contoso.com/EWS/Exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalMailboxServer</Name>
                <Value>mail.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>GroupingInformation</Name>
                <Value>CONTOSO-1</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope
```

## <a name="get-user-settings-by-using-pox-autodiscover"></a><span data-ttu-id="ab517-141">Abrufen von benutzereinstellungen mithilfe von POX AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="ab517-141">Get user settings by using POX Autodiscover</span></span>
<span data-ttu-id="ab517-142"><a name="bk_POX"> </a></span><span class="sxs-lookup"><span data-stu-id="ab517-142"></span></span>

<span data-ttu-id="ab517-143">Obwohl es wird empfohlen, dass Sie den AutoErmittlung SOAP-Webdienst verwenden, wird der Webdienst POX AutoErmittlung backup empfohlen für die Fälle, wenn SOAP nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab517-143">Although we recommend that you use the SOAP Autodiscover web service, the POX Autodiscover web service is a good backup option for those times when SOAP isn't available.</span></span> <span data-ttu-id="ab517-144">Beispielsweise Exchange 2007 bietet keine Unterstützung der AutoErmittlung für SOAP-Webdienst, wenn Sie Exchange 2007 abzielen, müssen Sie den Webdienst POX AutoErmittlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab517-144">For example, Exchange 2007 does not support the SOAP Autodiscover web service, so if you are targeting Exchange 2007, you have to use the POX Autodiscover web service.</span></span> <span data-ttu-id="ab517-145">Im Gegensatz zu den AutoErmittlung SOAP-Webdienst ist die spezielle Einstellungen anfordern des AutoErmittlungsdiensts POX nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ab517-145">Unlike the SOAP Autodiscover web service, the POX Autodiscover service does not allow you to request specific settings.</span></span> <span data-ttu-id="ab517-146">Stattdessen gibt der Server eine vollständige Liste der verfügbaren Einstellungen als untergeordnete Elemente des [Protokoll-Element](http://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx)zurück.</span><span class="sxs-lookup"><span data-stu-id="ab517-146">Instead, the server returns a full list of available settings as child elements of the [Protocol element](http://msdn.microsoft.com/library/f77e4d66-6fdd-4999-9339-f7d7f9c86f44%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="ab517-147">Das folgende Beispiel zeigt eine Anforderung POX AutoErmittlung benutzereinstellungen vom Server abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab517-147">The following example shows a POX Autodiscover request to get user settings from the server.</span></span> <span data-ttu-id="ab517-148">Im folgende XML wird über HTTP POST an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="ab517-148">The following XML is sent to the server via an HTTP POST.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>mara@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="ab517-149">Das folgende Beispiel zeigt die POX-Antwort, die vom Server zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab517-149">The following example shows the POX response that is returned by the server.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>Mara Whitley</DisplayName>
      <LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=f5eeabead90d4b6fb51d6379474692cd-Mara</LegacyDN>
      <AutoDiscoverSMTPAddress>mara@contoso.com</AutoDiscoverSMTPAddress>
      <DeploymentId>50817eff-b925-4578-a0db-13bfc635e7a5</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <MicrosoftOnline>False</MicrosoftOnline>
      <Protocol>
        <Type>EXCH</Type>
        <Server>5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</Server>
        <ServerDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com</ServerDN>
        <ServerVersion>73C08204</ServerVersion>
        <MdbDN>/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=5f76be3c-9138-4f66-85e0-21bc23ca35f0@contoso.com/cn=Microsoft Private MDB</MdbDN>
        <PublicFolderServer>public.contoso.com</PublicFolderServer>
        <AD>dc.contoso.com</AD>
        <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
        <EwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EwsUrl>
        <EmwsUrl>https://mail.contoso.com/EWS/Exchange.asmx</EmwsUrl>
        <EcpUrl>https://mail.contoso.com/ecp/</EcpUrl>
        <EcpUrl-um>?rfr=olk&amp;amp;p=customize/voicemail.aspx&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-um>
        <EcpUrl-aggr>?rfr=olk&amp;amp;p=personalsettings/EmailSubscriptions.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-aggr>
        <EcpUrl-mt>PersonalSettings/DeliveryReport.aspx?rfr=olk&amp;amp;exsvurl=1&amp;amp;IsOWA=&amp;lt;IsOWA&amp;gt;&amp;amp;MsgID=&amp;lt;MsgID&amp;gt;&amp;amp;Mbx=&amp;lt;Mbx&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-mt>
        <EcpUrl-ret>?rfr=olk&amp;amp;p=organize/retentionpolicytags.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-ret>
        <EcpUrl-sms>?rfr=olk&amp;amp;p=sms/textmessaging.slab&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-sms>
        <EcpUrl-publish>customize/calendarpublishing.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;FldID=&amp;lt;FldID&amp;gt;&amp;amp;realm=contoso.com</EcpUrl-publish>
        <EcpUrl-photo>PersonalSettings/EditAccount.aspx?rfr=olk&amp;amp;chgPhoto=1&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-photo>
        <EcpUrl-tm>?rfr=olk&amp;amp;ftr=TeamMailbox&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tm>
        <EcpUrl-tmCreating>?rfr=olk&amp;amp;ftr=TeamMailboxCreating&amp;amp;SPUrl=&amp;lt;SPUrl&amp;gt;&amp;amp;Title=&amp;lt;Title&amp;gt;&amp;amp;SPTMAppUrl=&amp;lt;SPTMAppUrl&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmCreating>
        <EcpUrl-tmEditing>?rfr=olk&amp;amp;ftr=TeamMailboxEditing&amp;amp;Id=&amp;lt;Id&amp;gt;&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-tmEditing>
        <EcpUrl-extinstall>Extension/InstalledExtensions.slab?rfr=olk&amp;amp;exsvurl=1&amp;amp;realm=contoso.com</EcpUrl-extinstall>
        <OOFUrl>https://mail.contoso.com/EWS/Exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/EWS/UM2007Legacy.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/c21c7bc2-53b3-4ddc-ad89-1219b486c37c/</OABUrl>
        <ServerExclusiveConnect>off</ServerExclusiveConnect>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>mail.contoso.com</Server>
        <SSL>Off</SSL>
        <AuthPackage>Ntlm</AuthPackage>
        <ServerExclusiveConnect>on</ServerExclusiveConnect>
        <CertPrincipalName>None</CertPrincipalName>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Basic, Fba">https://mail.contoso.com/owa/</OWAUrl>
          <Protocol>
            <Type>EXCH</Type>
            <ASUrl>https://mail.contoso.com/EWS/Exchange.asmx</ASUrl>
          </Protocol>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="next-steps"></a><span data-ttu-id="ab517-150">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ab517-150">Next steps</span></span>
<span data-ttu-id="ab517-151"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="ab517-151"></span></span>

<span data-ttu-id="ab517-152">Nachdem Sie die erforderlichen Konfigurationsschritte Details für Ihre Benutzer vom Server abgerufen haben, können Sie für die Kommunikation mit Exchange um dieselben Berechtigungen wie die Anwendung ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="ab517-152">After you've retrieved the necessary configuration details for your user from the server, you are ready to communicate with Exchange to do the things your application needs to do.</span></span> <span data-ttu-id="ab517-153">Der nächste Schritt hängt wie Sie mit Exchange kommunizieren und was Sie erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="ab517-153">What you do next depends on how you communicate with Exchange and what you want to accomplish.</span></span> <span data-ttu-id="ab517-154">Wenn Sie einige Inspiration benötigen und EWS verwenden, untersuchen Sie möglicherweise einige Vorschläge für die [Exchange-101-Codebeispiele](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c) .</span><span class="sxs-lookup"><span data-stu-id="ab517-154">If you need some inspiration, and you're using EWS, you might explore the [Exchange 101 code samples](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c) for some ideas.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab517-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab517-155">See also</span></span>


- [<span data-ttu-id="ab517-156">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="ab517-156">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="ab517-157">Exchange-Webdienste (EWS) Managed-API</span><span class="sxs-lookup"><span data-stu-id="ab517-157">Exchange Web Services (EWS) Managed API</span></span>](http://msdn.microsoft.com/de-de/library/exchange/jj220535%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="ab517-158">SOAP-Webdienst-Verweis für die AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="ab517-158">SOAP Autodiscover web service reference for Exchange</span></span>](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)
    
- [<span data-ttu-id="ab517-159">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="ab517-159">POX Autodiscover web service reference for Exchange</span></span>](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)
    

