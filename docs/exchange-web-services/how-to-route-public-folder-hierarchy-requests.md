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
# <a name="route-public-folder-hierarchy-requests"></a>Weiterleitung von Anforderungen für Öffentliche Ordner-Hierarchie

Alle Anfragen für Informationen zu öffentlichen Ordnern, die Kenntnisse in der Hierarchie Öffentlicher Ordner wie verschieben, aktualisieren, löschen oder Suchen nach öffentlichen Ordnern erfordern müssen an das Postfach für die Hierarchie von Öffentliche Ordner für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header auf bestimmte Werte, die von den AutoErmittlungsdienst festgelegt. 
  
**Übersicht über Öffentliche Ordner**

|Kopfzeile|Was muss ich?|Wie erhalte ich es?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |Der Wert der [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) aus [GetUserSettings](http://msdn.microsoft.com/en-us/library/office/dd877096%28v=exchg.150%29.aspx) AutoErmittlung SOAP-Antwort, die den Wert der **X-AnchorMailbox** Kopfzeile wird.<br/><br/> ![ERLEDIGEN](media/Ex15_PF_PFH_Anchor.png)| 1. senden Sie eine **GetUserSetting** -Anforderung mit der SMTP-Adresse für das Postfach des Benutzers.<br/><br/>2. Zwischenspeichern des Werts des **PublicFolderInformation** -Elements, der der AutoErmittlungsdienst zurückgibt. Dies kann eine zwischengespeicherte aus einem laufenden Anruf AutoErmittlung in Ihrem Code oder ein neuer [EWS Managed API GetUserSettings anrufen](#bk_getpfinfoewsma) oder eine [GetUserSettings SOAP-Anforderung](#bk_getpfinfoews)sein.  <br/><br/>3. verwenden Sie das **PublicFolderInformation** -Element zum Auffüllen des Werts der **X-AnchorMailbox** Kopfzeile. Der Wert des **PublicFolderInformation** -Elements ist eine SMTP-Adresse.  <br/> |
|**X-PublicFolderMailbox** <br/> |Der Wert der [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) aus einer [POX AutoErmittlung-Antwort](http://msdn.microsoft.com/en-us/library/bb204082%28v=exchg.150%29.aspx), die den Wert der **X-PublicFolderMailbox** Kopfzeile wird.<br/><br/> ![ERLEDIGEN](media/Ex15_PF_PFH_PFMailbox.png)|1. [Aufrufen der AutoErmittlung POX](#bk_makeautodrequest) -Dienst mithilfe von der **X-AnchorMailbox** e-Mail-Adresse.  <br/><br/>2. verwenden Sie das **Server** -Element, das den AutoErmittlungsdienst zurückgegebene zum Auffüllen des Werts der **X-PublicFolderMailbox** Kopfzeile. Der Wert der **X-PublicFolderMailbox** ist eine SMTP-Adresse, in dem der Benutzername ist eine GUID.  <br/> |

<br/>

Nachdem Sie die Werte für die Kopfzeile festgelegt haben, können Sie diese, [Wenn Sie Öffentliche Ordner-Hierarchie Anforderungen vornehmen](#bk_setheadervalues).
  
Die Schritte in diesem Artikel sind spezifisch für Öffentliche Ordner-Hierarchie Anforderungen. Um festzustellen, ob es sich bei Ihrer Anforderung einer Hierarchie Öffentlicher Ordner oder Content Anforderung ist, finden Sie unter [Routing für Öffentliche Ordner-Anfragen](public-folder-access-with-ews-in-exchange.md#bk_routing).
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>Bestimmen Sie den Wert der X-AnchorMailbox Kopfzeile mithilfe der EWS Managed API
<a name="bk_getpfinfoewsma"> </a>

Rufen Sie den Wert [PublicFolderInformation (POX)](http://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mithilfe der EWS Managed API können Sie Zwischenspeichern Sie den Wert des **PublicFolderInformation** -Elements, der ein laufenden Anruf mit dem AutoErmittlungsdienst zurückgibt, oder stellen einen neuen Anruf aus. 
  
Wenn Sie einen neuen Anruf tätigen, können Sie [Abrufen benutzereinstellungen mithilfe der EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[benutzereinstellungen mithilfe der EWS Managed API erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) , auf Ihr Code, und rufen Sie anschließend die **GetUserSettings** Beispiel-Methode mit den folgenden Code, die abruft nur der Wert des **PublicFolderInformation** -Elements. Enthalten Sie die SMTP-Adresse des Postfachbenutzers als Eingabeparameter. 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

Nach der Ausführung des Codes wird die folgende Informationen in der Konsole angezeigt:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

Nun, da Sie den Wert **PublicFolderInformation** haben, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Öffentliche Ordner-Hierarchie Anforderungen. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>Bestimmen Sie den Wert der X-AnchorMailbox Kopfzeile unter Verwendung von SOAP
<a name="bk_getpfinfoews"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie den **PublicFolderInformation** -Wert mit der [GetUserSettings](http://msdn.microsoft.com/en-us/library/dd877096%28v=exchg.150%29.aspx) SOAP-Operation abgerufen. Der Postfachbenutzer im [Postfach](http://msdn.microsoft.com/en-us/library/dd877076%28v=exchg.150%29.aspx) -Element angegeben ist, und das Element [RequestedSettings](http://msdn.microsoft.com/en-us/library/office/dd877107%28v=exchg.150%29.aspx) beschränkt die Antwort auf den Wert [PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx) . 
  
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

Die Antwort enthält den Wert **PublicFolderInformation** . 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Nun, da Sie den Wert **PublicFolderInformation** haben, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Öffentliche Ordner-Hierarchie Anforderungen. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>Stellen Sie eine autoermittlungsanforderung an den Wert X PublicFolderInformation zu bestimmen
<a name="bk_makeautodrequest"> </a>

Stellen Sie eine autoermittlungsanforderung für die mithilfe der **PublicFolderInformation** SMTP-Adresse, die jetzt als der Wert von **X-AnchorMailbox** verwendet wird. Verwendung der [Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Codebeispiel den AutoErmittlungsdienst aufgerufen, da es die AutoErmittlung für Sie vereinfacht. In diesem Codebeispiel verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenargumente, um den AutoErmittlungsdienst POX für die SMTP-Adresse **PublicFolderInformation** aufrufen. 
  
|**Befehlszeilenargument**|**Beschreibung**|
|:-----|:-----|
|emailAddress  <br/> |Die **PublicFolderInformation** SMTP-Adresse.  <br/> |
|-skipSOAP  <br/> | Verwenden Sie für dieses Szenario POX AutoErmittlungs-Anforderungen.  <br/> |
|-Auth authEmailAddress  <br/> |Das des Postfachbenutzers e-Mail-Adresse, die für die Authentifizierung verwendet wird. Sie werden aufgefordert, die beim Ausführen des Beispiels den Postfachbenutzer Kennwort eingeben.  <br/> |
   
Wenn SharedPublicFolder@contoso.com die SMTP-Adresse des **PublicFolderInformation** -Elements ist und sonyaf@contoso.com den Postfachbenutzer ist, sollte die Befehlszeilenargumente folgendermaßen aussehen. 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Beim Ausführen der **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel die letzte AutoErmittlung Antwort erfolgreich und umfassen sollten alle für die Benutzer die Postfach-GUID zugeordnet. Der [Server](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx) -Wert, der das [Protokoll](http://msdn.microsoft.com/en-us/library/bb204278%28v=exchg.150%29.aspx)für die EXCH[Typ](http://msdn.microsoft.com/en-us/library/office/bb204223%28v=exchg.150%29.aspx) -Element zugeordnet ist die Kopfzeilenwert **X-PublicFolderInformation** . 
  
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

Alternativ, wenn Sie nicht möchten, verwenden Sie die **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel können Sie den **Server** -Wert durch [eine Liste von Endpunkten AutoErmittlung generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und senden Sie dann die folgenden POX AutoErmittlung abrufen Fordern Sie an, dass jede URL, bis Sie eine erfolgreiche Antwort erhalten. SharedPublicFolder@contoso.com ist der Wert der **X-PublicFolderMailbox** Kopfzeile. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Weitere Informationen zu den AutoErmittlung-Prozesses finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [generieren eine Liste von AutoErmittlung-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Legen Sie die Werte der X-AnchorMailbox und X-PublicFolderMailbox-Header
<a name="bk_setheadervalues"> </a>

Verwenden den Wert der **PublicFolderInformation** SMTP-Adresse in [den Wert der X-AnchorMailbox Kopfzeile mithilfe der EWS Managed API bestimmen](#bk_getpfinfoewsma) oder [bestimmen den Wert der Verwendung von SOAP X AnchorMailbox Kopfzeile](#bk_getpfinfoews) und die **Server erworben haben **Wert erhalten haben, [stellen eine autoermittlungsanforderung an den X-PublicFolderInformation Wert zu ermitteln](#bk_makeautodrequest), legen Sie die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox** Kopfzeilen in Ihrer öffentlichen Ordner Content-Anforderung. 
  
Beispielsweise gehören Sie werden, wenn eine **PublicFolderInformation** SMTP-Adresse des SharedPublicFolder@contoso.com und **Server** Wert 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com, die folgenden Header beim Aufrufen der folgenden Methoden oder Vorgänge. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Öffentliche Ordner-Anrufe, die die X-AnchorMailbox und X-PublicFolder Header erfordern**

|**EWS Managed API-Methoden**|**EWS-Vorgänge**|
|:-----|:-----|
|[Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
Wenn diese Header mithilfe der EWS Managed API hinzufügen möchten, verwenden Sie die [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode. 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

Mit dem folgende Code wird beispielsweise eine Anforderung [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) mit dem **X-AnchorMailbox** und **X-PublicFolderMailbox** -Header auf die Werte in den Beispielen in diesem Artikel abgerufen festgelegt. 
  
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

## <a name="see-also"></a>Siehe auch

- [Zugriff auf Öffentliche Ordner mit EWS in Exchange](public-folder-access-with-ews-in-exchange.md)    
- [Weiterleiten von Anforderungen für Öffentliche Ordner](how-to-route-public-folder-content-requests.md)    
- [Rufen Sie benutzereinstellungen ab, indem Sie die EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

