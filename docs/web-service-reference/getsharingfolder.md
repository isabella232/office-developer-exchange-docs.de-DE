---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: Das GetSharingFolder-Element definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners. Es ist das Basiselement für den GetSharingFolder-Vorgang.
ms.openlocfilehash: cb76c534d9b30d0a9d1b267396551eb2871e638a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460505"
---
# <a name="getsharingfolder"></a><span data-ttu-id="38f20-104">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="38f20-104">GetSharingFolder</span></span>

<span data-ttu-id="38f20-105">Das **GetSharingFolder** -Element definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="38f20-105">The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder.</span></span> <span data-ttu-id="38f20-106">Es ist das Basiselement für den [GetSharingFolder-Vorgang](getsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="38f20-106">It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).</span></span>
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 <span data-ttu-id="38f20-107">**GetSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="38f20-107">**GetSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38f20-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="38f20-108">Attributes and elements</span></span>

<span data-ttu-id="38f20-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="38f20-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38f20-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="38f20-110">Attributes</span></span>

<span data-ttu-id="38f20-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="38f20-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38f20-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38f20-112">Child elements</span></span>

|<span data-ttu-id="38f20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="38f20-113">**Element**</span></span>|<span data-ttu-id="38f20-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38f20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38f20-115">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="38f20-115">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="38f20-116">Stellt die SMTP-e-Mail-Adresse des anderen Teilnehmers in der Freigabebeziehung dar.</span><span class="sxs-lookup"><span data-stu-id="38f20-116">Represents the SMTP e-mail address of the other party in the sharing relationship.</span></span> <span data-ttu-id="38f20-117">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38f20-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="38f20-118">DataType</span><span class="sxs-lookup"><span data-stu-id="38f20-118">DataType</span></span>](datatype.md) <br/> |<span data-ttu-id="38f20-119">Beschreibt den Typ der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38f20-119">Describes the type of data that is shared by a shared folder.</span></span> <span data-ttu-id="38f20-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="38f20-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="38f20-121">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="38f20-121">SharedFolderId</span></span>](sharedfolderid.md) <br/> |<span data-ttu-id="38f20-122">Stellt den Bezeichner des freigegebenen Ordners dar, dessen lokaler Ordner Bezeichner zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="38f20-122">Represents the identifier of the shared folder whose local folder identifier should be returned.</span></span> <span data-ttu-id="38f20-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="38f20-123">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38f20-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38f20-124">Parent elements</span></span>

<span data-ttu-id="38f20-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="38f20-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38f20-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38f20-126">Remarks</span></span>

<span data-ttu-id="38f20-127">Ein GetSharingFolder-Element muss ein [SmtpAddress](smtpaddress.md) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="38f20-127">A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element.</span></span> <span data-ttu-id="38f20-128">Ein GetSharingFolder-Element muss auch entweder ein [DataType](datatype.md) -Element oder ein [SharedFolderId](sharedfolderid.md) -Element enthalten, aber nicht beides enthalten.</span><span class="sxs-lookup"><span data-stu-id="38f20-128">A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both.</span></span> 
  
<span data-ttu-id="38f20-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="38f20-129">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38f20-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="38f20-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38f20-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="38f20-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38f20-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="38f20-132">Schema Name</span></span>  <br/> |<span data-ttu-id="38f20-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="38f20-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="38f20-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="38f20-134">Validation File</span></span>  <br/> |<span data-ttu-id="38f20-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="38f20-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38f20-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="38f20-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="38f20-137">False</span><span class="sxs-lookup"><span data-stu-id="38f20-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38f20-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38f20-138">See also</span></span>



[<span data-ttu-id="38f20-139">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="38f20-139">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="38f20-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="38f20-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

