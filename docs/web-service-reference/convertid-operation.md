---
title: ConvertId-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 47d96cf6-9e2f-4fc0-9682-7258d3fbf918
description: Hier finden Sie Informationen zum EWS-Vorgang der Convert-Funktion.
ms.openlocfilehash: 36bd47d3fc7c7ca7cea7b38222abb25fba6074ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452552"
---
# <a name="convertid-operation"></a><span data-ttu-id="30a55-103">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30a55-103">ConvertId operation</span></span>

<span data-ttu-id="30a55-104">Hier finden Sie Informationen zum EWS-Vorgang der **Convert** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="30a55-104">Find information about the **ConvertId** EWS operation.</span></span> 
  
<span data-ttu-id="30a55-105">Der Exchange-Webdienste-Vorgang **convertType** konvertiert Element-und Ordner Bezeichner zwischen Formaten, die von Exchange Online akzeptiert werden, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, die mit Exchange Server 2013 beginnen.</span><span class="sxs-lookup"><span data-stu-id="30a55-105">The **ConvertId** Exchange Web Services (EWS) operation converts item and folder identifiers between formats that are accepted by Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with Exchange Server 2013.</span></span> 
  
## <a name="using-the-convertid-operation"></a><span data-ttu-id="30a55-106">Verwenden des Convert-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="30a55-106">Using the ConvertId operation</span></span>
<span data-ttu-id="30a55-107"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-107"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="30a55-108">Sie können die folgenden Bezeichner mithilfe des **Convert** -Vorgangs konvertieren:</span><span class="sxs-lookup"><span data-stu-id="30a55-108">You can convert the following identifiers by using the **ConvertId** operation:</span></span> 
  
- <span data-ttu-id="30a55-109">Das ID-Format für EWS in der ersten Version von Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="30a55-109">The identifier format for EWS in the initial release version of Exchange 2007.</span></span> <span data-ttu-id="30a55-110">Dies wird durch den `EwsLegacyId` Aufzählungswert in der [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-110">This is represented by the  `EwsLegacyId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="30a55-111">Das ID-Format für EWS in Exchange 2007 SP1 oder Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="30a55-111">The identifier format for EWS in Exchange 2007 SP1 or Exchange 2010.</span></span> <span data-ttu-id="30a55-112">Dies wird durch den `EwsId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-112">This is represented by the  `EwsId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="30a55-113">Der MAPI-Bezeichner, wie in der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="30a55-113">The MAPI identifier, as in the **PR_ENTRYID** property.</span></span> <span data-ttu-id="30a55-114">Dies wird durch den `EntryId` Aufzählungswert in der [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) -Aufzählung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-114">This is represented by the  `EntryId` enumeration value in the [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) enumeration.</span></span> 
    
- <span data-ttu-id="30a55-115">Die Ereignis-ID des Verfügbarkeitskalenders.</span><span class="sxs-lookup"><span data-stu-id="30a55-115">The availability calendar event identifier.</span></span> <span data-ttu-id="30a55-116">Dies ist eine hexadezimal codierte Darstellung der **PR_ENTRYID** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="30a55-116">This is a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="30a55-117">Dies wird durch den `HexEntryId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-117">This is represented by the  `HexEntryId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span>
    
- <span data-ttu-id="30a55-118">Die Exchange-Informationsspeicher-ID.</span><span class="sxs-lookup"><span data-stu-id="30a55-118">The Exchange store identifier.</span></span> <span data-ttu-id="30a55-119">Dies wird durch den `StoreId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-119">This is represented by the  `StoreId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="30a55-120">Der **Convert** -ID-Vorgang konvertiert keine Bezeichner für Öffentliche Ordner aus dem EWS-Bezeichner in die Speicher-ID.</span><span class="sxs-lookup"><span data-stu-id="30a55-120">The **ConvertId** operation does not convert public folder identifiers from the EWS identifier to the store identifier.</span></span> 
    
- <span data-ttu-id="30a55-121">Die Outlook Web App-ID.</span><span class="sxs-lookup"><span data-stu-id="30a55-121">The Outlook Web App identifier.</span></span> <span data-ttu-id="30a55-122">Dies wird durch den `OwaId` Aufzählungswert in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-122">This is represented by the  `OwaId` enumeration value in [IdFormat](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.idformat%28v=exchg.80%29.aspx)</span></span>
    
    <span data-ttu-id="30a55-123">Die Übergabe von URLs, die von diesem Bezeichner an Outlook Web App erstellt werden, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30a55-123">The passing of URLs that are created from this identifier to Outlook Web App is not supported.</span></span> <span data-ttu-id="30a55-124">Der Outlook Web App Bezeichner gilt für Exchange 2007 und Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="30a55-124">The Outlook Web App identifier is applicable to Exchange 2007 and Exchange 2010.</span></span> <span data-ttu-id="30a55-125">Outlook Web App für Exchange Online und Versionen von Exchange, die mit Exchange Server 2013 beginnen, werden EWS-IDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="30a55-125">Outlook Web App for Exchange Online and versions of Exchange starting with Exchange Server 2013 uses EWS identifiers.</span></span>
    
<span data-ttu-id="30a55-126">Der **Convert** -ID-Vorgang funktioniert nicht wie erwartet beim Konvertieren von Bezeichnern für Öffentliche Ordner aus der EWS-ID in die Speicher-ID in Exchange Online und Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="30a55-126">The **ConvertId** operation does not work as expected when converting public folder identifiers from the EWS identifier to the store identifier in Exchange Online and Exchange 2013.</span></span> <span data-ttu-id="30a55-127">Zur Problemumgehung können Sie die zurückgegebene Kennung manuell anpassen.</span><span class="sxs-lookup"><span data-stu-id="30a55-127">You can manually update the identifier that is returned as a workaround.</span></span> <span data-ttu-id="30a55-128">So aktualisieren Sie den Bezeichner manuell:</span><span class="sxs-lookup"><span data-stu-id="30a55-128">To manually update the identifier:</span></span> 
  
1. <span data-ttu-id="30a55-129">Bestimmen Sie im Anwendungscode, ob sich das Zielelement/der Ordner in einem öffentlichen Ordner befindet.</span><span class="sxs-lookup"><span data-stu-id="30a55-129">In your application code, determine whether the target item/folder is in a public folder.</span></span> 
    
2. <span data-ttu-id="30a55-130">Decodieren Sie die Base64-codierte Bezeichner-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30a55-130">Decode the Base64-encoded identifier string.</span></span>
    
3. <span data-ttu-id="30a55-131">Stellen Sie sicher, dass das Typ Byte (21. Byte) den Wert 7 aufweist.</span><span class="sxs-lookup"><span data-stu-id="30a55-131">Verify that the type byte (21st byte) has a value of 7.</span></span> <span data-ttu-id="30a55-132">Der Wert 7 gibt an, dass der Bezeichner das falsche Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="30a55-132">A value of 7 indicates that the identifier is in the incorrect format.</span></span>
    
4. <span data-ttu-id="30a55-133">Überspringen Sie die ersten vier Bytes.</span><span class="sxs-lookup"><span data-stu-id="30a55-133">Skip the first four bytes.</span></span> <span data-ttu-id="30a55-134">Sie müssen auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="30a55-134">They must be set to zero.</span></span>
    
5. <span data-ttu-id="30a55-135">Aktualisieren der nächsten 16 Bytes mit der folgenden GUID: 1A447390AA6611CD9BC800AA002FC45A</span><span class="sxs-lookup"><span data-stu-id="30a55-135">Update the next 16 bytes with the following GUID: 1A447390AA6611CD9BC800AA002FC45A</span></span>
    
6. <span data-ttu-id="30a55-136">Aktualisieren Sie das nächste Byte (Typ Byte) mit dem Wert 9.</span><span class="sxs-lookup"><span data-stu-id="30a55-136">Update the next byte (type byte) with a value of 9.</span></span>
    
7. <span data-ttu-id="30a55-137">Ändern Sie den Bezeichner in eine Base64-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30a55-137">Change the identifier to a Base64-encoded string.</span></span>
    
> [!NOTE]
> <span data-ttu-id="30a55-138">Der **Convert** -Vorgang überprüft, ob eine bestimmte SMTP-Adresse ein gültiges Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="30a55-138">The **ConvertId** operation validates that a given SMTP address has a valid format.</span></span> <span data-ttu-id="30a55-139">Der Vorgang bestimmt nicht, ob eine SMTP-Adresse ein gültiges Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="30a55-139">The operation does not determine whether an SMTP address represents a valid mailbox.</span></span> 
  
<span data-ttu-id="30a55-140">Der **Convert** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="30a55-140">The **ConvertId** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="30a55-141">**Tabelle 1. SOAP-Header für Convert-Operation**</span><span class="sxs-lookup"><span data-stu-id="30a55-141">**Table 1. ConvertId operation SOAP headers**</span></span>

|<span data-ttu-id="30a55-142">**Header**</span><span class="sxs-lookup"><span data-stu-id="30a55-142">**Header**</span></span>|<span data-ttu-id="30a55-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="30a55-143">**Element**</span></span>|<span data-ttu-id="30a55-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30a55-144">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30a55-145">Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="30a55-145">Impersonation</span></span>  <br/> |[<span data-ttu-id="30a55-146">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="30a55-146">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="30a55-p112">Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="30a55-p112">Identifies the user whom the client application is impersonating. This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="30a55-149">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="30a55-149">RequestVersion</span></span>  <br/> |[<span data-ttu-id="30a55-150">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="30a55-150">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="30a55-151">Gibt die Schemaversion für die Vorgangsanforderung an, die für eine Anforderung gilt.</span><span class="sxs-lookup"><span data-stu-id="30a55-151">Identifies the schema version for the operation request This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="30a55-152">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="30a55-152">ServerVersion</span></span>  <br/> |[<span data-ttu-id="30a55-153">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="30a55-153">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="30a55-p113">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="30a55-p113">Identifies the version of the server that responded to the request. This is applicable to a response.</span></span>  <br/> |
   
## <a name="convertid-operation-request-example"></a><span data-ttu-id="30a55-156">Convert-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="30a55-156">ConvertId operation request example</span></span>
<span data-ttu-id="30a55-157"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-157"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="30a55-158">Das folgende Beispiel einer **Konvertierungs** Anforderung zeigt, wie eine EWS-ID in einen Outlook Web App Bezeichner konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="30a55-158">The following example of a **ConvertId** request shows how to convert from an EWS identifier to an Outlook Web App identifier.</span></span> 
  
<span data-ttu-id="30a55-159">Das [RequestServerVersion](requestserverversion.md) -Element im SOAP-Header muss auf Exchange2007_SP1 oder höher festgelegt sein, damit dieser Vorgang funktioniert.</span><span class="sxs-lookup"><span data-stu-id="30a55-159">The [RequestServerVersion](requestserverversion.md) element in the SOAP header must be set to Exchange2007_SP1 or later for this operation to work.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30a55-160">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="30a55-160">The item identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <ConvertId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               DestinationFormat="OwaId">
      <SourceIds>
        <t:AlternateId Format="EwsId" Id="AAMkAGZhN2IxYTA0LWNiNzItN="
                       Mailbox="user1@example.com"/>
      </SourceIds>
    </ConvertId>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-response-example"></a><span data-ttu-id="30a55-161">Beispiel für eine Convert-Vorgangs Antwort</span><span class="sxs-lookup"><span data-stu-id="30a55-161">ConvertId operation response example</span></span>
<span data-ttu-id="30a55-162"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-162"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="30a55-163">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **Convert** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="30a55-163">The following example shows a successful response to a **ConvertId** request.</span></span> <span data-ttu-id="30a55-164">Dieses Antwortbeispiel enthält einen Outlook Web App Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="30a55-164">This response example contains an Outlook Web App identifier.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30a55-165">Die Outlook Web App-ID wurde verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30a55-165">The Outlook Web App identifier has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                         MajorBuildNumber="191" MinorBuildNumber="0" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <AlternateId xsi:type="t:AlternateIdType" Format="OwaId" Id="RgAAAAAS2%2" 
                         Mailbox="user@example.com" />
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="convertid-operation-error-response-example"></a><span data-ttu-id="30a55-166">Fehlerantwort Beispiel für Convert-Operation</span><span class="sxs-lookup"><span data-stu-id="30a55-166">ConvertId operation error response example</span></span>
<span data-ttu-id="30a55-167"><a name="bk_usingConvertId"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-167"><a name="bk_usingConvertId"> </a></span></span>

<span data-ttu-id="30a55-168">Das folgende Beispiel zeigt die Antwort auf eine Anforderung, die den falschen Typ des Bezeichnerformat enthält.</span><span class="sxs-lookup"><span data-stu-id="30a55-168">The following example shows the response to a request that contains the wrong type of identifier format.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <ServerVersionInfo MajorVersion="8" MinorVersion="1" 
                       MajorBuildNumber="206" MinorBuildNumber="0"
                       Version="Exchange2010" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ConvertIdResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <ConvertIdResponseMessage ResponseClass="Error">
          <MessageText>Id is malformed.</MessageText>
          <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
          <DescriptiveLinkKey>0</DescriptiveLinkKey>
        </ConvertIdResponseMessage>
      </ResponseMessages>
    </ConvertIdResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="version-differences"></a><span data-ttu-id="30a55-169">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="30a55-169">Version differences</span></span>
<span data-ttu-id="30a55-170"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-170"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

<span data-ttu-id="30a55-171">Das EWS-Bezeichnerformat wurde zwischen der ursprünglichen Veröffentlichungsversion von Exchange 2007 und Exchange 2007 Service Pack 1 (SP1) geändert.</span><span class="sxs-lookup"><span data-stu-id="30a55-171">The EWS identifier format changed between the initial release version of Exchange 2007 and Exchange 2007 Service Pack 1 (SP1).</span></span> <span data-ttu-id="30a55-172">Exchange Online im Rahmen von Office 365, Exchange Online und lokalen Versionen von Exchange, die mit Exchange 2010 beginnen, verwenden dasselbe von Exchange 2007 SP1 verwendete ID-Format.</span><span class="sxs-lookup"><span data-stu-id="30a55-172">Exchange Online as part of Office 365, Exchange Online, and on-premises versions of Exchange starting with Exchange 2010 use the same identifier format that Exchange 2007 SP1 uses.</span></span>
  
<span data-ttu-id="30a55-173">Mit dem **Konvertierungs** -ID-Vorgang werden Bezeichner für Öffentliche Ordner aus dem EWS-Bezeichner in die Speicher-ID in Exchange 2007 und Exchange 2010 konvertiert.</span><span class="sxs-lookup"><span data-stu-id="30a55-173">The **ConvertId** operation converts public folder identifiers from the EWS identifier to the store identifier in Exchange 2007 and Exchange 2010.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30a55-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a55-174">See also</span></span>
<span data-ttu-id="30a55-175"><a name="bk_ConvertIdVersionDiff"> </a></span><span class="sxs-lookup"><span data-stu-id="30a55-175"><a name="bk_ConvertIdVersionDiff"> </a></span></span>

- [<span data-ttu-id="30a55-176">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="30a55-176">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)
    
- [<span data-ttu-id="30a55-177">ConvertIdType</span><span class="sxs-lookup"><span data-stu-id="30a55-177">ConvertIdType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ConvertIdType.aspx)
    
- [<span data-ttu-id="30a55-178">ConvertId</span><span class="sxs-lookup"><span data-stu-id="30a55-178">ConvertId</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ExchangeServiceBinding.ConvertId.aspx)
    

