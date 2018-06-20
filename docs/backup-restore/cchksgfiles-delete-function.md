---
title: CChkSGFiles.Delete-Funktion
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
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: 5c41007a797e5a256692b2c4bdcb3cfae82c12ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756804"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles.Delete-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Löscht eine vorhandene Instanz der **CChkSGFiles** -Klasse. Sie müssen diese Funktion aufrufen, nachdem die Anwendung arbeiten mit dem angegebenen Objekt beendet wurde. 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>Parameter

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
Input-Parameter. Ein Zeiger auf ein vorhandenes **CCheckSGFiles** -Objekt. Klicken Sie dann das Objekt zugeordnete Arbeitsspeicher bleiben. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Die **Löschen** -Funktion gibt den Speicherplatz frei **CCheckSGFiles** -Objekt zugeordnet. Nach dem Aufruf von **Löschen**der *Pcchecksgfiles* -Parameter übergebene Zeiger ist ungültig und keine anderen Operationen für dieses Objekt ausgeführt werden können. 
  
Wenn die Anwendung die **ErrCheckDbPages** -Funktion verwendet wird, muss die Anwendung Pufferüberläufe manuell frei; die **Löschen** -Funktion gibt es nicht frei. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **Löschen** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

