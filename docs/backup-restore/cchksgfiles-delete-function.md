---
title: CChkSGFiles.Delete-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: cf1c23dd75442d73dfea49e0831d0859da321a40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510540"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles.Delete-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Zerstört eine vorhandene Instanz der **CChkSGFiles-Klasse.** Sie müssen diese Funktion aufrufen, nachdem die Anwendung die Arbeit mit dem angegebenen Objekt abgeschlossen hat. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Parameter

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Eingabeparameter. Ein Zeiger auf ein **vorhandenes CCheckSGFiles-Objekt.** Der dem Objekt zugeordnete Speicher wird dann freigegeben. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **Delete-Funktion** gibt den Speicher frei, der dem **CCheckSGFiles-Objekt** zugeordnet ist. Nachdem Sie **"Delete"** aufgerufen haben, ist der im Parameter  *"pcchecksgfiles"*  übergebene Zeiger ungültig, und es können keine weiteren Vorgänge für dieses Objekt ausgeführt werden. 
  
Wenn die Anwendung die **ErrCheckDbPages-Funktion** verwendet, muss die Anwendung den Speicherpuffer manuell freigeben. die **Delete-Funktion** gibt sie nicht frei. 
  
Wenn Sie CHKSGFILES in einer Multithreadanwendung verwenden, müssen Sie die **Delete-Funktion** im Singlethread-Teil der Anwendung aufrufen, und Sie können sie nur einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

