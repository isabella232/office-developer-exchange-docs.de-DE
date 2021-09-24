---
title: Weiterleiten von Anforderungen für öffentliche Ordnerhierarchien
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Alle Anforderungen für Informationen zu öffentlichen Ordnern, die Kenntnisse der Hierarchie öffentlicher Ordner erfordern, z. B. Verschieben, Aktualisieren, Löschen oder Suchen nach öffentlichen Ordnern, müssen an das Standardpostfach für die Öffentliche Ordnerhierarchie für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header "X-AnchorMailbox" und "X-PublicFolderMailbox" auf bestimmte Werte festlegen, die vom AutoErmittlungsdienst zurückgegeben werden.
ms.openlocfilehash: e86e1956db33b7ad8e654a22b980900b4f59dd87
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513122"
---
# <a name="route-public-folder-hierarchy-requests"></a>Weiterleiten von Anforderungen für öffentliche Ordnerhierarchien

Alle Anforderungen für Informationen zu öffentlichen Ordnern, die Kenntnisse der Hierarchie öffentlicher Ordner erfordern, z. B. Verschieben, Aktualisieren, Löschen oder Suchen nach öffentlichen Ordnern, müssen an das Standardpostfach für die Öffentliche Ordnerhierarchie für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die **Header "X-AnchorMailbox"** und **"X-PublicFolderMailbox"** auf bestimmte Werte festlegen, die vom AutoErmittlungsdienst zurückgegeben werden. 
  
**Übersicht über öffentliche Ordner**

|Header|Was benöte ich?|Wie erhalte ich es?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |Der [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) -Wert aus einer [GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx) AutoErmittlung SOAP-Antwort, die der Wert des **X-AnchorMailbox-Headers** wird.<br/><br/> ![X-AnchorMailbox-Antwort](media/Ex15_PF_PFH_Anchor.png)| 1. Senden Sie eine **GetUserSetting-Anforderung** mit der SMTP-Adresse für das Postfach des Benutzers.<br/><br/>2. Zwischenspeichern des Werts des **PublicFolderInformation-Elements,** das vom AutoErmittlungsdienst zurückgegeben wird. Hierbei kann es sich um einen Cache aus einem vorhandenen AutoErmittlungsaufruf in Ihrem Code oder einen neuen [GetUserSettings-Aufruf der verwalteten EWS-API](#bk_getpfinfoewsma) oder eine [GetUserSettings-SOAP-Anforderung](#bk_getpfinfoews)handeln.  <br/><br/>3. Verwenden Sie das **PublicFolderInformation-Element,** um den Wert des **X-AnchorMailbox-Headers** aufzufüllen. Der Wert des **PublicFolderInformation-Elements** ist eine SMTP-Adresse.  <br/> |
|**X-PublicFolderMailbox** <br/> |Der [Serverwert](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) aus einer [POX-AutoErmittlungsantwort,](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx)der zum Wert des **X-PublicFolderMailbox-Headers** wird.<br/><br/> ![X-PublicFolderMailbox-Antwort](media/Ex15_PF_PFH_PFMailbox.png)|1. [Rufen Sie den POX-AutoErmittlungsdienst](#bk_makeautodrequest) mithilfe der **X-AnchorMailbox-E-Mail-Adresse** auf.  <br/><br/>2. Verwenden Sie das vom AutoErmittlungsdienst zurückgegebene **Serverelement,** um den Wert des **X-PublicFolderMailbox-Headers** aufzufüllen. Der Wert von **X-PublicFolderMailbox** ist eine SMTP-Adresse, bei der der Benutzername eine GUID ist.  <br/> |

<br/>

Nachdem Sie die Headerwerte bestimmt haben, schließen Sie sie ein, wenn Sie Anforderungen an die [Hierarchie öffentlicher Ordner stellen.](#bk_setheadervalues)
  
Die Schritte in diesem Artikel gelten speziell für Anforderungen für die Hierarchie öffentlicher Ordner. Informationen dazu, ob es sich bei Ihrer Anforderung um eine Hierarchie öffentlicher Ordner oder eine Inhaltsanforderung handelt, finden Sie unter [Routing von Anforderungen für öffentliche Ordner.](public-folder-access-with-ews-in-exchange.md#bk_routing)
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>Ermitteln des Werts des X-AnchorMailbox-Headers mithilfe der verwalteten EWS-API
<a name="bk_getpfinfoewsma"> </a>

Um den [PublicFolderInformation (POX)-Wert](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) mithilfe der verwalteten EWS-API abzurufen, können Sie entweder den Wert des **PublicFolderInformation-Elements** zwischenspeichern, das ein vorhandener Aufruf des AutoErmittlungsdiensts zurückgibt, oder einen neuen Aufruf ausführen. 
  
Wenn Sie einen neuen Aufruf ausführen, können Sie [Benutzereinstellungen mithilfe der verwalteten EWS-API abrufen](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[von Benutzereinstellungen mithilfe der verwalteten EWS-API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) für Ihren Code abrufen und dann die **GetUserSettings-Beispielmethode** aufrufen, indem Sie den folgenden Code verwenden, der nur den Wert des **PublicFolderInformation-Elements** abruft. Fügen Sie die SMTP-Adresse des Postfachbenutzers als Eingabeparameter ein. 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

Nach dem Ausführen des Codes werden die folgenden Informationen auf der Konsole angezeigt:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

Nachdem Sie nun über den **PublicFolderInformation-Wert** verfügen, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Anforderungen der Hierarchie öffentlicher Ordner ein. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>Ermitteln des Werts des X-AnchorMailbox-Headers mithilfe von SOAP
<a name="bk_getpfinfoews"> </a>

Das folgende Codebeispiel zeigt, wie der **PublicFolderInformation-Wert** mithilfe des [SOAP-Vorgangs GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) abgerufen wird. Der Postfachbenutzer wird im [Mailbox-Element](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) angegeben, und das [RequestedSettings-Element](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) beschränkt die Antwort auf den [PublicFolderInformation-Wert.](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
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

Die Antwort enthält den **PublicFolderInformation-Wert.** 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Nachdem Sie nun über den **PublicFolderInformation-Wert** verfügen, fügen Sie ihn als Wert für den X-AnchorMailbox-Header in alle Anforderungen der Hierarchie öffentlicher Ordner ein. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>Erstellen einer AutoErmittlungsanforderung zum Ermitteln des X-PublicFolderInformation-Werts
<a name="bk_makeautodrequest"> </a>

Stellen Sie eine AutoErmittlungsanforderung mithilfe der **SMTP-Adresse "PublicFolderInformation",** die jetzt als **X-AnchorMailbox-Wert** verwendet wird. Verwenden Sie die [Exchange 2013: Abrufen](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) von Benutzereinstellungen mit AutoErmittlungscodebeispiel, um den AutoErmittlungsdienst aufzurufen, da dadurch der AutoErmittlungsprozess für Sie optimiert wird. In diesem Codebeispiel werden die in der folgenden Tabelle aufgeführten Befehlszeilenargumente verwendet, um den POX-AutoErmittlungsdienst für die **SMTP-Adresse "PublicFolderInformation"** aufzurufen. 
  
|**Befehlszeilenargument**|**Beschreibung**|
|:-----|:-----|
|emailAddress  <br/> |Die **SMTP-Adresse "PublicFolderInformation".**  <br/> |
|-skipSOAP  <br/> | Verwenden Sie POX-AutoErmittlungsanforderungen für dieses Szenario.  <br/> |
|-auth authEmailAddress  <br/> |Die E-Mail-Adresse des Postfachbenutzers, die für die Authentifizierung verwendet wird. Sie werden aufgefordert, das Kennwort des Postfachbenutzers einzugeben, wenn Sie das Beispiel ausführen.  <br/> |
   
Wenn SharedPublicFolder@contoso.com beispielsweise die SMTP-Adresse des **PublicFolderInformation-Elements** und sonyaf@contoso.com der Postfachbenutzer ist, sollten die Befehlszeilenargumente wie folgt aussehen. 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Wenn Sie die **Exchange 2013 ausführen: Abrufen von Benutzereinstellungen mithilfe** des AutoErmittlungsbeispiels, sollte die letzte AutoErmittlungsantwort erfolgreich sein und alle Benutzereinstellungen enthalten, die der Postfach-GUID zugeordnet sind. Der [Serverwert,](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) der dem [EXCH-Protokolltypelement](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)[](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx) zugeordnet ist, ist der **X-PublicFolderInformation-Headerwert.** 
  
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

Wenn Sie die **Exchange 2013 nicht verwenden möchten: Benutzereinstellungen mit autoErmittlungsbeispiel abrufen,** können Sie den **Serverwert** abrufen, indem Sie [eine Liste der AutoErmittlungsendpunkte generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und dann die folgende POX-AutoErmittlungsanforderung an jede URL senden, bis Sie eine erfolgreiche Antwort erhalten. SharedPublicFolder@contoso.com ist der Wert des **X-PublicFolderMailbox-Headers.** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Weitere Informationen zum AutoErmittlungsprozess finden Sie unter [AutoErmittlung für Exchange,](autodiscover-for-exchange.md) [Generieren einer Liste von AutoErmittlungsendpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und Abrufen von [Benutzereinstellungen aus Exchange mithilfe der AutoErmittlung.](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Festlegen der Werte der Header "X-AnchorMailbox" und "X-PublicFolderMailbox"
<a name="bk_setheadervalues"> </a>

Legen Sie unter Verwendung des Werts der **PublicFolderInformation** SMTP-Adresse, die sie in ["Ermitteln des Werts des X-AnchorMailbox-Headers" erworben hat, mithilfe der verwalteten EWS-API](#bk_getpfinfoewsma) oder [mithilfe von SOAP den Wert des X-AnchorMailbox-Headers](#bk_getpfinfoews) und den **Serverwert** fest, der in [einer AutoErmittlungsanforderung zum Ermitteln des X-PublicFolderInformation-Werts](#bk_makeautodrequest)abgerufen wurde, legen Sie die Werte der **X-AnchorMailbox-** und **X-PublicFolderMailbox-Header** in Ihrer Inhaltsanforderung für öffentliche Ordner fest. 
  
Wenn Sie beispielsweise eine **PublicFolderInformation-SMTP-Adresse** von SharedPublicFolder@contoso.com und einen **Serverwert** von 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com angeben, schließen Sie die folgenden Header ein, wenn Sie Aufrufe der folgenden Methoden oder Vorgänge ausführen. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Öffentliche Ordneraufrufe, die die Header X-AnchorMailbox und X-PublicFolder erfordern**

|**EWS Managed API-Methoden**|**EWS-Vorgänge**|
|:-----|:-----|
|[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
Um diese Header mithilfe der verwalteten EWS-API hinzuzufügen, verwenden Sie die [HttpHeaders.Add-Methode.](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

Der folgende Code zeigt beispielsweise eine [FindFolder-Anforderung,](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) bei der der **Header X-AnchorMailbox** und **X-PublicFolderMailbox** auf die werte festgelegt ist, die in den Beispielen in diesem Artikel abgerufen wurden. 
  
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
- [Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner](how-to-route-public-folder-content-requests.md)    
- [Abrufen von Benutzereinstellungen mithilfe der EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

