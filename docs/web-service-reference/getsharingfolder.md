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
description: Das GetSharingFolder-Element definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen. Es ist das Basiselement für den Vorgang GetSharingFolder.
ms.openlocfilehash: 7c2f31aa27c1cbde6cdad2b41a341916b4bed2ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829669"
---
# <a name="getsharingfolder"></a><span data-ttu-id="c5c70-104">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="c5c70-104">GetSharingFolder</span></span>

<span data-ttu-id="c5c70-105">Das **GetSharingFolder** -Element definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5c70-105">The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder.</span></span> <span data-ttu-id="c5c70-106">Es ist das Basiselement für den [GetSharingFolder-Vorgang](getsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="c5c70-106">It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).</span></span>
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 <span data-ttu-id="c5c70-107">**GetSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="c5c70-107">**GetSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5c70-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c5c70-108">Attributes and elements</span></span>

<span data-ttu-id="c5c70-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c5c70-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5c70-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c5c70-110">Attributes</span></span>

<span data-ttu-id="c5c70-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5c70-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5c70-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5c70-112">Child elements</span></span>

|<span data-ttu-id="c5c70-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c5c70-113">**Element**</span></span>|<span data-ttu-id="c5c70-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c5c70-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5c70-115">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c5c70-115">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="c5c70-116">Stellt die SMTP-Adresse der anderen Partei in die Beziehung.</span><span class="sxs-lookup"><span data-stu-id="c5c70-116">Represents the SMTP e-mail address of the other party in the sharing relationship.</span></span> <span data-ttu-id="c5c70-117">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5c70-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="c5c70-118">DataType</span><span class="sxs-lookup"><span data-stu-id="c5c70-118">DataType</span></span>](datatype.md) <br/> |<span data-ttu-id="c5c70-119">Beschreibt die Art der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5c70-119">Describes the type of data that is shared by a shared folder.</span></span> <span data-ttu-id="c5c70-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c5c70-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c5c70-121">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="c5c70-121">SharedFolderId</span></span>](sharedfolderid.md) <br/> |<span data-ttu-id="c5c70-122">Stellt den Bezeichner des freigegebenen Ordners, dessen Bezeichner lokalen Ordner zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c5c70-122">Represents the identifier of the shared folder whose local folder identifier should be returned.</span></span> <span data-ttu-id="c5c70-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="c5c70-123">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5c70-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5c70-124">Parent elements</span></span>

<span data-ttu-id="c5c70-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="c5c70-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5c70-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c5c70-126">Remarks</span></span>

<span data-ttu-id="c5c70-127">Ein GetSharingFolder-Element muss ein [SmtpAddress](smtpaddress.md) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5c70-127">A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element.</span></span> <span data-ttu-id="c5c70-128">Ein GetSharingFolder-Element muss auch eine [DataType](datatype.md) -Element oder ein [SharedFolderId](sharedfolderid.md) -Element enthalten, jedoch nicht beide enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c5c70-128">A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both.</span></span> 
  
<span data-ttu-id="c5c70-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c5c70-129">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5c70-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c5c70-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5c70-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5c70-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c5c70-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c5c70-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c5c70-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c5c70-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c5c70-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c5c70-134">Validation File</span></span>  <br/> |<span data-ttu-id="c5c70-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c5c70-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c5c70-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c5c70-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c5c70-137">False</span><span class="sxs-lookup"><span data-stu-id="c5c70-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5c70-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5c70-138">See also</span></span>



[<span data-ttu-id="c5c70-139">GetSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c5c70-139">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="c5c70-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c5c70-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

