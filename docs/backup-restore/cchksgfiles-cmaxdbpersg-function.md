---
title: CChkSGFiles.CMaxDbPerSG-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Zuletzt geändert: 22 Februar 2013'
ms.openlocfilehash: bf09074bab6dee13e97e8a59a22ae1b19522a5e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757766"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles.CMaxDbPerSG-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die maximale Anzahl von Datenbanken in einer einzelnen Exchange Server-Speichergruppe zulässig.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parameter

None.
  
## <a name="return-value"></a>Rückgabewert

Die maximale Anzahl von Datenbanken, die der angegebene Exchange-Server pro Speichergruppe zulässt. Diese Funktion gibt 1 zurück, da Speichergruppen nicht Teil der Exchange 2013 sind.
  
## <a name="remarks"></a>Hinweise

Sie können das **CCheckSGFiles** -Objekt verwenden, um Datenbanken (und Transaktionsprotokolldateien) in nur einer Speichergruppe, überprüfen, damit der von der Funktion **CMaxDbPerSG** zurückgegebene Wert auch die maximale Anzahl von Datenbanken darstellt, die Sie mithilfe von überprüfen kann ein die Instanz der **CCheckSGFiles** -Klasse. 
  
Beachten Sie, dass standardmäßig bis zu fünf Datenbanken pro Speichergruppe Exchange Server 2003 und Exchange Server 2007 ermöglichen.
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 umfasst nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter die Anwendung ausgeführt wird, benötigen Lesezugriff auf die Datenbank und die Protokolldateien, die überprüft werden sollen.
  

