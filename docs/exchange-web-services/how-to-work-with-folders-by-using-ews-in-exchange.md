---
title: Arbeiten mit Ordnern unter Verwendung von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4b3eb746-74c4-42a0-aa2c-742c147f1871
description: Erfahren Sie, wie Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.
localization_priority: Priority
ms.openlocfilehash: c09c0c76edda4af025a6ac7121fdf9ab9660fcab
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012545"
---
# <a name="work-with-folders-by-using-ews-in-exchange"></a>Arbeiten mit Ordnern unter Verwendung von EWS in Exchange

Erfahren Sie, wie Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.
  
EWS in Exchange verwendet Ordner, um Postfächer zu strukturieren und zu organisieren. Mithilfe der EWS Managed API oder EWS können Sie neue Ordner erstellen und Ordner abrufen, aktualisieren und löschen. Jeder der in der folgenden Tabelle aufgeführten Methoden oder Vorgehensweisen wird in einem [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)objekt, einem [Ordner](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)-Typ oder [einer der abgeleiteten Ordnerklassen oder -typen](folders-and-items-in-ews-in-exchange.md#bk_folders) ausgeführt.
  
**Tabelle 1. Methoden und Vorgänge für das Erstellen, Abrufen, Aktualisieren und Löschen von Ordnern**

|**Gewünschte Aktion**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen eines Ordners  <br/> |[Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|Erstellen einer Ordnerhierarchie  <br/> |Nicht verfügbar  <br/> |[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |
|Einen Ordner abrufen  <br/> |[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|Abrufen einer Ordnerhierarchie  <br/> |[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> |[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Ordners  <br/> |[Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Löschen eines Ordners  <br/> |[Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |

<a name="bk_createfolderewsma"> </a>

## <a name="create-a-folder-by-using-the-ews-managed-api"></a>Erstellen eines Ordners mithilfe der verwalteten EWS-API

Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)-Klasse ein neuer allgemeiner Ordner mit dem [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) "Benutzerdefinierter Ordner" und dem [FolderClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx)-Eigenschaftswert "IPF.Note" erstellt wird. Die [Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)-Methode speichert den Ordner als untergeordneten Ordner des Posteingangsordners. 
  
In diesen Beispielen wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```csharp
// Create a custom folder.
Folder folder = new Folder(service);
folder.DisplayName = "Custom Folder";
folder.FolderClass = "IPF.Note";
// Save the folder as a child folder of the Inbox.
folder.Save(WellKnownFolderName.Inbox);
```

Um einen anderen Ordnertyp zu erstellen, z. B. [CalendarFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [ContactsFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) oder [TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), erstellen Sie eine neue Instaz der angegebenen Klasse (anstelle der generischen **Folder** -Klasse) und legen die **FolderClass** -Eigenschaft nicht fest. Im folgenden Codebeispiel wird beispielsweise gezeigt, wie ein neuer [TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) erstellt wird.
  
```csharp
// Create a custom Tasks folder.
TasksFolder folder = new TasksFolder(service);
folder.DisplayName = "Custom Tasks";
// Save the folder as a child folder in the Inbox folder.
// This method call results in a CreateFolder call to EWS.
folder.Save(WellKnownFolderName.Inbox);
```

Wenn Sie versuchen, eine Instaz einer angegebenen Klasse zu erstellen und dabei auch die **FolderClass** -Eigenschaft festlegen, wird der Fehler [ErrorNoFolderClassOverride](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) ausgelöst. 
  
Beachten Sie, dass Sie die Erstellung mehrerer Ordner in einem einzigen Methodenaufruf mithilfe der EWS Managed API nicht stapelweise verarbeiten können.
  
## <a name="create-a-folder-by-using-ews"></a>Erstellen eines Ordners mithilfe von EWS
<a name="bk_createfolderews"> </a>

Sie können einen einzelnen Ordner oder mehrere Ordner mithilfe von EWS erstellen.
  
Um einen einzelnen Ordner zu erstellen, senden Sie eine [CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)-Vorgangsanforderungsnachricht. Die **CreateFolder**-Vorgangsanforderung gibt an, dass der übergeordnete Ordner der Posteingang, der [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) "Benutzerdefinierter Ordner" und der [FolderClass](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)-Elementwert "IPF.Note" ist. 
  
Dies ist auch die XML-Anforderung, die EWS Managed API sendet, wenn Sie einen neuen Ordner erstellen und die [Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)-Methode aufrufen. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:Folders>
        <t:Folder>
          <t:FolderClass>IPF.Note</t:FolderClass>
          <t:DisplayName>Custom Folder</t:DisplayName>
        </t:Folder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateFolder**-Anforderung mit einer [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass der Ordner erfolgreich erstellt wurde, sowie die [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) der neu erstellten Nachricht. 
  
Um mehrere Ordner zu erstellen, schließen Sie mehrere [Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)-Elemente in die **CreateFolder**-Vorgangsanforderungsnachricht ein. Alle neuen Ordner müssen sich in demselben übergeordneten Ordner befinden. 
  
## <a name="create-a-folder-hierarchy-by-using-ews"></a>Erstellen einer Ordnerhierarchie mithilfe von EWS
<a name="bk_createfolderhierarchy"> </a>

Mithilfe des [CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx)-Vorgangs in EWS können Sie mit einem einzigen Aufruf eine Ordnerhierarchie erstellen. Die gleiche Funktionalität ist in derEWS Managed API nicht verfügbar. Wenn Sie die EWS Managed API verwenden, können Sie stattdessen Ordner nacheinander erstellen, wie in [Erstellen eines Ordners mithilfe von EWS](#bk_createfolderews) dargestellt.
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
## <a name="get-a-folder-by-using-the-ews-managed-api"></a>Abrufen eines Ordners mithilfe der EWS Managed API
<a name="bk_getfolderewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe der [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)-Methode der Posteingangsordner abgerufen werden kann. Es hat sich bewährt, die zurückgegebenen Eigenschaften auf die für die Anwendung erforderlichen einzuschränken. In diesem Beispiel werden die zurückgegebenen Eigenschaften so eingeschränkt, dass nur die [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)-Eigenschaft durch Erstellen eines [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)-Objekts und das Anwenden des [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)-Werts auf die [BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx)-Eigenschaft eingeschlossen wird. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```csharp
// As a best practice, limit the properties returned to only those that are required.
// In this scenario, you only need the FolderId.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get only the properties specified in the PropertySet.
// This method call results in a GetFolder call to EWS.
Folder rootfolder = Folder.Bind(service, WellKnownFolderName.Inbox, propSet);
```

Wenn zusätzliche Eigenschaften zurückgegeben werden sollen, fügen Sie Eigenschaften aus der [FolderSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx)-Klasse zu **PropertySet** hinzu, oder verwenden Sie eine der überladenen [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)-Methoden, die alle Eigenschaften der ersten Klasse zurückgeben. 
  
Beachten Sie, dass Sie mit der EWS Managed API nicht mehrere Ordner gleichzeitig abrufen können. Sie müssen die **Bind** -Methode in jedem Ordner separat aufrufen. 
  
## <a name="get-a-folder-by-using-ews"></a>Abrufen eines Ordners mithilfe von EWS
<a name="bk_getfolderews"> </a>

Sie können einen einzelnen Ordner oder mehrere Ordner mithilfe von EWS abrufen.
  
Um einen einzelnen Ordner abzurufen, senden Sie eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)-Vorgangsanforderungsnachricht an den Server. Im folgenden Beispiel wird [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) auf **IdOnly** festgelegt, es wird also nur die [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) des angegebenen Ordners zurückgegeben. Das [FolderIds](https://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx)-Element gibt an, dass der abzurufende Ordner der Posteingangsordner ist. 
  
Dies ist auch die XML-Anforderung, die EWS Managed API sendet, wenn Sie mithilfe der [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)-Methode eine Bindung an einen Ordner erstellen. 
  
Um mehrere Ordner zu abzurufen, schließen Sie mehrere [FolderIds](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)-Elemente in die **GetFolder**-Vorgangsanforderungsnachricht ein. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

Das folgende XML-Beispiel zeigt die [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)-Nachricht, die vom Server an den Client als Antwort auf die **GetFolder**-Vorgangsanforderung gesendet wird. Sie enthält nur den [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)-Wert für den Ordner "Posteingang". Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="800"
                         MinorBuildNumber="16"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAENAAA=" ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAEkbCr"/>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-a-folder-hierarchy-by-using-the-ews-managed-api"></a>Abrufen einer Ordnerhierarchie mithilfe der EWS Managed API
<a name="bk_getfolderhierarchyewsma"> </a>

Im folgenden Codebeispiel wird gezeigt, wie die Unterordner für einen bestimmten Stammordner abgerufen werden. In diesem Beispiel werden die Unterordner des **MsgFolderRoot**-Ordners abgerufen, der der Stamm der IMP-Unterstruktur ist (in der Postfachordner und -elemente gespeichert sind). 
  
In diesem Beispiel wird ein [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)-Klassenobjekt erstellt, um die Ergebnisse der [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)-Methodenantwort einzuschränken. Durch dieses Szenario werden die Eigenschaften so eingeschränkt, dass Folgendes zurückgegeben wird: [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) und die erweiterte Eigenschaft, die angibt, ob der Ordner ein ausgeblendeter Ordner ist. Legen Sie den [FolderView.Traversal](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx)-Wert auf "Deep" fest, um eine rekursive Suche auszuführen, sodass der Server die Unterordner abruft, und legen Sie den Stammordner auf **MsgFolderRoot** fest, damit der Server alle Ordner des Benutzers zurückgibt (und der Server keine Systemordner in der Nicht-IPM-Unterstruktur zurückgibt).
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```csharp
// Create a new folder view, and pass in the maximum number of folders to return.
FolderView view = new FolderView(folderViewSize);
// Create an extended property definition for the PR_ATTR_HIDDEN property,
// so that your results will indicate whether the folder is a hidden folder.
ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
// As a best practice, limit the properties returned to only those required.
// In this case, return the folder ID, DisplayName, and the value of the isHiddenProp
// extended property.
view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, isHiddenProp);
// Indicate a Traversal value of Deep, so that all subfolders are retrieved.
view.Traversal = FolderTraversal.Deep;
// Call FindFolders to retrieve the folder hierarchy, starting with the MsgFolderRoot folder.
// This method call results in a FindFolder call to EWS.
FindFoldersResults findFolderResults = service.FindFolders(WellKnownFolderName.MsgFolderRoot, view);
```

## <a name="get-a-folder-hierarchy-by-using-ews"></a>Abrufen einer Ordnerhierarchie mithilfe von EWS
<a name="bk_getfolderhierarchyews"> </a>

In den folgenden XML-Beispielen wird veranschaulicht, wie der [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)-Vorgang zum Abrufen einer Ordnerhierarchie mithilfe von EWS verwendet wird. In diesem Beispiel werden der **msgfolderroot**-Ordner, der der Stamm der IPM-Unterstruktur ist, sowie alle Unterordner abgerufen. Das **Traversal**-Attribut wird auf **Deep** festgelegt, sodass der Server eine rekursive Suche der Ordnerhierarchie ausführt und nur Ordner und Unterordner unter dem angegebenen Stamm in der Antwort zurückgibt. In diesem Beispiel ist das [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)-Element auf **IdOnly** festgelegt, sodass der Server nur das [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)-Element zurückgibt. Um die Ausgabe leichter verständlich zu machen, schließen Sie das **DisplayName**-Element in Ihre Ergebnisse mit ein, indem Sie dieses in das [AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)-Element in der Anforderung zusammen mit dem **ExtendedFieldURI**-Wert für die **PR_ATTR_HIDDEN** -Eigenschaft einschließen, sodass Sie wissen, ob die Ordner ausgeblendete Ordner sind. 
  
Dies ist auch die XML-Anforderung, die EWS Managed API sendet, wenn Sie die [FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)-Methode aufrufen. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

Das folgende XML-Beispiel zeigt die [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)-Nachricht, die vom Server an den Client als Antwort auf die **FindFolder**-Vorgangsanforderung gesendet wird. Sie enthält nur die[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), den [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) und den Wert der erweiterten **PR_ATTR_HIDDEN** -Eigenschaft für alle Unterordner unter dem **msgrootfolder**-Ordner. Wenn das [Value](https://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx)-Element auf "true" festgelegt ist, wird der Ordner in der Clientansicht ausgeblendet. 
  
Dies ist auch die XML-Antwort, die die EWS Managed API sendet, wenn Sie mehrere Ordner mithilfe der [FindFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)-Methode abrufen. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige Ordner wurden aus Platzgründen nicht eingeschlossen. 
  
```xml
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="815"
                         MinorBuildNumber="6"
                         Version="V2_7"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="16"
                        TotalItemsInView="16"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:CalendarFolder>
                <t:FolderId Id="AAAEOAAA="
                            ChangeKey="AgAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA3"/>
                <t:DisplayName>Calendar</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:CalendarFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAEPAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA4"/>
                <t:DisplayName>Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAUKAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAS5"/>
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AAAUJAAA="
                            ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAASx"/>
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
…
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-folder-by-using-the-ews-managed-api"></a>Aktualisieren eines Ordners mithilfe der EWS Managed API
<a name="bk_updatefolderewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie der Anzeigename eines Ordners mithilfe der EWS Managed API aktualisiert wird.
  
Erstellen Sie zuerst einen [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx), um die Anzahl von Eigenschaften einzuschränken, die der Server in der [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)-Antwort zurückgibt. Es wird empfohlen, dass Sie **IdOnly** **BasePropertySet** verwenden, um die Aufrufe der Exchange-Datenbank zu reduzieren. Verwenden Sie anschließend die **Bind** -Methode, um eine Bindung an den zu aktualisierenden Ordner herzustellen. Aktualisieren Sie dann die [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)-Eigenschaft, und verwenden Sie die [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)-Methode, um die Änderungen zu speichern. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer für einen Exchange-Server authentifiziert wurde. Die lokale Variable  *folderId*  ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) des zu aktualisierenden Ordners. 
  
```cs
// As a best practice, only include the ID value in the PropertySet.
PropertySet propertySet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get the FolderId.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId, propertySet);
// Update the display name of the folder.
folder.DisplayName = "Updated folder name";
// Save the updates.
// This method call results in an UpdateFolder call to EWS.
folder.Update();

```

## <a name="update-a-folder-by-using-ews"></a>Aktualisieren eines Ordners mithilfe von EWS
<a name="bk_updatefolderews"> </a>

In den folgenden XML-Beispielen wird veranschaulicht, wie der Anzeigename eines Ordners mithilfe von EWS aktualisiert wird.
  
Senden Sie zunächst eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)-Vorgangsanforderungsnachricht an den zu aktualisierenden Ordner, wie in [Abrufen einer Ordnerhierarchie mithilfe von EWS](#bk_getfolderhierarchyews) dargestellt.
  
Senden Sie dann eine [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)-Vorgangsanforderungsnachricht an den Server, um einen Ordner zu aktualisieren. Die **UpdateFolder**-Vorgangsanforderung aktualisiert den [DisplayName](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) in "Aktualisierten benutzerdefinierten Ordner". 
  
Dies ist auch die XML-Anforderung, die die EWS Managed API sendet, wenn Sie einen Ordner mithilfe der [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)-Methode aktualisieren. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWb" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName" />
              <t:Folder>
                <t:DisplayName>Updated Custom Folder</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateFolder**-Anforderung mit einer [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** und die [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) des Ordners enthält, der mit einem aktualisierten **ChangeKey**-Attributwert aktualisiert wurde. 
  
## <a name="delete-a-folder-by-using-the-ews-managed-api"></a>Löschen eines Ordners mithilfe der EWS Managed API
<a name="bk_deletefolderewsma"> </a>

Dieser Artikel enthält ein einfaches Beispiel, in dem gezeigt wird, wie ein Ordner mithilfe der EWS Managed API gelöscht wird. Weitere Informationen zum Löschen von Ordnern finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).
  
Um einen Ordner mithilfe der EWS Managed API zu löschen, verwenden Sie zuerst die [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)-Methode, um das Dienstobjekt an den zu löschenden Ordner zu binden. Verwenden Sie dann die [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)-Methode, um den Ordner mithilfe des [HardDelete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx)-Löschmodus zu löschen. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt istund der Benutzer bei einem Exchange-Server authentifiziert wurde. Die lokale Variable  *folderId*  ist die [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) des zu löschenden Ordners. 
  
```cs
// Bind to an existing folder and get all its properties.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId);
// HardDelete the folder.
// This method call results in a DeleteFolder call to EWS.
folder.Delete(DeleteMode.HardDelete);
```

## <a name="delete-a-folder-by-using-ews"></a>Löschen eines Ordners mithilfe von EWS
<a name="bk_deletefolderews"> </a>

Dieser Artikel enthält ein einfaches Beispiel, in dem gezeigt wird, wie ein Ordner mithilfe von EWS gelöscht wird. Weitere Informationen zum Löschen von Ordnern finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).
  
Um einen Ordner mit EWS zu löschen, senden Sie zuerst eine [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)-Vorgangsanforderungsnachricht, damit der Ordner wie in [Abrufen eines Ordners mithilfe von EWS](#bk_getfolderews) gezeigt aktualisiert wird. 
  
Senden Sie als Nächstes eine [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)-Vorgangsanforderungsnachricht an den Server, um den Ordner zu löschen. Die **DeleteFolder**-Vorgangsanforderung gibt an, dass der **DeleteType** **HardDelete** ist und die [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) des zu löschenden Ordners umfasst. 
  
Dies ist auch die XML-Antwort, die die EWS Managed API sendet, wenn Sie einen Ordner mithilfe der [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)-Methode löschen. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt, und einige Ordner wurden aus Platzgründen nicht eingeschlossen. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="HardDelete">
      <m:FolderIds>
        <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWf" />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **DeleteFolder**-Anforderung mit einer [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass der Ordner erfolgreich gelöscht wurde.
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_nextsteps"> </a>

Nachdem Sie die Ordner auf dem Server abgerufen haben oder Änderungen an Ordner vorgenommen haben, möchten Sie vielleicht [Ihre Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md) oder [Benachrichtigungen zu Änderungen von Ordnern auf dem Server abonnieren](notification-subscriptions-mailbox-events-and-ews-in-exchange.md). 
  
## <a name="see-also"></a>Siehe auch

- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)   
- [Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)   
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

