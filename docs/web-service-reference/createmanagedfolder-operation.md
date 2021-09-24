---
title: CreateManagedFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: Der CreateManagedFolder-Vorgang erstellt einen verwalteten Ordner im Exchange Speicher.
ms.openlocfilehash: 2b00691fbaba294950a091d5caafb8054f3e2073
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536424"
---
# <a name="createmanagedfolder-operation"></a>CreateManagedFolder-Vorgang

Der CreateManagedFolder-Vorgang erstellt einen verwalteten Ordner im Exchange Speicher.
  
## <a name="using-the-createmanagedfolder-operation"></a>Verwenden des CreateManagedFolder-Vorgangs

Der CreateManagedFolder-Vorgang fügt dem Postfach eines Benutzers einen verwalteten benutzerdefinierten Ordner hinzu. Sie können das Cmdlet **"Get-ManagedFolder"** der Exchange Verwaltungsshell verwenden, um verfügbare verwaltete Ordner zu suchen, die hinzugefügt werden sollen. Obwohl dieses Cmdlet sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner zurückgibt, können nur verwaltete benutzerdefinierte Ordner hinzugefügt werden. Verwaltete benutzerdefinierte Ordner werden durch den Ordnertyp "ManagedCustomFolder" identifiziert. Der System.DirectoryServices-Namespace enthält auch Typen, mit denen die Namen der verfügbaren verwalteten Ordner ermittelt werden können. 
  
> [!NOTE]
> Sie können Exchange Webdienste nicht verwenden, um die Namen der verfügbaren verwalteten Ordner zu finden, die einem Postfach hinzugefügt werden sollen. 
  
Sie können die FindFolder- und GetFolder-Vorgänge verwenden, um auf verwaltete Ordner zuzugreifen. FindFolder wird verwendet, um nach Ordnern in einem angegebenen übergeordneten Ordner zu suchen. Dies kann verwendet werden, damit verwaltete Ordner in einem Ordner ermittelt werden können, bevor versucht wird, demselben Verzeichnis einen doppelten verwalteten benutzerdefinierten Ordner hinzuzufügen. GetFolder wird nach dem FindFolder-Vorgang verwendet, um weitere Informationen zu einem verwalteten benutzerdefinierten Ordner abzurufen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Informationen zum Einrichten einer MRM-Richtlinie (Messaging Records Management) finden Sie unter [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).
  
Informationen zum Entfernen von verwalteten benutzerdefinierten Ordnern aus einem Postfach finden Sie unter [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>CreateManagedFolder-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer CreateManagedFolder-Anforderung zeigt, wie Sie einem Postfach einen verwalteten Ordner namens "Test Managed Folder" hinzufügen.
  
> [!NOTE]
> Sie können auch den Delegatzugriff verwenden, um verwaltete benutzerdefinierte Ordner hinzuzufügen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
Weitere Optionen für die Anforderungsnachricht des CreateManagedFolder-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie mit dem [CreateManagedFolder-Element.](createmanagedfolder.md) 
  
## <a name="successful-createmanagedfolder-response"></a>Erfolgreiche CreateManagedFolder-Antwort

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine erfolgreiche Antwort auf eine CreateManagedFolder-Anforderung.
  
> [!NOTE]
> Die Attributwerte **"Id"** und **"ChangeKey"** wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Ordner](folder.md)
    
- [FolderId](folderid.md)
    
Weitere Optionen für die Antwortnachrichten des CreateManagedFolder-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie beim [CreateManagedFolderResponse-Element.](createmanagedfolderresponse.md) 
  
## <a name="createmanagedfolder-error-response"></a>CreateManagedFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine Fehlerantwort auf eine CreateManagedFolder-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[GetFolder-Vorgang](getfolder-operation.md)
  
[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

