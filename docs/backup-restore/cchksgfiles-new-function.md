---
title: CChkSGFiles.New-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: e50b41e761b8e46d778011b6bac3db4dbb624809
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516272"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles.New-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Erstellt eine neue Instanz der **CChkSGFiles-Klasse.** Sie müssen diese Funktion aufrufen, bevor Sie die zu überprüfende Speichergruppe und datenbanken angeben können. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parameter

Keine.
  
## <a name="return-value"></a>Return value

Ein Verweis (Zeiger) auf das neu erstellte Objekt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **Neue** Funktion erstellt ein **CCheckSGFiles** -Objekt und gibt an den Aufrufer einen Verweis (Zeiger) auf dieses Objekt zurück. Sie müssen diese Funktion aufrufen, bevor sie eine der anderen Funktionen in der **CCheckSGFiles-Klasse aufruft.** 
  
Wenn Sie CHKSGFILES in einer Multithreadanwendung verwenden, müssen Sie die **Funktion "New"** im Singlethreadteil der Anwendung aufrufen, und Sie können sie nur einmal für jedes **CCheckSGFiles-Objekt** aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

