---
title: Behandeln von Fehlermeldungen für die AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Lernen Sie die verschiedenen Typen von AutoErmittlung Fehler und wie Sie mit diesen vorgehen.
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756840"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="ec7c7-103">Behandeln von Fehlermeldungen für die AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="ec7c7-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="ec7c7-104">Lernen Sie die verschiedenen Typen von AutoErmittlung Fehler und wie Sie mit diesen vorgehen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="ec7c7-105">AutoErmittlung ermöglicht der Anwendung, um Konfigurationsinformationen automatisch abzurufen, und es funktioniert hervorragend.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-105">Autodiscover enables your applications to retrieve configuration information automatically, and it works great.</span></span> <span data-ttu-id="ec7c7-106">Allerdings gehen Sie Dinge planmäßig nicht immer.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-106">However, things don't always go according to plan.</span></span> <span data-ttu-id="ec7c7-107">Sehen wir uns die häufige Fehler, die auftreten können, und Sie können wie behandeln sie minimieren auffordern, Ihre Benutzer Ihre Client manuell konfiguriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-107">Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="ec7c7-108">HTTP-Status-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-108">HTTP status errors</span></span>
<span data-ttu-id="ec7c7-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="ec7c7-109"></span></span>

<span data-ttu-id="ec7c7-110">Der erste Typ von Fehler, die auftreten können, wenn AutoErmittlung-Anforderungen senden, ist der HTTP-Status.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-110">The first type of error you might encounter when sending Autodiscover requests is the HTTP status.</span></span> <span data-ttu-id="ec7c7-111">Wenn der HTTP-Status in Ihre Antwort etwas anderes als 200 (OK) ist, enthält Antwort Nutzlast keine die Antwort der AutoErmittlung gesuchte wurden.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-111">If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for.</span></span> <span data-ttu-id="ec7c7-112">Zur Vereinfachung können wir nicht 200 Statuscodes in drei Kategorien gruppieren.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-112">For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="ec7c7-113">**In Tabelle 1. HTTP-Statuscodes**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="ec7c7-114">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-114">**Status code**</span></span>|<span data-ttu-id="ec7c7-115">**Art des Fehlers**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-115">**Type of error**</span></span>|<span data-ttu-id="ec7c7-116">**Behandlung von...**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec7c7-117">301 oder 302</span><span class="sxs-lookup"><span data-stu-id="ec7c7-117">301 or 302</span></span>  <br/> |<span data-ttu-id="ec7c7-118">Umleiten von Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-118">Redirect error</span></span>  <br/> |<span data-ttu-id="ec7c7-119">Anzeigen Sie Ihrer Anforderung an dem URI in der "Location"-HTTP-Antwortheader enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-119">Resend your request to the URI contained in the "Location" HTTP response header.</span></span> <span data-ttu-id="ec7c7-120">Weitere Informationen hierzu finden Sie unter [Behandlung umleiten Fehler](#bk_HandlingRedirects).</span><span class="sxs-lookup"><span data-stu-id="ec7c7-120">For details, see [Handling redirect errors](#bk_HandlingRedirects).</span></span>  <br/> |
|<span data-ttu-id="ec7c7-121">401</span><span class="sxs-lookup"><span data-stu-id="ec7c7-121">401</span></span>  <br/> |<span data-ttu-id="ec7c7-122">Des Fehlers</span><span class="sxs-lookup"><span data-stu-id="ec7c7-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="ec7c7-123">Da der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) mehrere potenzielle URLs versucht umfasst, konnte dies auf eine URL, die nur für den nächsten zu Ihrer Anmeldeinformationen akzeptiert haben abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="ec7c7-124">Aus diesem Grund sollten nicht Sie einen einzelnen 401-Fehler, um anzugeben, dass die Anmeldeinformationen ungültig sind, berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="ec7c7-125">Wenn Sie mehrere URLs 401-Fehler erhalten, sollten Sie den Benutzer auffordern, ihr Kennwort erneut einzugeben, (falls möglich).</span><span class="sxs-lookup"><span data-stu-id="ec7c7-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="ec7c7-126">Alle anderen nicht 200-status</span><span class="sxs-lookup"><span data-stu-id="ec7c7-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="ec7c7-127">Ungültige AutoErmittlung-Endpunkt-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="ec7c7-128">Berücksichtigen Sie die URL ein, der anderen nicht 200 Statuscode ungültig liegend zurückgibt, und weiterhin versuchen den nächsten URL in der Liste.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="ec7c7-129">AutoErmittlung-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-129">Autodiscover errors</span></span>
<span data-ttu-id="ec7c7-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="ec7c7-130"></span></span>

<span data-ttu-id="ec7c7-131">Auch wenn Sie nach dem Senden einer Anforderung der AutoErmittlung 200 (OK) Statuscode erhalten möchten, nicht bedeuten, dass der Server die Informationen gesendet, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-131">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need.</span></span> <span data-ttu-id="ec7c7-132">Der Status 200 bedeutet nur, dass Sie eine Antwort der AutoErmittlung haben und diese Antwort möglicherweise einen Fehler in der Nutzlast enthält.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-132">The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload.</span></span> <span data-ttu-id="ec7c7-133">Der Speicherort der die Fehlerinformationen hängt davon ab, ob das Format SOAP oder POX ist.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-133">The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="ec7c7-134">SOAP-AutoErmittlung-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="ec7c7-135">Für die SOAP-AutoErmittlung kann die Antwort ein oder mehrere [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) Elemente an verschiedenen Orten enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="ec7c7-136">Sie können in der Regel eine als untergeordnetes Element des Elements [Antwort (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) und eine als untergeordnetes Element jedes [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) -Elements in der Antwort erwarten.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-136">Typically you can expect one as a child element of the [Response (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="ec7c7-137">Auch kann eine als untergeordnetes Element eines [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) -Elements auftreten, wenn diese vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-137">You might also encounter one as a child of a [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="ec7c7-138">Im Kontext des Fehlers hängt davon ab, wo sich das **ErrorCode** -Element, wie folgt befindet:</span><span class="sxs-lookup"><span data-stu-id="ec7c7-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="ec7c7-139">Als untergeordnetes Element des Elements **Antwort** stellt das **ErrorCode** -Element einen Fehler auf, der für die gesamte Anforderung gilt.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="ec7c7-140">Als untergeordnetes Element des Elements **UserResponse** stellt er einen Fehler, der nur für diesen bestimmte Benutzer gilt.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="ec7c7-141">Als untergeordnetes Element des **UserSettingError** -Elements stellt er einen Fehler, der für eine bestimmte Einstellung gilt, das angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="ec7c7-142">Sehen Sie ein Beispiel für eine Antwort an.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-142">Let's take a look at an example of a response.</span></span> <span data-ttu-id="ec7c7-143">In diesem Beispiel hat das **ErrorCode** -Element unter dem Element **Antwort** Wert "NoError", die Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-143">In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success.</span></span> <span data-ttu-id="ec7c7-144">Das **ErrorCode** -Element unter dem **UserResponse** -Element hat jedoch den Wert "RedirectAddress", die angibt, dass für diesen Benutzer ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-144">However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
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

<span data-ttu-id="ec7c7-145">Im Artikel [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) enthält eine vollständige Liste der möglichen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-145">The [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="ec7c7-146">Geben Sie an, die meisten dieser Fehler kann nicht behoben, aber nur einige besondere Behandlung rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="ec7c7-147">**In Tabelle 2. SOAP-Autodisover ErrorCode-Werte**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="ec7c7-148">**ErrorCode-Wert**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-148">**ErrorCode value**</span></span>|<span data-ttu-id="ec7c7-149">**Behandlung von...**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec7c7-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="ec7c7-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="ec7c7-151">[Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse](#bk_RestartAutodiscover) mit der e-Mail-Adresse in das Element [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ec7c7-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="ec7c7-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="ec7c7-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="ec7c7-153">[Erneutes Senden der Anforderung an eine neue URL](#bk_ResendRequest) , an die URL im **RedirectTarget** -Element.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="ec7c7-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="ec7c7-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="ec7c7-155">Wiederholen Sie diese URL nach einer kleinen Verzögerung.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-155">Retry this URL after a small delay.</span></span> <span data-ttu-id="ec7c7-156">Sie können warten Sie einen bestimmten Zeitraum oder verschieben einfach an das Ende der Liste der URLs und Testen Sie diese URL.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-156">You might wait a set amount of time or simply move this URL to the end of your list of URLs to try.</span></span> <span data-ttu-id="ec7c7-157">Wenn Sie diese Fehlermeldung mehrere Male über eine URL angezeigt wird, sollten Sie die URL ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-157">If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="ec7c7-158">POX AutoErmittlung-Fehler</span><span class="sxs-lookup"><span data-stu-id="ec7c7-158">POX Autodiscover errors</span></span>

<span data-ttu-id="ec7c7-159">Der AutoErmittlungsdienst POX meldet Fehler ein wenig anders aus.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="ec7c7-160">Nicht wiederherstellbaren Fehler sind im [Fehler (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-160">Non-recoverable errors are contained in the [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="ec7c7-161">Im Artikel [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) enthält eine vollständige Liste der möglichen Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-161">The [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="ec7c7-162">Umleitung Fehler sind in der [Aktion (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-162">Redirect errors are contained in the [Action (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="ec7c7-163">Jeder Wert des **Action** -Elements als "Einstellungen" gibt eine Umleitung Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="ec7c7-164">**Tabelle 3. POX Autodisover ErrorCode-Werte**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="ec7c7-165">**Aktionswert**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-165">**Action value**</span></span>|<span data-ttu-id="ec7c7-166">**Behandlung von...**</span><span class="sxs-lookup"><span data-stu-id="ec7c7-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec7c7-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="ec7c7-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="ec7c7-168">[Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse](#bk_RestartAutodiscover) mit der e-Mail-Adresse in das Element [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ec7c7-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="ec7c7-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="ec7c7-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="ec7c7-170">[Erneutes Senden der Anforderung an eine neue URL](#bk_ResendRequest) , an die URL im Element [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ec7c7-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="ec7c7-171">In diesem Beispiel hat das **Action** -Element den Wert "RedirectAddr", die angibt, dass eine neue Anforderung mit der neuen e-Mail-Adresse im **RedirectAddr** -Element enthaltenen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="ec7c7-172">Nächster Schritt: Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="ec7c7-172">Handling redirect errors</span></span>
<span data-ttu-id="ec7c7-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="ec7c7-173"></span></span>

<span data-ttu-id="ec7c7-174">Sie können die Umleitung Fehlerszenarien auf zwei Arten behandeln:</span><span class="sxs-lookup"><span data-stu-id="ec7c7-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="ec7c7-175">Durch einen Neustart AutoErmittlung mit einer neuen e-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="ec7c7-176">Durch erneutes Senden der Anforderung an einer neuen URL.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="ec7c7-177">Beide Szenarien erfordern, dass einige Überprüfung vor dem fortfahren.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="ec7c7-178">Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="ec7c7-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="ec7c7-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="ec7c7-179"></span></span>

<span data-ttu-id="ec7c7-180">Wenn Sie eine neue e-Mail-Adresse in eine AutoErmittlung abrufen Antwort umleiten, stellen Sie zuerst sicher, dass die neue e-Mail-Adresse, die in der Umleitung Fehlerantwort bereitgestellt wurde nicht dieselbe Adresse ist, die Sie in der Anforderung gesendet, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-180">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error.</span></span> <span data-ttu-id="ec7c7-181">Wenn dies der Fall, sollten nicht neu starten AutoErmittlung und stattdessen die URL, die die Antwort um ungültige werden generiert.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-181">If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="ec7c7-182">Wenn die neue e-Mail-Adresse ist, Verwerfen der vorhandenen Liste der potenziellen AutoErmittlung-Endpunkt-URLs und zum Generieren einer neuen Liste basierend auf der neuen e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="ec7c7-183">Erneutes Senden der Anforderung an einer neuen URL</span><span class="sxs-lookup"><span data-stu-id="ec7c7-183">Resending your request to a new URL</span></span>
<span data-ttu-id="ec7c7-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="ec7c7-184"></span></span>

<span data-ttu-id="ec7c7-185">Wenn Sie eine neue URL in einer Antwort der AutoErmittlung umleiten möchten, sollten Sie zuerst die URL wie folgt überprüfen:</span><span class="sxs-lookup"><span data-stu-id="ec7c7-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="ec7c7-186">Stellen Sie sicher, dass die URL eine HTTPS-URL ist.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="ec7c7-187">Stellen Sie sicher, dass Sie keinen Fehler aus dieser URL mit der aktuellen e-Mail-Adresse vor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="ec7c7-188">Gegebenenfalls der Anwendung informieren Sie den Benutzer über die Umleitung zu und ihre Zustimmung folgen die Umleitung.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="ec7c7-189">Senden einer Anforderung an die URL, und [Stellen Sie sicher, dass das SSL-Zertifikat vom Server bereitgestellten gültig ist](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c7-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="ec7c7-190">Falls die URL war erfolgreich, senden Sie die Anforderung an diesen neuen URL.</span><span class="sxs-lookup"><span data-stu-id="ec7c7-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ec7c7-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec7c7-191">See also</span></span>


- [<span data-ttu-id="ec7c7-192">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="ec7c7-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="ec7c7-193">Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec7c7-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="ec7c7-194">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ec7c7-194">ErrorCode (SOAP)</span></span>](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="ec7c7-195">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="ec7c7-195">ErrorCode (POX)</span></span>](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

