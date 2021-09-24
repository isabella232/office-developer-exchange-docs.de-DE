---
title: CChkSGFiles-Klassenreferenz
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Hier finden Sie Referenzinformationen für die CHKSGFILES-API in Exchange 2013.
ms.openlocfilehash: 2daf31c41a47684b85ede196b415884335c3ca79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510533"
---
# <a name="cchksgfiles-class-reference"></a>CChkSGFiles-Klassenreferenz

Hier finden Sie Referenzinformationen für die CHKSGFILES-API in Exchange 2013.
  
**Gilt für:** Exchange Server 2013 
  
Die CHKSGFILES-API ermöglicht es Anwendungen zum Sichern und Wiederherstellen, die Integrität von Transaktionsprotokolldateien und Datenbanken für Exchange Server 2013 programmgesteuert zu überprüfen. Sie können diese API in Sicherungs- und Wiederherstellungsanwendungen verwenden, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.
  
> [!NOTE]
> Storage Gruppen sind in Exchange 2013 nicht verfügbar. Die Unterstützung für Speichergruppen wurde von Versionen von Exchange ab Exchange Server 2010 entfernt. Aus Gründen der Abwärtskompatibilität mit Datenbanken und Speichergruppen in Früheren Versionen von Exchange als Exchange 2010 können Sie mit der CHKSGFILES-API Speichergruppen angeben. Wenn Sie CHKSGFILES für Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Speichergruppenbezeichner auf eine leere Zeichenfolge festlegen. 
  
## <a name="file-location"></a>Dateispeicherort
<a name="bk_fileslocation"> </a>

Die CHKSGFILES-API wird im Rahmen Exchange 2013 ausgeliefert. Sie können diese API auf einem Computer verwenden, auf dem die Postfachserverrolle installiert ist. 
  
Standardmäßig wird die CHKSGFILES-DLL im Verzeichnis "C:\Programme\Microsoft\Exchange\V15\Bin" installiert.
  
Exchange 2013 enthält nur eine 64-Bit-Version (amd64) der CHKSGFILES-API. 
  
Sie können eine .zip Datei herunterladen, die die ChKSGFILE.lib-Bibliothek und die CHKSGFILES.hxx-Headerdateien für die Verwendung in Ihrer benutzerdefinierten Anwendung aus dem [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802)enthält.
  
## <a name="development-languages"></a>Entwicklungssprachen
<a name="bk_developmentlanguages"> </a>

Die CHKSGFILES-API ist für die Verwendung mit Versionen von Visual Studio ab Visual Studio 2005 in systemeigenem C/C++ vorgesehen. Die CHKSGFILES-API ist nicht für die Verwendung in verwaltetem Code vorgesehen. Obwohl Sie eine COM-Interopassembly mit CHKSGFILES erstellen können, wird mit Exchange 2013 keine unterstützte COM-Interopassembly ausgeliefert.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG-Funktion](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete-Funktion](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR-Aufzählung](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders-Funktion](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages-Funktion](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs-Funktion](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles.ErrGetHeader-Funktion (reserviert)](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit-Funktion](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm-Funktion](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid-Aufzählung](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New-Funktion](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS-Aufzählung](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles.PAGE_INFO-Struktur](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset-Funktion](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Siehe auch

- [Exchange Online- und Exchange-Entwicklung](../exchange-server-development.md)
- [Sicherung, Wiederherstellung und Notfallwiederherstellung](https://technet.microsoft.com/library/dd876874)
    

