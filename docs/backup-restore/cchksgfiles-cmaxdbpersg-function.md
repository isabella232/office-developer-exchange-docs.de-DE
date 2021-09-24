---
title: CChkSGFiles.CMaxDbPerSG-Funktion
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 'Last modified: February 22, 2013'
ms.openlocfilehash: 1a82e71afde4766734d0875f68d7932a9fd9f26a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510525"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles.CMaxDbPerSG-Funktion

**Gilt für:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013
  
Gibt die maximale Anzahl von Datenbanken zurück, die in einer einzelnen Exchange Serverspeichergruppe zulässig sind.
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>Parameter

Keine.
  
## <a name="return-value"></a>Return value

Die maximale Anzahl von Datenbanken, die der angegebene Exchange Server pro Speichergruppe zulässt. Da Speichergruppen nicht Teil von Exchange 2013 sind, gibt diese Funktion 1 zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

Sie können das **CCheckSGFiles-Objekt** verwenden, um Datenbanken (und Transaktionsprotokolldateien) nur in einer Speichergruppe zu überprüfen. Daher stellt der von der **CMaxDbPerSG-Funktion** zurückgegebene Wert auch die maximale Anzahl von Datenbanken dar, die Sie mithilfe einer Instanz der **CCheckSGFiles-Klasse** überprüfen können. 
  
Beachten Sie, dass Exchange Server 2003 und Exchange Server 2007 standardmäßig maximal fünf Datenbanken pro Speichergruppe zulassen.
  
## <a name="requirements"></a>Anforderungen

Exchange 2013 enthält nur eine 64-Bit-Version der CHKSGFILES-API.
  
Das Konto, unter dem die Anwendung ausgeführt wird, muss über Lesezugriffsberechtigungen für die Datenbank und die Protokolldateien verfügen, die überprüft werden sollen.
  

