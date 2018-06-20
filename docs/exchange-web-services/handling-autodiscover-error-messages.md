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
# <a name="handling-autodiscover-error-messages"></a>Behandeln von Fehlermeldungen für die AutoErmittlung

Lernen Sie die verschiedenen Typen von AutoErmittlung Fehler und wie Sie mit diesen vorgehen.
  
AutoErmittlung ermöglicht der Anwendung, um Konfigurationsinformationen automatisch abzurufen, und es funktioniert hervorragend. Allerdings gehen Sie Dinge planmäßig nicht immer. Sehen wir uns die häufige Fehler, die auftreten können, und Sie können wie behandeln sie minimieren auffordern, Ihre Benutzer Ihre Client manuell konfiguriert werden müssen.
  
## <a name="http-status-errors"></a>HTTP-Status-Fehler
<a name="bk_HttpErrors"> </a>

Der erste Typ von Fehler, die auftreten können, wenn AutoErmittlung-Anforderungen senden, ist der HTTP-Status. Wenn der HTTP-Status in Ihre Antwort etwas anderes als 200 (OK) ist, enthält Antwort Nutzlast keine die Antwort der AutoErmittlung gesuchte wurden. Zur Vereinfachung können wir nicht 200 Statuscodes in drei Kategorien gruppieren.
  
**In Tabelle 1. HTTP-Statuscodes**

|**Statuscode**|**Art des Fehlers**|**Behandlung von...**|
|:-----|:-----|:-----|
|301 oder 302  <br/> |Umleiten von Fehler  <br/> |Anzeigen Sie Ihrer Anforderung an dem URI in der "Location"-HTTP-Antwortheader enthalten sind. Weitere Informationen hierzu finden Sie unter [Behandlung umleiten Fehler](#bk_HandlingRedirects).  <br/> |
|401  <br/> |Des Fehlers  <br/> |Da der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) mehrere potenzielle URLs versucht umfasst, konnte dies auf eine URL, die nur für den nächsten zu Ihrer Anmeldeinformationen akzeptiert haben abgerufen werden. Aus diesem Grund sollten nicht Sie einen einzelnen 401-Fehler, um anzugeben, dass die Anmeldeinformationen ungültig sind, berücksichtigen. Wenn Sie mehrere URLs 401-Fehler erhalten, sollten Sie den Benutzer auffordern, ihr Kennwort erneut einzugeben, (falls möglich).  <br/> |
|Alle anderen nicht 200-status  <br/> |Ungültige AutoErmittlung-Endpunkt-Fehler  <br/> |Berücksichtigen Sie die URL ein, der anderen nicht 200 Statuscode ungültig liegend zurückgibt, und weiterhin versuchen den nächsten URL in der Liste.  <br/> |
   
## <a name="autodiscover-errors"></a>AutoErmittlung-Fehler
<a name="bk_AutodiscoverErrors"> </a>

Auch wenn Sie nach dem Senden einer Anforderung der AutoErmittlung 200 (OK) Statuscode erhalten möchten, nicht bedeuten, dass der Server die Informationen gesendet, die Sie benötigen. Der Status 200 bedeutet nur, dass Sie eine Antwort der AutoErmittlung haben und diese Antwort möglicherweise einen Fehler in der Nutzlast enthält. Der Speicherort der die Fehlerinformationen hängt davon ab, ob das Format SOAP oder POX ist.
  
### <a name="soap-autodiscover-errors"></a>SOAP-AutoErmittlung-Fehler

Für die SOAP-AutoErmittlung kann die Antwort ein oder mehrere [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) Elemente an verschiedenen Orten enthalten. Sie können in der Regel eine als untergeordnetes Element des Elements [Antwort (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) und eine als untergeordnetes Element jedes [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) -Elements in der Antwort erwarten. Auch kann eine als untergeordnetes Element eines [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) -Elements auftreten, wenn diese vorhanden ist. Im Kontext des Fehlers hängt davon ab, wo sich das **ErrorCode** -Element, wie folgt befindet: 
  
- Als untergeordnetes Element des Elements **Antwort** stellt das **ErrorCode** -Element einen Fehler auf, der für die gesamte Anforderung gilt. 
    
- Als untergeordnetes Element des Elements **UserResponse** stellt er einen Fehler, der nur für diesen bestimmte Benutzer gilt. 
    
- Als untergeordnetes Element des **UserSettingError** -Elements stellt er einen Fehler, der für eine bestimmte Einstellung gilt, das angefordert wurde. 
    
Sehen Sie ein Beispiel für eine Antwort an. In diesem Beispiel hat das **ErrorCode** -Element unter dem Element **Antwort** Wert "NoError", die Erfolg angibt. Das **ErrorCode** -Element unter dem **UserResponse** -Element hat jedoch den Wert "RedirectAddress", die angibt, dass für diesen Benutzer ist ein Fehler aufgetreten. 
  
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

Im Artikel [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) enthält eine vollständige Liste der möglichen Fehler. Geben Sie an, die meisten dieser Fehler kann nicht behoben, aber nur einige besondere Behandlung rechtfertigen. 
  
**In Tabelle 2. SOAP-Autodisover ErrorCode-Werte**

|**ErrorCode-Wert**|**Behandlung von...**|
|:-----|:-----|
|RedirectAddress  <br/> |[Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse](#bk_RestartAutodiscover) mit der e-Mail-Adresse in das Element [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .  <br/> |
|RedirectUrl  <br/> |[Erneutes Senden der Anforderung an eine neue URL](#bk_ResendRequest) , an die URL im **RedirectTarget** -Element.  <br/> |
|ServerBusy  <br/> |Wiederholen Sie diese URL nach einer kleinen Verzögerung. Sie können warten Sie einen bestimmten Zeitraum oder verschieben einfach an das Ende der Liste der URLs und Testen Sie diese URL. Wenn Sie diese Fehlermeldung mehrere Male über eine URL angezeigt wird, sollten Sie die URL ungültig ist.  <br/> |
   
### <a name="pox-autodiscover-errors"></a>POX AutoErmittlung-Fehler

Der AutoErmittlungsdienst POX meldet Fehler ein wenig anders aus. Nicht wiederherstellbaren Fehler sind im [Fehler (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) -Element enthalten. Im Artikel [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) enthält eine vollständige Liste der möglichen Fehlercodes. 
  
Umleitung Fehler sind in der [Aktion (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) -Element enthalten. Jeder Wert des **Action** -Elements als "Einstellungen" gibt eine Umleitung Fehler an. 
  
**Tabelle 3. POX Autodisover ErrorCode-Werte**

|**Aktionswert**|**Behandlung von...**|
|:-----|:-----|
|redirectAddr  <br/> |[Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse](#bk_RestartAutodiscover) mit der e-Mail-Adresse in das Element [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .  <br/> |
|redirectUrl  <br/> |[Erneutes Senden der Anforderung an eine neue URL](#bk_ResendRequest) , an die URL im Element [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .  <br/> |
   
In diesem Beispiel hat das **Action** -Element den Wert "RedirectAddr", die angibt, dass eine neue Anforderung mit der neuen e-Mail-Adresse im **RedirectAddr** -Element enthaltenen gesendet werden sollen. 
  
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

## <a name="handling-redirect-errors"></a>Nächster Schritt: Fehlerbehandlung
<a name="bk_HandlingRedirects"> </a>

Sie können die Umleitung Fehlerszenarien auf zwei Arten behandeln:
  
- Durch einen Neustart AutoErmittlung mit einer neuen e-Mail-Adresse ein.
    
- Durch erneutes Senden der Anforderung an einer neuen URL.
    
Beide Szenarien erfordern, dass einige Überprüfung vor dem fortfahren.
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>Neustarten der AutoErmittlung mit einer neuen e-Mail-Adresse
<a name="bk_RestartAutodiscover"> </a>

Wenn Sie eine neue e-Mail-Adresse in eine AutoErmittlung abrufen Antwort umleiten, stellen Sie zuerst sicher, dass die neue e-Mail-Adresse, die in der Umleitung Fehlerantwort bereitgestellt wurde nicht dieselbe Adresse ist, die Sie in der Anforderung gesendet, die den Fehler verursacht hat. Wenn dies der Fall, sollten nicht neu starten AutoErmittlung und stattdessen die URL, die die Antwort um ungültige werden generiert.
  
Wenn die neue e-Mail-Adresse ist, Verwerfen der vorhandenen Liste der potenziellen AutoErmittlung-Endpunkt-URLs und zum Generieren einer neuen Liste basierend auf der neuen e-Mail-Adresse.
  
### <a name="resending-your-request-to-a-new-url"></a>Erneutes Senden der Anforderung an einer neuen URL
<a name="bk_ResendRequest"> </a>

Wenn Sie eine neue URL in einer Antwort der AutoErmittlung umleiten möchten, sollten Sie zuerst die URL wie folgt überprüfen:
  
- Stellen Sie sicher, dass die URL eine HTTPS-URL ist.
    
- Stellen Sie sicher, dass Sie keinen Fehler aus dieser URL mit der aktuellen e-Mail-Adresse vor erhalten haben.
    
- Gegebenenfalls der Anwendung informieren Sie den Benutzer über die Umleitung zu und ihre Zustimmung folgen die Umleitung.
    
- Senden einer Anforderung an die URL, und [Stellen Sie sicher, dass das SSL-Zertifikat vom Server bereitgestellten gültig ist](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).
    
Falls die URL war erfolgreich, senden Sie die Anforderung an diesen neuen URL.
  
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

