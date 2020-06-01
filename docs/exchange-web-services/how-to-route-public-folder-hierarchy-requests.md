---
title: Weiterleiten von Hierarchie Anforderungen für Öffentliche Ordner
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: Alle Anforderungen für Öffentliche Ordner-Informationen, die Kenntnisse der Hierarchie Öffentlicher Ordner erfordern, beispielsweise verschieben, aktualisieren, löschen oder suchen öffentlicher Ordner, müssen an das Standardpostfach für Öffentliche Ordner für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header x-AnchorMailbox und x-PublicFolderMailbox auf bestimmte vom AutoErmittlungsdienst zurückgegebene Werte festlegen.
ms.openlocfilehash: 2773aa3ab29868c69d1fb088deb6c8a96dfb9ecc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455701"
---
# <a name="route-public-folder-hierarchy-requests"></a>Weiterleiten von Hierarchie Anforderungen für Öffentliche Ordner

Alle Anforderungen für Öffentliche Ordner-Informationen, die Kenntnisse der Hierarchie Öffentlicher Ordner erfordern, beispielsweise verschieben, aktualisieren, löschen oder suchen öffentlicher Ordner, müssen an das Standardpostfach für Öffentliche Ordner für den angegebenen Benutzer weitergeleitet werden. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header **x-AnchorMailbox** und **x-PublicFolderMailbox** auf bestimmte vom AutoErmittlungsdienst zurückgegebene Werte festlegen. 
  
**Übersicht über öffentliche Ordner**

|Kopfzeile|Was benötige ich?|Wie erhalte ich diese?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |Der [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) -Wert aus einer [GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx) -SOAP-Antwort, die zum Wert des **X-AnchorMailbox-** Headers wird.<br/><br/> ![TODO](media/Ex15_PF_PFH_Anchor.png)| 1. senden Sie eine **GetUserSetting** -Anforderung mit der SMTP-Adresse für das Postfach des Benutzers.<br/><br/>2. Zwischenspeichern des Werts des **PublicFolderInformation** -Elements, das vom AutoErmittlungsdienst zurückgegeben wird. Dies kann ein zwischengespeicherter von einem vorhandenen Auto Ermittlungs Aufruf in Ihrem Code sein oder ein neuer [verwaltete EWS-API GetUserSettings-Aufruf](#bk_getpfinfoewsma) oder eine [GetUserSettings-SOAP-Anforderung](#bk_getpfinfoews).  <br/><br/>3. verwenden Sie das **PublicFolderInformation** -Element, um den Wert der **X-AnchorMailbox-** Kopfzeile aufzufüllen. Der Wert des **PublicFolderInformation** -Elements ist eine SMTP-Adresse.  <br/> |
|**X-PublicFolderMailbox** <br/> |Der [Server](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) Wert aus einer [POX-Auto Ermittlungs Antwort](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx), die zum Wert des **X-PublicFolderMailbox-** Headers wird.<br/><br/> ![TODO](media/Ex15_PF_PFH_PFMailbox.png)|1. [rufen Sie den POX-Auto Ermittlungs](#bk_makeautodrequest) Dienst unter Verwendung der **X-AnchorMailbox** -e-Mail-Adresse auf.  <br/><br/>2. verwenden Sie das vom AutoErmittlungsdienst zurückgegebene **Server** Element, um den Wert des **X-PublicFolderMailbox-** Headers aufzufüllen. Der Wert von **X-PublicFolderMailbox** ist eine SMTP-Adresse, bei der es sich bei dem Benutzernamen um eine GUID handelt.  <br/> |

<br/>

Wenn Sie die kopfzeilenwerte bestimmt haben, schließen Sie diese ein, [Wenn Sie Hierarchie Anforderungen für Öffentliche Ordner vornehmen](#bk_setheadervalues).
  
Die Schritte in diesem Artikel gelten speziell für Hierarchie Anforderungen für Öffentliche Ordner. Informationen zum ermitteln, ob es sich bei Ihrer Anforderung um eine Hierarchie Öffentlicher Ordner oder eine Inhaltsanforderung handelt, finden Sie unter [Routing Public Folder Requests](public-folder-access-with-ews-in-exchange.md#bk_routing).
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>Bestimmen Sie den Wert des X-AnchorMailbox-Headers mithilfe der verwaltete EWS-API
<a name="bk_getpfinfoewsma"> </a>

Wenn Sie den [PublicFolderInformation (POX)](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) -Wert mithilfe der verwaltete EWS-API abrufen möchten, können Sie entweder den Wert des **PublicFolderInformation** -Elements Zwischenspeichern, das ein vorhandener Aufruf des AutoErmittlungsdiensts zurückgibt, oder einen neuen Anruf tätigen. 
  
Wenn Sie einen neuen Anruf tätigen, können Sie [Benutzereinstellungen abrufen](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed), indem Sie mithilfe des verwaltete EWS-API[Benutzereinstellungen abrufen, indem Sie den Code verwaltete EWS-API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed) verwenden, und dann die **GetUserSettings** -Beispielmethode mit dem folgenden Code aufrufen, der nur den Wert des **PublicFolderInformation** -Elements abruft. Schließen Sie die SMTP-Adresse des Postfachbenutzers als Eingabeparameter ein. 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

Nach dem Ausführen des Codes werden die folgenden Informationen in der Konsole angezeigt:
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

Nachdem Sie nun den **PublicFolderInformation** -Wert haben, fügen Sie ihn als Wert für die X-AnchorMailbox-Kopfzeile in allen Hierarchie Anforderungen für Öffentliche Ordner ein. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>Ermitteln des Werts des X-AnchorMailbox-Headers mit SOAP
<a name="bk_getpfinfoews"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie der **PublicFolderInformation** -Wert mithilfe des [GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) -SOAP-Vorgangs abgerufen wird. Der Postfachbenutzer wird im [Post Fach](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) Element angegeben, und das [RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) -Element schränkt die Antwort auf den [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) -Wert ein. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

Die Antwort enthält den **PublicFolderInformation** -Wert. 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

Nachdem Sie nun den **PublicFolderInformation** -Wert haben, fügen Sie ihn als Wert für die X-AnchorMailbox-Kopfzeile in allen Hierarchie Anforderungen für Öffentliche Ordner ein. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>Erstellen einer AutoErmittlungs-Anforderung zum Ermitteln des X-PublicFolderInformation-Werts
<a name="bk_makeautodrequest"> </a>

Erstellen Sie eine Auto Ermittlungsanforderung mithilfe der SMTP-Adresse **PublicFolderInformation** , die nun als **X-AnchorMailbox-** Wert verwendet wird. Verwenden Sie die [Exchange 2013: Abrufen von Benutzereinstellungen mit der Auto](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Ermittlungs Code-Beispiel, um den AutoErmittlungsdienst aufzurufen, da er den Auto Ermittlungsprozess rationalisiert. In diesem Codebeispiel werden die in der folgenden Tabelle aufgeführten Befehlszeilenargumente verwendet, um den POX-AutoErmittlungsdienst für die SMTP-Adresse **PublicFolderInformation** aufzurufen. 
  
|**Befehlszeilenargument**|**Beschreibung**|
|:-----|:-----|
|emailAddress  <br/> |Die **PublicFolderInformation** -SMTP-Adresse.  <br/> |
|-skipSOAP  <br/> | Verwenden Sie POX-Auto Ermittlungsanforderungen für dieses Szenario.  <br/> |
|-auth authEmailAddress  <br/> |Die e-Mail-Adresse des Postfachbenutzers, die für die Authentifizierung verwendet wird. Sie werden aufgefordert, das Kennwort des Postfachbenutzers einzugeben, wenn Sie das Beispiel ausführen.  <br/> |
   
Wenn SharedPublicFolder@contoso.com beispielsweise die SMTP-Adresse des **PublicFolderInformation** -Elements ist und sonyaf@contoso.com der Postfachbenutzer ist, sollten die Befehlszeilenargumente wie folgt aussehen. 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Wenn Sie das **Exchange 2013: Abrufen von Benutzereinstellungen mit dem Auto Ermittlungs** Beispiel ausführen, sollte die letzte Antwort auf die AutoErmittlung erfolgreich sein und alle Benutzereinstellungen einschließen, die der Postfach-GUID zugeordnet sind. Der [Server](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) Wert, der dem [Protokolltyp](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)-Element des[Typs Typ](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx) zugeordnet ist, ist der **X-PublicFolderInformation-** Headerwert. 
  
```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

Alternativ können Sie, wenn Sie die **Exchange 2013: Abrufen von Benutzereinstellungen mit Auto Ermittlungs** Beispiel verwenden möchten, den **Server** Wert abrufen, indem Sie [eine Liste der Auto Ermittlungs Endpunkte generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und dann die folgende POX-Auto Ermittlungsanforderung an jede URL senden, bis Sie eine erfolgreiche Antwort erhalten. SharedPublicFolder@contoso.com ist der Wert der **X-PublicFolderMailbox-** Kopfzeile. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Weitere Informationen zum Auto Ermittlungsprozess finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [Generieren einer Liste mit Auto Ermittlungs Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Festlegen der Werte der x-AnchorMailbox-und x-PublicFolderMailbox-Kopfzeilen
<a name="bk_setheadervalues"> </a>

Verwenden Sie den Wert der **PublicFolderInformation** -SMTP-Adresse, die in [bestimmen des Werts der x-AnchorMailbox-Kopfzeile mithilfe des verwaltete EWS-APIs verwendet wird](#bk_getpfinfoewsma) , oder [bestimmen Sie den Wert des x-AnchorMailbox-Headers mit SOAP](#bk_getpfinfoews) und den in [make a AutoErmittlung](#bk_makeautodrequest)Acquired erworbenen **Wert der** x- **AnchorMailbox** -und **x-PublicFolderMailbox-** Header in der Inhaltsanforderung für Öffentliche Ordner. 
  
Wenn Sie beispielsweise eine **PublicFolderInformation** -SMTP-Adresse von SharedPublicFolder@contoso.com und einen **Server** Wert von 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com verwenden, schließen Sie die folgenden Kopfzeilen ein, wenn Sie die folgenden Methoden oder Vorgänge aufrufen. 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**Öffentliche Ordner-Aufrufe, die die Header x-AnchorMailbox und x-PublicFolder erfordern**

|**EWS Managed API-Methoden**|**EWS-Operationen**|
|:-----|:-----|
|[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
Verwenden Sie die [httpheaders-. Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode, um diese Header mithilfe der verwaltete EWS-API hinzuzufügen. 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

Der folgende Code zeigt beispielsweise eine [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) -Anforderung, bei der der **x-AnchorMailbox** -und der **x-PublicFolderMailbox-** Header auf die in den Beispielen in diesem Artikel abgerufenen Werte festgelegt sind. 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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
- [Weiterleiten von Inhaltsanforderungen für Öffentliche Ordner](how-to-route-public-folder-content-requests.md)    
- [Abrufen von Benutzereinstellungen mithilfe der EWS Managed API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

