---
title: Weiterleitung von Anforderungen für Öffentliche Ordner-Hierarchie
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Alle Anfragen für Informationen zu öffentlichen Ordnern, die Kenntnisse in der Hierarchie Öffentlicher Ordner wie verschieben, aktualisieren, löschen oder Suchen nach öffentlichen Ordnern erfordern müssen an das Postfach für die Hierarchie von Öffentliche Ordner für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die X-AnchorMailbox und X-PublicFolderMailbox-Header auf bestimmte Werte, die von den AutoErmittlungsdienst festgelegt.
ms.openlocfilehash: 983431864729edbb040a7206dae416d10bfb2b7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757000"
---
# <a name="route-public-folder-hierarchy-requests"></a><span data-ttu-id="080df-104">Weiterleitung von Anforderungen für Öffentliche Ordner-Hierarchie</span><span class="sxs-lookup"><span data-stu-id="080df-104">Route public folder hierarchy requests</span></span>

<span data-ttu-id="080df-105">Alle Anfragen für Informationen zu öffentlichen Ordnern, die Kenntnisse in der Hierarchie Öffentlicher Ordner wie verschieben, aktualisieren, löschen oder Suchen nach öffentlichen Ordnern erfordern müssen an das Postfach für die Hierarchie von Öffentliche Ordner für den angegebenen Benutzer weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="080df-105">All requests for public folder information that require knowledge of the public folder hierarchy, such as moving, updating, deleting, or finding public folders, need to be routed to the default public folder hierarchy mailbox for the given user.</span></span> <span data-ttu-id="080df-106">Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header auf bestimmte Werte, die von den AutoErmittlungsdienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="080df-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values returned by the Autodiscover service.</span></span> 
  
<span data-ttu-id="080df-107">**Übersicht über Öffentliche Ordner**</span><span class="sxs-lookup"><span data-stu-id="080df-107">**Overview of public folders**</span></span>

|<span data-ttu-id="080df-108">Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="080df-108">Header</span></span>|<span data-ttu-id="080df-109">Was muss ich?</span><span class="sxs-lookup"><span data-stu-id="080df-109">What do I need?</span></span>|<span data-ttu-id="080df-110">Wie erhalte ich es?</span><span class="sxs-lookup"><span data-stu-id="080df-110">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="080df-111">**X-AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="080df-111">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="080df-112">Der Wert der [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) aus [GetUserSettings](http://msdn.microsoft.com/en-us/library/office/dd877096%28v=exchg.150%29.aspx) AutoErmittlung SOAP-Antwort, die den Wert der **X-AnchorMailbox** Kopfzeile wird.</span><span class="sxs-lookup"><span data-stu-id="080df-112">The [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) value from a [GetUserSettings](http://msdn.microsoft.com/en-us/library/office/dd877096%28v=exchg.150%29.aspx) Autodiscover SOAP response, which becomes the value of the **X-AnchorMailbox** header.</span></span><br/><br/> <span data-ttu-id="080df-113">![ERLEDIGEN](media/Ex15_PF_PFH_Anchor.png)</span><span class="sxs-lookup"><span data-stu-id="080df-113">![TODO](media/Ex15_PF_PFH_Anchor.png)</span></span>| <span data-ttu-id="080df-114">1. senden Sie eine **GetUserSetting** -Anforderung mit der SMTP-Adresse für das Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="080df-114">1. Send a **GetUserSetting** request with the SMTP address for the user's mailbox.</span></span><br/><br/><span data-ttu-id="080df-115">2. Zwischenspeichern des Werts des **PublicFolderInformation** -Elements, der der AutoErmittlungsdienst zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="080df-115">2. Cache the value of the **PublicFolderInformation** element that the Autodiscover service returns.</span></span> <span data-ttu-id="080df-116">Dies kann eine zwischengespeicherte aus einem laufenden Anruf AutoErmittlung in Ihrem Code oder ein neuer [EWS Managed API GetUserSettings anrufen](#bk_getpfinfoewsma) oder eine [GetUserSettings SOAP-Anforderung](#bk_getpfinfoews)sein.</span><span class="sxs-lookup"><span data-stu-id="080df-116">This can be a cached from an existing Autodiscover call in your code, or a new [EWS Managed API GetUserSettings call](#bk_getpfinfoewsma) or a [GetUserSettings SOAP request](#bk_getpfinfoews).</span></span>  <br/><br/><span data-ttu-id="080df-117">3. verwenden Sie das **PublicFolderInformation** -Element zum Auffüllen des Werts der **X-AnchorMailbox** Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="080df-117">3. Use the **PublicFolderInformation** element to populate the value of the **X-AnchorMailbox** header.</span></span> <span data-ttu-id="080df-118">Der Wert des **PublicFolderInformation** -Elements ist eine SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="080df-118">The value of the **PublicFolderInformation** element is an SMTP address.</span></span>  <br/> |
|<span data-ttu-id="080df-119">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="080df-119">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="080df-120">Der Wert der [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) aus einer [POX AutoErmittlung-Antwort](http://msdn.microsoft.com/en-us/library/bb204082%28v=exchg.150%29.aspx), die den Wert der **X-PublicFolderMailbox** Kopfzeile wird.</span><span class="sxs-lookup"><span data-stu-id="080df-120">The [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) value from a [POX Autodiscover response](http://msdn.microsoft.com/en-us/library/bb204082%28v=exchg.150%29.aspx), which becomes the value of the **X-PublicFolderMailbox** header.</span></span><br/><br/> <span data-ttu-id="080df-121">![ERLEDIGEN](media/Ex15_PF_PFH_PFMailbox.png)</span><span class="sxs-lookup"><span data-stu-id="080df-121">![TODO](media/Ex15_PF_PFH_PFMailbox.png)</span></span>|<span data-ttu-id="080df-122">1. [Aufrufen der AutoErmittlung POX](#bk_makeautodrequest) -Dienst mithilfe von der **X-AnchorMailbox** e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="080df-122">1. [Call the POX Autodiscover](#bk_makeautodrequest) service using the **X-AnchorMailbox** email address.</span></span>  <br/><br/><span data-ttu-id="080df-123">2. verwenden Sie das **Server** -Element, das den AutoErmittlungsdienst zurückgegebene zum Auffüllen des Werts der **X-PublicFolderMailbox** Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="080df-123">2. Use the **Server** element returned by the Autodiscover service to populate the value of the **X-PublicFolderMailbox** header.</span></span> <span data-ttu-id="080df-124">Der Wert der **X-PublicFolderMailbox** ist eine SMTP-Adresse, in dem der Benutzername ist eine GUID.</span><span class="sxs-lookup"><span data-stu-id="080df-124">The value of the **X-PublicFolderMailbox** is an SMTP address where the username is a GUID.</span></span>  <br/> |

<br/>

<span data-ttu-id="080df-125">Nachdem Sie die Werte für die Kopfzeile festgelegt haben, können Sie diese, [Wenn Sie Öffentliche Ordner-Hierarchie Anforderungen vornehmen](#bk_setheadervalues).</span><span class="sxs-lookup"><span data-stu-id="080df-125">After you have determined the header values, include them [when you make public folder hierarchy requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="080df-126">Die Schritte in diesem Artikel sind spezifisch für Öffentliche Ordner-Hierarchie Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="080df-126">The steps in this article are specific to public folder hierarchy requests.</span></span> <span data-ttu-id="080df-127">Um festzustellen, ob es sich bei Ihrer Anforderung einer Hierarchie Öffentlicher Ordner oder Content Anforderung ist, finden Sie unter [Routing für Öffentliche Ordner-Anfragen](public-folder-access-with-ews-in-exchange.md#bk_routing).</span><span class="sxs-lookup"><span data-stu-id="080df-127">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a><span data-ttu-id="080df-128">Bestimmen Sie den Wert der X-AnchorMailbox Kopfzeile mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="080df-128">Determine the value of the X-AnchorMailbox header by using the EWS Managed API</span></span>
<span data-ttu-id="080df-129"><a name="bk_getpfinfoewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="080df-129"></span></span>

<span data-ttu-id="080df-130">Rufen Sie den Wert [PublicFolderInformation (POX)](http://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mithilfe der EWS Managed API können Sie Zwischenspeichern Sie den Wert des **PublicFolderInformation** -Elements, der ein laufenden Anruf mit dem AutoErmittlungsdienst zurückgibt, oder stellen einen neuen Anruf aus.</span><span class="sxs-lookup"><span data-stu-id="080df-130">To retrieve the [PublicFolderInformation (POX)](http://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) value by using the EWS Managed API, you can either cache the value of the **PublicFolderInformation** element that an existing call to the Autodiscover service returns, or make a new call.</span></span> 
  
<span data-ttu-id="080df-131">Wenn Sie einen neuen Anruf tätigen, können Sie [Abrufen benutzereinstellungen mithilfe der EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[benutzereinstellungen mithilfe der EWS Managed API erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) , auf Ihr Code, und rufen Sie anschließend die **GetUserSettings** Beispiel-Methode mit den folgenden Code, die abruft nur der Wert des **PublicFolderInformation** -Elements.</span><span class="sxs-lookup"><span data-stu-id="080df-131">If you're making a new call, you can [Get user settings by using the EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[Get user settings by using the EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) to your code, and then call the **GetUserSettings** sample method by using the following code, which retrieves only the value of the **PublicFolderInformation** element.</span></span> <span data-ttu-id="080df-132">Enthalten Sie die SMTP-Adresse des Postfachbenutzers als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="080df-132">Include the SMTP address of the mailbox user as an input parameter.</span></span> 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

<span data-ttu-id="080df-133">Nach der Ausführung des Codes wird die folgende Informationen in der Konsole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="080df-133">After running the code, the following information is displayed on the console:</span></span>
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

<span data-ttu-id="080df-134">Nun, da Sie den Wert **PublicFolderInformation** haben, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Öffentliche Ordner-Hierarchie Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="080df-134">Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a><span data-ttu-id="080df-135">Bestimmen Sie den Wert der X-AnchorMailbox Kopfzeile unter Verwendung von SOAP</span><span class="sxs-lookup"><span data-stu-id="080df-135">Determine the value of the X-AnchorMailbox header using SOAP</span></span>
<span data-ttu-id="080df-136"><a name="bk_getpfinfoews"> </a></span><span class="sxs-lookup"><span data-stu-id="080df-136"></span></span>

<span data-ttu-id="080df-137">Im folgenden Codebeispiel wird veranschaulicht, wie den **PublicFolderInformation** -Wert mit der [GetUserSettings](http://msdn.microsoft.com/en-us/library/dd877096%28v=exchg.150%29.aspx) SOAP-Operation abgerufen.</span><span class="sxs-lookup"><span data-stu-id="080df-137">The following code example shows how to retrieve the **PublicFolderInformation** value by using the [GetUserSettings](http://msdn.microsoft.com/en-us/library/dd877096%28v=exchg.150%29.aspx) SOAP operation.</span></span> <span data-ttu-id="080df-138">Der Postfachbenutzer im [Postfach](http://msdn.microsoft.com/en-us/library/dd877076%28v=exchg.150%29.aspx) -Element angegeben ist, und das Element [RequestedSettings](http://msdn.microsoft.com/en-us/library/office/dd877107%28v=exchg.150%29.aspx) beschränkt die Antwort auf den Wert [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="080df-138">The mailbox user is specified in the [Mailbox](http://msdn.microsoft.com/en-us/library/dd877076%28v=exchg.150%29.aspx) element, and the [RequestedSettings](http://msdn.microsoft.com/en-us/library/office/dd877107%28v=exchg.150%29.aspx) element limits the response to the [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) value.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>sonyaf@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>PublicFolderInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="080df-139">Die Antwort enthält den Wert **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="080df-139">The response includes the **PublicFolderInformation** value.</span></span> 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

<span data-ttu-id="080df-140">Nun, da Sie den Wert **PublicFolderInformation** haben, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Öffentliche Ordner-Hierarchie Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="080df-140">Now that you have the **PublicFolderInformation** value, include it as the value for the X-AnchorMailbox header in all public folder hierarchy requests.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a><span data-ttu-id="080df-141">Stellen Sie eine autoermittlungsanforderung an den Wert X PublicFolderInformation zu bestimmen</span><span class="sxs-lookup"><span data-stu-id="080df-141">Make an Autodiscover request to determine the X-PublicFolderInformation value</span></span>
<span data-ttu-id="080df-142"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="080df-142"></span></span>

<span data-ttu-id="080df-143">Stellen Sie eine autoermittlungsanforderung für die mithilfe der **PublicFolderInformation** SMTP-Adresse, die jetzt als der Wert von **X-AnchorMailbox** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="080df-143">Make an Autodiscover request by using the **PublicFolderInformation** SMTP address, which is now being used as the **X-AnchorMailbox** value.</span></span> <span data-ttu-id="080df-144">Verwendung der [Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Codebeispiel den AutoErmittlungsdienst aufgerufen, da es die AutoErmittlung für Sie vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="080df-144">Use the [Exchange 2013: Get user settings with Autodiscover](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="080df-145">In diesem Codebeispiel verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenargumente, um den AutoErmittlungsdienst POX für die SMTP-Adresse **PublicFolderInformation** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="080df-145">This code sample uses the command line arguments listed in the following table to call the POX Autodiscover service on the **PublicFolderInformation** SMTP address.</span></span> 
  
|<span data-ttu-id="080df-146">**Befehlszeilenargument**</span><span class="sxs-lookup"><span data-stu-id="080df-146">**Command-line argument**</span></span>|<span data-ttu-id="080df-147">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="080df-147">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="080df-148">emailAddress</span><span class="sxs-lookup"><span data-stu-id="080df-148">emailAddress</span></span>  <br/> |<span data-ttu-id="080df-149">Die **PublicFolderInformation** SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="080df-149">The **PublicFolderInformation** SMTP address.</span></span>  <br/> |
|<span data-ttu-id="080df-150">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="080df-150">-skipSOAP</span></span>  <br/> | <span data-ttu-id="080df-151">Verwenden Sie für dieses Szenario POX AutoErmittlungs-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="080df-151">Use POX Autodiscover requests for this scenario.</span></span>  <br/> |
|<span data-ttu-id="080df-152">-Auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="080df-152">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="080df-153">Das des Postfachbenutzers e-Mail-Adresse, die für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="080df-153">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="080df-154">Sie werden aufgefordert, die beim Ausführen des Beispiels den Postfachbenutzer Kennwort eingeben.</span><span class="sxs-lookup"><span data-stu-id="080df-154">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="080df-155">Wenn SharedPublicFolder@contoso.com die SMTP-Adresse des **PublicFolderInformation** -Elements ist und sonyaf@contoso.com den Postfachbenutzer ist, sollte die Befehlszeilenargumente folgendermaßen aussehen.</span><span class="sxs-lookup"><span data-stu-id="080df-155">For example, when SharedPublicFolder@contoso.com is the SMTP address of the **PublicFolderInformation** element, and sonyaf@contoso.com is the mailbox user, the command-line arguments should look like this.</span></span> 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="080df-156">Beim Ausführen der **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel die letzte AutoErmittlung Antwort erfolgreich und umfassen sollten alle für die Benutzer die Postfach-GUID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="080df-156">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="080df-157">Der [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) -Wert, der das [Protokoll](http://msdn.microsoft.com/en-us/library/bb204278%28v=exchg.150%29.aspx)für die EXCH[Typ](http://msdn.microsoft.com/en-us/library/office/bb204223%28v=exchg.150%29.aspx) -Element zugeordnet ist die Kopfzeilenwert **X-PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="080df-157">The [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) value associated with the EXCH [Protocol](http://msdn.microsoft.com/en-us/library/bb204278%28v=exchg.150%29.aspx)[Type](http://msdn.microsoft.com/en-us/library/office/bb204223%28v=exchg.150%29.aspx) element is the **X-PublicFolderInformation** header value.</span></span> 
  
```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

<span data-ttu-id="080df-158">Alternativ, wenn Sie nicht möchten, verwenden Sie die **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel können Sie den **Server** -Wert durch [eine Liste von Endpunkten AutoErmittlung generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und senden Sie dann die folgenden POX AutoErmittlung abrufen Fordern Sie an, dass jede URL, bis Sie eine erfolgreiche Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="080df-158">Alternatively, if you do not want to use the **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **Server** value by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span> <span data-ttu-id="080df-159">SharedPublicFolder@contoso.com ist der Wert der **X-PublicFolderMailbox** Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="080df-159">SharedPublicFolder@contoso.com is the value of the **X-PublicFolderMailbox** header.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="080df-160">Weitere Informationen zu den AutoErmittlung-Prozesses finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [generieren eine Liste von AutoErmittlung-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="080df-160">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="080df-161">Legen Sie die Werte der X-AnchorMailbox und X-PublicFolderMailbox-Header</span><span class="sxs-lookup"><span data-stu-id="080df-161">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="080df-162"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="080df-162"></span></span>

<span data-ttu-id="080df-163">Verwenden den Wert der **PublicFolderInformation** SMTP-Adresse in [den Wert der X-AnchorMailbox Kopfzeile mithilfe der EWS Managed API bestimmen](#bk_getpfinfoewsma) oder [bestimmen den Wert der Verwendung von SOAP X AnchorMailbox Kopfzeile](#bk_getpfinfoews) und die **Server erworben haben **Wert erhalten haben, [stellen eine autoermittlungsanforderung an den X-PublicFolderInformation Wert zu ermitteln](#bk_makeautodrequest), legen Sie die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox** Kopfzeilen in Ihrer öffentlichen Ordner Content-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="080df-163">Using the value of the **PublicFolderInformation** SMTP address acquired in [Determine the value of the X-AnchorMailbox header by using the EWS Managed API](#bk_getpfinfoewsma) or [Determine the value of the X-AnchorMailbox header using SOAP](#bk_getpfinfoews) and the **Server** value acquired in [Make an Autodiscover request to determine the X-PublicFolderInformation value](#bk_makeautodrequest), set the values of **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="080df-164">Beispielsweise gehören Sie werden, wenn eine **PublicFolderInformation** SMTP-Adresse des SharedPublicFolder@contoso.com und **Server** Wert 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, die folgenden Header beim Aufrufen der folgenden Methoden oder Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="080df-164">For example, given a **PublicFolderInformation** SMTP address of SharedPublicFolder@contoso.com and a **Server** value of 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, include the following headers when making calls to the following methods or operations.</span></span> 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

<span data-ttu-id="080df-165">**Öffentliche Ordner-Anrufe, die die X-AnchorMailbox und X-PublicFolder Header erfordern**</span><span class="sxs-lookup"><span data-stu-id="080df-165">**Public folder calls that require the X-AnchorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="080df-166">**EWS Managed API-Methoden**</span><span class="sxs-lookup"><span data-stu-id="080df-166">**EWS Managed API methods**</span></span>|<span data-ttu-id="080df-167">**EWS-Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="080df-167">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="080df-168">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="080df-168">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="080df-169">Folder.Delete</span><span class="sxs-lookup"><span data-stu-id="080df-169">Folder.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="080df-170">Folder.Update</span><span class="sxs-lookup"><span data-stu-id="080df-170">Folder.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="080df-171">Folder.Move</span><span class="sxs-lookup"><span data-stu-id="080df-171">Folder.Move</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="080df-172">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="080df-172">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [<span data-ttu-id="080df-173">FindFolder</span><span class="sxs-lookup"><span data-stu-id="080df-173">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [<span data-ttu-id="080df-174">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="080df-174">DeleteFolder</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [<span data-ttu-id="080df-175">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="080df-175">UpdateFolder</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [<span data-ttu-id="080df-176">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="080df-176">MoveFolder</span></span>](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="080df-177">Wenn diese Header mithilfe der EWS Managed API hinzufügen möchten, verwenden Sie die [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="080df-177">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

<span data-ttu-id="080df-178">Mit dem folgende Code wird beispielsweise eine Anforderung [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) mit dem **X-AnchorMailbox** und **X-PublicFolderMailbox** -Header auf die Werte in den Beispielen in diesem Artikel abgerufen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="080df-178">For example, the following code shows a [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: SharedPublicFolder@contoso.com
X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com
Host: outlook.office365.com
Content-Length: 1174
Expect: 100-continue
Connection: Keep-Alive
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:FieldURIOrConstant>
            <t:Constant Value="My Public Contacts" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAwIAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/XB" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="080df-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="080df-179">See also</span></span>

- [<span data-ttu-id="080df-180">Zugriff auf Öffentliche Ordner mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="080df-180">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="080df-181">Weiterleiten von Anforderungen für Öffentliche Ordner</span><span class="sxs-lookup"><span data-stu-id="080df-181">Route public folder content requests</span></span>](how-to-route-public-folder-content-requests.md)    
- [<span data-ttu-id="080df-182">Rufen Sie benutzereinstellungen ab, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="080df-182">Get user settings by using the EWS Managed API</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

