---
title: Behandeln von AutoErmittlungs-Fehlermeldungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Erfahren Sie mehr über die unterschiedlichen Arten von Fehlern bei der AutoErmittlung und wie damit umzugehen ist.
localization_priority: Priority
ms.openlocfilehash: 0cba7e54cb251a9775e0971826560e277dcd9d2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455961"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="5aeef-103">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="5aeef-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="5aeef-104">Erfahren Sie mehr über die unterschiedlichen Arten von Fehlern bei der AutoErmittlung und wie damit umzugehen ist.</span><span class="sxs-lookup"><span data-stu-id="5aeef-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="5aeef-p101">Die AutoErmittlung ermöglicht Ihren Anwendungen, automatisch Konfigurationsinformationen abzurufen, und sie funktioniert hervorragend. Aber die Dinge verlaufen nicht immer nach Plan. Lassen Sie uns die typischen Fehler ansehen, die auftreten können, und wie Sie mit diesen umgehen können, um die Notwendigkeit zu minimieren, Ihre Benutzer aufzufordern, Ihren Client manuell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p101">Autodiscover enables your applications to retrieve configuration information automatically, and it works great. However, things don't always go according to plan. Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="5aeef-108">HTTP-Statusfehler</span><span class="sxs-lookup"><span data-stu-id="5aeef-108">HTTP status errors</span></span>
<span data-ttu-id="5aeef-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="5aeef-109"><a name="bk_HttpErrors"> </a></span></span>

<span data-ttu-id="5aeef-p102">Die erste Art von Fehler, die beim Senden von AutoErmittlungsanforderungen auftreten kann, betrifft den HTTP-Status. Wenn der HTTP-Status in Ihrer Antwort nicht 200 (OK) ist, enthält die Antwortnutzlast nicht die AutoErmittlungsantwort, nach der Sie gesucht haben. Der Einfachheit halber können wir andere Statuscodes als 200 in drei Kategorien gruppieren.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p102">The first type of error you might encounter when sending Autodiscover requests is the HTTP status. If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for. For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="5aeef-113">**Tabelle 1: HTTP-Statuscodes**</span><span class="sxs-lookup"><span data-stu-id="5aeef-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="5aeef-114">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="5aeef-114">**Status code**</span></span>|<span data-ttu-id="5aeef-115">**Fehlertyp**</span><span class="sxs-lookup"><span data-stu-id="5aeef-115">**Type of error**</span></span>|<span data-ttu-id="5aeef-116">**Behandlung**</span><span class="sxs-lookup"><span data-stu-id="5aeef-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5aeef-117">301 oder 302</span><span class="sxs-lookup"><span data-stu-id="5aeef-117">301 or 302</span></span>  <br/> |<span data-ttu-id="5aeef-118">Fehler beim Umleiten</span><span class="sxs-lookup"><span data-stu-id="5aeef-118">Redirect error</span></span>  <br/> |<span data-ttu-id="5aeef-p103">Senden Sie Ihre Anforderung erneut an den URI, der im HTTP-Antwortheader „Location“ enthalten ist. Weitere Informationen finden Sie unter [Behandlung von Umleitungsfehlern](#bk_HandlingRedirects).</span><span class="sxs-lookup"><span data-stu-id="5aeef-p103">Resend your request to the URI contained in the "Location" HTTP response header. For details, see [Handling redirect errors](#bk_HandlingRedirects).  </span></span><br/> |
|<span data-ttu-id="5aeef-121">401</span><span class="sxs-lookup"><span data-stu-id="5aeef-121">401</span></span>  <br/> |<span data-ttu-id="5aeef-122">Fehler „Nicht autorisiert“</span><span class="sxs-lookup"><span data-stu-id="5aeef-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="5aeef-123">Da der [AutoErmittlungs-Prozess](autodiscover-for-exchange.md) das Ausprobieren mehrerer potenzieller URLs umfasst, könnte dieser Fehler bei einer URL lediglich deswegen angezeigt werden, dass Ihre Anmeldeinformationen bei der nächsten akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="5aeef-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="5aeef-124">Aus diesem Grund sollten Sie bei einem einzigen 401-Fehler nicht davon ausgehen, dass die Anmeldeinformationen ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="5aeef-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="5aeef-125">Wenn Sie jedoch von mehreren URLs 401-Fehler erhalten, sollten Sie den Benutzer vielleicht auffordern, sein Kennwort (falls möglich) erneut einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5aeef-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="5aeef-126">Alle anderen Nicht-200-Status</span><span class="sxs-lookup"><span data-stu-id="5aeef-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="5aeef-127">Fehler „Ungültiger AutoErmittlungs-Endpunkt“</span><span class="sxs-lookup"><span data-stu-id="5aeef-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="5aeef-128">Gehen Sie davon aus, dass die URL, bei der andere Nicht-200-Statuscodes zurückgegeben werden, ungültig ist, und fahren Sie mit der nächsten URL in Ihrer Liste fort.</span><span class="sxs-lookup"><span data-stu-id="5aeef-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="5aeef-129">AutoErmittlungs-Fehler</span><span class="sxs-lookup"><span data-stu-id="5aeef-129">Autodiscover errors</span></span>
<span data-ttu-id="5aeef-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="5aeef-130"><a name="bk_AutodiscoverErrors"> </a></span></span>

<span data-ttu-id="5aeef-p105">Auch wenn Sie nach dem Senden einer AutoErmittlungsanforderung den Statuscode 200 (OK) erhalten, bedeutet das nicht, dass der Server die Informationen gesendet hat, die Sie benötigen. Der Status 200 bedeutet nur, dass Sie eine Antwort der AutoErmittlung haben, und diese Antwort kann einen Fehler in der Nutzlast enthalten. Der Standort der Fehlerinformationen ist unterschiedlich, je nachdem, ob das Format SOAP oder POX ist.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p105">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need. The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload. The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="5aeef-134">SOAP-AutoErmittlungs-Fehler</span><span class="sxs-lookup"><span data-stu-id="5aeef-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="5aeef-135">Für die SOAP-AutoErmittlung kann die Antwort ein oder mehrere [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)-Elemente an unterschiedlichen Stellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5aeef-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="5aeef-136">In der Regel ist eines ein untergeordnetes Element des [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)-Elements und eines ein untergeordnetes Element der einzelnen [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)-Elemente in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="5aeef-136">Typically you can expect one as a child element of the [Response (SOAP)](https://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](https://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="5aeef-137">Vielleicht tritt eines auch als untergeordnetes Element eines [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)-Elements auf, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5aeef-137">You might also encounter one as a child of a [UserSettingError (SOAP)](https://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="5aeef-138">Der Kontext des Fehlercodes ist davon abhängig, wo sich das **ErrorCode**-Element befindet:</span><span class="sxs-lookup"><span data-stu-id="5aeef-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="5aeef-139">Das **ErrorCode**-Element stellt als untergeordnetes Element des **Response**-Elements einen Fehler dar, der für die gesamte Anforderung gilt.</span><span class="sxs-lookup"><span data-stu-id="5aeef-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="5aeef-140">Als untergeordnetes Element des **UserResponse**-Elements stellt es einen Fehler dar, der nur für diesen bestimmten Benutzer gilt.</span><span class="sxs-lookup"><span data-stu-id="5aeef-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="5aeef-141">Als untergeordnetes Element des **UserSettingError**-Elements stellt es einen Fehler dar, der für eine bestimmte Einstellung gilt, die angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="5aeef-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="5aeef-p107">Lassen Sie uns einen Blick auf ein Beispiel für eine Antwort werfen. In diesem Beispiel wird hat das Element **ErrorCode** unter dem Element **Response** den Wert „NoError“, was auf einen allgemeinen Erfolg hinweist. Allerdings weist das Element **ErrorCode** unter dem Element **UserResponse** den Wert „RedirectAddress“ auf, was darauf hinweist, dass für diesen bestimmten Benutzer ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p107">Let's take a look at an example of a response. In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success. However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
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
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="5aeef-145">Der Artikel [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) enthält eine vollständige Liste möglicher Fehler.</span><span class="sxs-lookup"><span data-stu-id="5aeef-145">The [ErrorCode (SOAP)](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="5aeef-146">Bei den meisten Fehlern handelt es sich um nicht behebbare Fehler, einige können jedoch auf spezielle Weise behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5aeef-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="5aeef-147">**Tabelle 2. ErrorCode-Werte der SOAP-AutoErmittlung**</span><span class="sxs-lookup"><span data-stu-id="5aeef-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="5aeef-148">**ErrorCode-Wert**</span><span class="sxs-lookup"><span data-stu-id="5aeef-148">**ErrorCode value**</span></span>|<span data-ttu-id="5aeef-149">**Behandlung**</span><span class="sxs-lookup"><span data-stu-id="5aeef-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5aeef-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="5aeef-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="5aeef-151">[Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse](#bk_RestartAutodiscover) mit der E-Mail-Adresse im [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)-Element.</span><span class="sxs-lookup"><span data-stu-id="5aeef-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](https://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="5aeef-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5aeef-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="5aeef-153">[Erneutes Senden Ihrer Anforderung an eine neue URL](#bk_ResendRequest) an die URL im **RedirectTarget**-Element.</span><span class="sxs-lookup"><span data-stu-id="5aeef-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="5aeef-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="5aeef-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="5aeef-p109">Wiederholen Sie diese URL nach einer kurzen Verzögerung. Sie können für einen bestimmten Zeitraum warten oder diese URL einfach an das Ende Ihrer Liste mit URLs verschieben, um es erneut zu versuchen. Wenn Sie diesen Fehler mehrmals für eine URL erhalten, sollten Sie die URL als ungültig betrachten.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p109">Retry this URL after a small delay. You might wait a set amount of time or simply move this URL to the end of your list of URLs to try. If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="5aeef-158">POX-AutoErmittlungs-Fehler</span><span class="sxs-lookup"><span data-stu-id="5aeef-158">POX Autodiscover errors</span></span>

<span data-ttu-id="5aeef-159">Der POX-AutoErmittlungsdienst meldet Fehler etwas anders.</span><span class="sxs-lookup"><span data-stu-id="5aeef-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="5aeef-160">Nicht behebbare Fehler sind im [Error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="5aeef-160">Non-recoverable errors are contained in the [Error (POX)](https://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="5aeef-161">Der Artikel [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) enthält eine vollständige Liste möglicher Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="5aeef-161">The [ErrorCode (POX)](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="5aeef-162">Umleitungsfehler sind im [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)-Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="5aeef-162">Redirect errors are contained in the [Action (POX)](https://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="5aeef-163">Jeder Wert des **Action**-Elements, der nicht „settings“ lautet, deutet auf einen Umleitungsfehler hin.</span><span class="sxs-lookup"><span data-stu-id="5aeef-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="5aeef-164">**Tabelle 3. ErrorCode-Werte der POX-AutoErmittlung**</span><span class="sxs-lookup"><span data-stu-id="5aeef-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="5aeef-165">**Aktionswert**</span><span class="sxs-lookup"><span data-stu-id="5aeef-165">**Action value**</span></span>|<span data-ttu-id="5aeef-166">**Behandlung**</span><span class="sxs-lookup"><span data-stu-id="5aeef-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5aeef-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="5aeef-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="5aeef-168">[Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse](#bk_RestartAutodiscover) mit der E-Mail-Adresse im [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)-Element.</span><span class="sxs-lookup"><span data-stu-id="5aeef-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](https://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="5aeef-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="5aeef-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="5aeef-170">[Erneutes Senden Ihrer Anforderung an eine neue URL](#bk_ResendRequest) an die URL im [RedirectUrl (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)-Element.</span><span class="sxs-lookup"><span data-stu-id="5aeef-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](https://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="5aeef-171">In diesem Beispiel weist das **Action**-Element den Wert „redirectAddr“ auf, was darauf hindeutet, dass eine neue Anforderung mit der neuen E-Mail-Adresse gesendet werden sollte, die sich im **RedirectAddr**-Element befindet.</span><span class="sxs-lookup"><span data-stu-id="5aeef-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="5aeef-172">Behandlung von Umleitungsfehlern</span><span class="sxs-lookup"><span data-stu-id="5aeef-172">Handling redirect errors</span></span>
<span data-ttu-id="5aeef-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="5aeef-173"><a name="bk_HandlingRedirects"> </a></span></span>

<span data-ttu-id="5aeef-174">Szenarien mit Umleitungsfehlern können auf zweierlei Weise behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="5aeef-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="5aeef-175">Durch einen Neustart der AutoErmittlung mit einer neuen E-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5aeef-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="5aeef-176">Durch erneutes Senden der Anforderung an eine neue URL.</span><span class="sxs-lookup"><span data-stu-id="5aeef-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="5aeef-177">Beide Szenarien erfordern einige Überprüfungen, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5aeef-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="5aeef-178">Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="5aeef-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="5aeef-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="5aeef-179"><a name="bk_RestartAutodiscover"> </a></span></span>

<span data-ttu-id="5aeef-p112">Wenn Sie eine neue E-Mail-Adresse in einer AutoErmittlungs-Umleitungsantwort erhalten, überprüfen Sie zunächst, ob die neue E-Mail-Adresse, die in der Umleitungsfehlerantwort bereitgestellt wurde, nicht dieselbe Adresse ist, die Sie in der Anforderung gesendet haben, die den Fehler verursacht hat. Wenn dies der Fall ist, sollten Sie die AutoErmittlung nicht neu starten, sondern stattdessen die URL, die die Antwort generiert hat, als ungültig betrachten.</span><span class="sxs-lookup"><span data-stu-id="5aeef-p112">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error. If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="5aeef-182">Wenn die neue E-Mail-Adresse anders lautet, verwerfen Sie die vorhandene Liste potenzieller URLs für AutoErmittlungs-Endpunkte, und generieren Sie eine neue Liste basierend auf der neuen E-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="5aeef-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="5aeef-183">Erneutes Senden der Anforderung an eine neue URL</span><span class="sxs-lookup"><span data-stu-id="5aeef-183">Resending your request to a new URL</span></span>
<span data-ttu-id="5aeef-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="5aeef-184"><a name="bk_ResendRequest"> </a></span></span>

<span data-ttu-id="5aeef-185">Wenn Sie eine neue E-Mail-Adresse in einer Umleitungsantwort der AutoErmittlung abrufen, sollten Sie die URL zunächst wie folgt überprüfen:</span><span class="sxs-lookup"><span data-stu-id="5aeef-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="5aeef-186">Stellen Sie sicher, dass die URL eine HTTPS-URL ist.</span><span class="sxs-lookup"><span data-stu-id="5aeef-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="5aeef-187">Stellen Sie sicher, dass Sie zuvor keinen Fehler von dieser URL mit der aktuellen E-Mail-Adresse erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="5aeef-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="5aeef-188">Informieren Sie den Benutzer über die Umleitung, und holen Sie sich dessen Berechtigung zum Folgen der Umleitung, wenn dies für Ihre Anwendung zutrifft.</span><span class="sxs-lookup"><span data-stu-id="5aeef-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="5aeef-189">Senden Sie eine Anforderung an die URL, und [überprüfen Sie, dass das SSL-Zertifikat gültig ist](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="5aeef-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="5aeef-190">Wenn die URL die Überprüfung besteht, senden Sie die Anforderung erneute an diese neue URL.</span><span class="sxs-lookup"><span data-stu-id="5aeef-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5aeef-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aeef-191">See also</span></span>


- [<span data-ttu-id="5aeef-192">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="5aeef-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="5aeef-193">Suchen nach AutoErmittlungs-Endpunkten mit der SCP-Suche in Exchange</span><span class="sxs-lookup"><span data-stu-id="5aeef-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="5aeef-194">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5aeef-194">ErrorCode (SOAP)</span></span>](https://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="5aeef-195">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="5aeef-195">ErrorCode (POX)</span></span>](https://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

