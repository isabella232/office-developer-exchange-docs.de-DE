---
title: Behandeln von AutoErmittlungs-Fehlermeldungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Erfahren Sie mehr über die unterschiedlichen Arten von Fehlern bei der AutoErmittlung und wie damit umzugehen ist.
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756840"
---
# <a name="handling-autodiscover-error-messages"></a>Behandeln von AutoErmittlungs-Fehlermeldungen

Erfahren Sie mehr über die unterschiedlichen Arten von Fehlern bei der AutoErmittlung und wie damit umzugehen ist.
  
Die AutoErmittlung ermöglicht es Anwendungen, Konfigurationsinformationen automatisch abzurufen, und dies funktioniert hervorragend. Aber es läuft nicht immer alles nach Plan. Schauen wir uns die gängigen Fehler an, die auftreten können, und wie Sie diese behandeln können, um den Benutzer so wenig wie möglich auffordern zu müssen, den Client manuell zu konfigurieren.
  
## <a name="http-status-errors"></a>HTTP-Statusfehler
<a name="bk_HttpErrors"> </a>

Der erste Fehlertyp, der möglicherweise beim Senden von AutoErmittlung-Anforderungen auftritt, ist der HTTP-Status. Wenn der HTTP-Status in Ihrer Antwort anders als 200 (OK) lautet, enthält die Nutzlast der Antwort nicht die gewünschte Antwort der AutoErmittlung. Der Einfachheit halber können Nicht-200 Statuscodes in drei Kategorien gruppiert werden.
  
**Tabelle 1: HTTP-Statuscodes**

|**Statuscode**|**Fehlertyp**|**Behandlung**|
|:-----|:-----|:-----|
|301 oder 302  <br/> |Fehler beim Umleiten  <br/> |Senden Sie Ihre Anforderung erneut an den im HTTP-Antwortheader „Location“ enthaltenen URI. Weitere Informationen finden Sie unter [Behandlung von Umleitungsfehlern](#bk_HandlingRedirects).  <br/> |
|401  <br/> |Fehler „Nicht autorisiert“  <br/> |Da der [AutoErmittlungs-Prozess](autodiscover-for-exchange.md) das Ausprobieren mehrerer potenzieller URLs umfasst, könnte dieser Fehler bei einer URL lediglich deswegen angezeigt werden, dass Ihre Anmeldeinformationen bei der nächsten akzeptiert werden. Aus diesem Grund sollten Sie bei einem einzigen 401-Fehler nicht davon ausgehen, dass die Anmeldeinformationen ungültig sind. Wenn Sie jedoch von mehreren URLs 401-Fehler erhalten, sollten Sie den Benutzer vielleicht auffordern, sein Kennwort (falls möglich) erneut einzugeben.  <br/> |
|Alle anderen Nicht-200-Status  <br/> |Fehler „Ungültiger AutoErmittlungs-Endpunkt“  <br/> |Gehen Sie davon aus, dass die URL, bei der andere Nicht-200-Statuscodes zurückgegeben werden, ungültig ist, und fahren Sie mit der nächsten URL in Ihrer Liste fort.  <br/> |
   
## <a name="autodiscover-errors"></a>AutoErmittlungs-Fehler
<a name="bk_AutodiscoverErrors"> </a>

Selbst wenn Sie nach dem Senden einer AutoErmittlungs-Anforderung einen 200-Statuscode (OK) erhalten, bedeutet das nicht, dass der Server die von Ihnen benötigten Informationen gesendet hat. Der Status 200 bedeutet nur, dass Sie von der AutoErmittlung eine Antwort erhalten haben und dass diese Antwort möglicherweise einen Fehler innerhalb der Nutzlast enthält. Der Speicherort der Fehlerinformationen variiert in Abhängigkeit davon, ob das Format SOAP oder POX ist.
  
### <a name="soap-autodiscover-errors"></a>SOAP-AutoErmittlungs-Fehler

Für die SOAP-AutoErmittlung kann die Antwort ein oder mehrere [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)-Elemente an unterschiedlichen Stellen enthalten. In der Regel ist eines ein untergeordnetes Element des [Response (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx)-Elements und eines ein untergeordnetes Element der einzelnen [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx)-Elemente in der Antwort. Vielleicht tritt eines auch als untergeordnetes Element eines [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx)-Elements auf, falls vorhanden. Der Kontext des Fehlercodes ist davon abhängig, wo sich das **ErrorCode**-Element befindet: 
  
- Das **ErrorCode**-Element stellt als untergeordnetes Element des **Response**-Elements einen Fehler dar, der für die gesamte Anforderung gilt. 
    
- Als untergeordnetes Element des **UserResponse**-Elements stellt es einen Fehler dar, der nur für diesen bestimmten Benutzer gilt. 
    
- Als untergeordnetes Element des **UserSettingError**-Elements stellt es einen Fehler dar, der für eine bestimmte Einstellung gilt, die angefordert wurde. 
    
Werfen wir einen Blick auf ein Beispiel für eine Antwort. In diesem Beispiel weist das **ErrorCode**-Element unter dem **Response**-Element den Wert „NoError“ auf, der auf allgemeinen Erfolg hindeutet. Das **ErrorCode**-Element unter dem **UserResponse**-Element weist jedoch den Wert „RedirectAddress“ auf, was auf einen Fehler hinweist, der für diesen bestimmten Benutzer aufgetreten ist. 
  
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

Der Artikel [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) enthält eine vollständige Liste möglicher Fehler. Bei den meisten Fehlern handelt es sich um nicht behebbare Fehler, einige können jedoch auf spezielle Weise behandelt werden. 
  
**Tabelle 2. ErrorCode-Werte der SOAP-AutoErmittlung**

|**ErrorCode-Wert**|**Behandlung**|
|:-----|:-----|
|RedirectAddress  <br/> |[Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse](#bk_RestartAutodiscover) mit der E-Mail-Adresse im [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx)-Element.  <br/> |
|RedirectUrl  <br/> |[Erneutes Senden Ihrer Anforderung an eine neue URL](#bk_ResendRequest) an die URL im **RedirectTarget**-Element.  <br/> |
|ServerBusy  <br/> |Wiederholen dieser URL nach eine kurzen Verzögerung. Sie können eine festgelegte Zeit warten oder diese URL einfach an das Ende Ihrer Liste mit URLs verschieben, die Sie ausprobieren. Wenn Sie diese Fehlermeldung mehrmals von einer URL erhalten, sollten Sie diese URL als ungültig betrachten.  <br/> |
   
### <a name="pox-autodiscover-errors"></a>POX-AutoErmittlungs-Fehler

Der POX-AutoErmittlungsdienst meldet Fehler etwas anders. Nicht behebbare Fehler sind im [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx)-Element enthalten. Der Artikel [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) enthält eine vollständige Liste möglicher Fehlercodes. 
  
Umleitungsfehler sind im [Action (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx)-Element enthalten. Jeder Wert des **Action**-Elements, der nicht „settings“ lautet, deutet auf einen Umleitungsfehler hin. 
  
**Tabelle 3. ErrorCode-Werte der POX-AutoErmittlung**

|**Aktionswert**|**Behandlung**|
|:-----|:-----|
|redirectAddr  <br/> |[Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse](#bk_RestartAutodiscover) mit der E-Mail-Adresse im [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx)-Element.  <br/> |
|redirectUrl  <br/> |[Erneutes Senden Ihrer Anforderung an eine neue URL](#bk_ResendRequest) an die URL im [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx)-Element.  <br/> |
   
In diesem Beispiel weist das **Action**-Element den Wert „redirectAddr“ auf, was darauf hindeutet, dass eine neue Anforderung mit der neuen E-Mail-Adresse gesendet werden sollte, die sich im **RedirectAddr**-Element befindet. 
  
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

## <a name="handling-redirect-errors"></a>Behandlung von Umleitungsfehlern
<a name="bk_HandlingRedirects"> </a>

Szenarien mit Umleitungsfehlern können auf zweierlei Weise behandelt werden:
  
- Durch einen Neustart der AutoErmittlung mit einer neuen E-Mail-Adresse.
    
- Durch erneutes Senden der Anforderung an eine neue URL.
    
Beide Szenarien erfordern einige Überprüfungen, bevor Sie fortfahren.
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a>Neustarten der AutoErmittlung mit einer neuen E-Mail-Adresse
<a name="bk_RestartAutodiscover"> </a>

Wenn Sie eine neue E-Mail-Adresse in einer Umleitungsantwort der AutoErmittlung abrufen, überprüfen Sie zunächst, dass die neue E-Mail-Adresse, die in der Umleitungsfehlerantwort bereitgestellt wurde, nicht die gleiche Adresse wie diejenige ist, die Sie in der Anforderung gesendet haben, die zu einem Fehler führte. Ist dies der Fall, sollten Sie die AutoErmittlung nicht neu starten; betrachten Sie die URL, die die Antwort generierte, als ungültig.
  
Wenn die neue E-Mail-Adresse anders lautet, verwerfen Sie die vorhandene Liste potenzieller URLs für AutoErmittlungs-Endpunkte, und generieren Sie eine neue Liste basierend auf der neuen E-Mail-Adresse.
  
### <a name="resending-your-request-to-a-new-url"></a>Erneutes Senden der Anforderung an eine neue URL
<a name="bk_ResendRequest"> </a>

Wenn Sie eine neue E-Mail-Adresse in einer Umleitungsantwort der AutoErmittlung abrufen, sollten Sie die URL zunächst wie folgt überprüfen:
  
- Stellen Sie sicher, dass die URL eine HTTPS-URL ist.
    
- Stellen Sie sicher, dass Sie zuvor keinen Fehler von dieser URL mit der aktuellen E-Mail-Adresse erhalten haben.
    
- Informieren Sie den Benutzer über die Umleitung, und holen Sie sich dessen Berechtigung zum Folgen der Umleitung, wenn dies für Ihre Anwendung zutrifft.
    
- Senden Sie eine Anforderung an die URL, und [überprüfen Sie, dass das SSL-Zertifikat gültig ist](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).
    
Wenn die URL die Überprüfung besteht, senden Sie die Anforderung erneute an diese neue URL.
  
## <a name="see-also"></a>Siehe auch


- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)
    
- [Suchen nach AutoErmittlungs-Endpunkten mit der SCP-Suche in Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    

