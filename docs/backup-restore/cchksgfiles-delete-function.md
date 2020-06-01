---
title: CChkSGFiles. Delete-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 'Letzte Änderung: 22. Februar 2013'
ms.openlocfilehash: 38cb72b42727855f652de607bb2a02ecdeaae16e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447050"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles. Delete-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Zerstört eine vorhandene Instanz der **CChkSGFiles** -Klasse. Sie müssen diese Funktion aufrufen, nachdem die Anwendung die Arbeit mit dem angegebenen Objekt abgeschlossen hat. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Parameter

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Eingabeparameter. Ein Zeiger auf ein vorhandenes **CCheckSGFiles** -Objekt. Der dem Objekt zugeordnete Arbeitsspeicher wird dann freigegeben. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die **Delete** -Funktion gibt den Arbeitsspeicher frei, der dem **CCheckSGFiles** -Objekt zugeordnet ist. Nachdem Sie **Delete**aufgerufen haben, ist der im *pcchecksgfiles* -Parameter übergebene Zeiger ungültig, und für dieses Objekt können keine anderen Vorgänge ausgeführt werden. 
  
Wenn die Anwendung die **ErrCheckDbPages** -Funktion verwendet, muss die Anwendung den Arbeitsspeicherpuffer manuell freigeben; die **Delete** -Funktion kann Sie nicht freigeben. 
  
Wenn Sie CHKSGFILES in einer Multithread-Anwendung verwenden, müssen Sie die **Delete** -Funktion im Single-Thread-Teil der Anwendung aufrufen, und Sie können Sie nur einmal für jedes **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung betrieben wird, muss über Lesezugriffsberechtigungen für die zu überprüfenden Datenbank-und Protokolldateien verfügen.
  

