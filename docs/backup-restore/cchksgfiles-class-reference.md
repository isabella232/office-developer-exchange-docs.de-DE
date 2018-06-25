---
title: Referenz für die CChkSGFiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Referenzinformationen Sie für die CHKSGFILES-API in Exchange 2013.
ms.openlocfilehash: 583ac5e16ab60d119c3028bf81123e9f60a58ff4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756805"
---
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="4fc47-103">Referenz für die CChkSGFiles</span><span class="sxs-lookup"><span data-stu-id="4fc47-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="4fc47-104">Referenzinformationen Sie für die CHKSGFILES-API in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4fc47-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="4fc47-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fc47-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="4fc47-106">Die CHKSGFILES-API ermöglicht die Sicherung und Wiederherstellung Applications, um die Integrität von Exchange Server 2013-Transaktionsprotokolldateien und Datenbanken programmgesteuert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4fc47-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="4fc47-107">Sie können diese API in Sicherung verwenden und Wiederherstellen von Webanwendungen, die den Volumeschattenkopie-Dienst (Volume Shadow Copy Service, VSS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fc47-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4fc47-108">Speichergruppen sind nicht verfügbar in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4fc47-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="4fc47-109">Unterstützung für Speichergruppen wurde aus Exchange beginnend mit Exchange Server 2010-Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="4fc47-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="4fc47-110">Für die Abwärtskompatibilität mit Datenbanken und Speichergruppen in früheren Versionen von Exchange als Exchange 2010 können mit der API für CHKSGFILES Speichergruppen angeben.</span><span class="sxs-lookup"><span data-stu-id="4fc47-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="4fc47-111">Wenn Sie für CHKSGFILES in Exchange 2013-Datenbanken ausführen, sollten Sie Parameter festlegen, die einen Gruppenbezeichner Speicher auf eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="4fc47-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="4fc47-112">Dateispeicherort</span><span class="sxs-lookup"><span data-stu-id="4fc47-112">File location</span></span>
<span data-ttu-id="4fc47-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="4fc47-113"></span></span>

<span data-ttu-id="4fc47-114">Die CHKSGFILES-API ist im Lieferumfang von Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="4fc47-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="4fc47-115">Sie können diese API auf einem Computer verwenden, die die Postfach-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4fc47-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="4fc47-116">Standardmäßig ist die CHKSGFILES-DLL im Verzeichnis C:\Program Files\Microsoft\Exchange\V15\Bin installiert.</span><span class="sxs-lookup"><span data-stu-id="4fc47-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="4fc47-117">Exchange 2013 umfasst nur eine 64-Bit-Version (amd64) Version der CHKSGFILES-API.</span><span class="sxs-lookup"><span data-stu-id="4fc47-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="4fc47-118">Sie können eine ZIP-Datei, die die Bibliothek CHKSGFILE.lib enthält und CHKSGFILES.hxx-Header-Dateien für die Verwendung in Ihrer benutzerdefinierten Anwendung aus dem [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4fc47-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="4fc47-119">Entwicklungssprachen</span><span class="sxs-lookup"><span data-stu-id="4fc47-119">Development languages</span></span>
<span data-ttu-id="4fc47-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="4fc47-120"></span></span>

<span data-ttu-id="4fc47-121">Die CHKSGFILES-API ist für die Verwendung mit Visual Studio beginnend mit Visual Studio 2005 im systemeigenen C/C++-Versionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4fc47-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="4fc47-122">Die CHKSGFILES-API ist nicht für die Verwendung in verwaltetem Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="4fc47-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="4fc47-123">Obwohl Sie eine COM-Interop-Assembly mit CHKSGFILES erstellen können, werden wir eine unterstützte COM-Interop-Assembly mit Exchange 2013 nicht geliefert.</span><span class="sxs-lookup"><span data-stu-id="4fc47-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="4fc47-124">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="4fc47-124">In this section</span></span>
<span data-ttu-id="4fc47-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="4fc47-125"></span></span>

- [<span data-ttu-id="4fc47-126">CChkSGFiles.CMaxDbPerSG-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="4fc47-127">CChkSGFiles.Delete-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="4fc47-128">CChkSGFiles.ERR-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="4fc47-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="4fc47-129">CChkSGFiles.ErrCheckDbHeaders-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="4fc47-130">CChkSGFiles.ErrCheckDbPages-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="4fc47-131">CChkSGFiles.ErrCheckLogs-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="4fc47-132">CChkSGFiles.ErrGetHeader-Funktion (reserviert)</span><span class="sxs-lookup"><span data-stu-id="4fc47-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="4fc47-133">CChkSGFiles.ErrInit-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="4fc47-134">CChkSGFiles.ErrTerm-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="4fc47-135">CChkSGFiles.iDbInvalid-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="4fc47-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="4fc47-136">CChkSGFiles.New-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="4fc47-137">CChkSGFiles.NO_FLAGS-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="4fc47-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="4fc47-138">CChkSGFiles.PAGE_INFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="4fc47-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="4fc47-139">CChkSGFiles.PgnoFromFileOffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fc47-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="4fc47-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fc47-140">See also</span></span>

- [<span data-ttu-id="4fc47-141">Exchange Online und Exchange-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="4fc47-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="4fc47-142">Sicherung, Wiederherstellung und Notfallwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="4fc47-142">Backup, Restore, and Disaster Recovery</span></span>](http://technet.microsoft.com/en-us/library/dd876874)
    

