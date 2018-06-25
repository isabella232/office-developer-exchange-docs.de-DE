---
title: CChkSGFiles.New-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: b40f8b1a95477715b29defb4addabfb333e92d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756798"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles.New-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Erstellt eine neue Instanz der **CChkSGFiles** -Klasse. Sie müssen diese Funktion aufrufen, bevor Sie angeben können, die Speichergruppe und Datenbanken überprüft werden soll. 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>Parameter

None.
  
## <a name="return-value"></a>Rückgabewert

Ein Verweis (Zeiger) auf das neu erstellte Objekt.
  
## <a name="remarks"></a>Hinweise

Die **New** -Funktion erstellt ein **CCheckSGFiles** -Objekt und gibt einen Verweis (Zeiger) auf dieses Objekt an den Anrufer zurück. Sie müssen diese Funktion aufrufen, bevor sie eine der anderen Funktionen in der **CCheckSGFiles** -Klasse aufruft. 
  
Wenn Sie für CHKSGFILES in multithreaded-Anwendung verwenden, müssen Sie die **New** -Funktion in den einzelnen Thread Teil der Anwendung aufrufen und können Sie nur einmal für jede **CCheckSGFiles** -Objekt aufrufen. 
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

