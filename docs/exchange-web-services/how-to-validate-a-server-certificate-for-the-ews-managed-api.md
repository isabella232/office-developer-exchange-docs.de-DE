---
title: Überprüfen ein Serverzertifikats für die verwaltete EWS-API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Hier erfahren Sie, wie Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen und referenzieren, sodass Sie verwaltete EWS-API Anforderungen an einen Exchange-Server stellen können.
localization_priority: Priority
ms.openlocfilehash: 195c51ca71890d6092e4182d23990bb528d37095
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456780"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="005db-103">Überprüfen ein Serverzertifikats für die verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="005db-103">Validate a server certificate for the EWS Managed API</span></span>

<span data-ttu-id="005db-104">Hier erfahren Sie, wie Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen und referenzieren, sodass Sie verwaltete EWS-API Anforderungen an einen Exchange-Server stellen können.</span><span class="sxs-lookup"><span data-stu-id="005db-104">Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.</span></span>
  
<span data-ttu-id="005db-105">Standardmäßig verwenden Versionen von Exchange, die mit Exchange 2007 SP1 beginnen, selbstsignierte X509-Zertifikate, um Anrufe von EWS zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="005db-105">By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS.</span></span> <span data-ttu-id="005db-106">Wenn Sie die verwaltete EWS-API verwenden, müssen Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen. Andernfalls tritt für verwaltete EWS-API-Anforderungen ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="005db-106">When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail.</span></span> <span data-ttu-id="005db-107">Wenn Sie den AutoErmittlungsdienst verwenden, schlägt der Aufruf der verwaltete EWS-API Auto Ermittlungsmethode mit einem **AutodiscoverLocalException** -Fehler fehl.</span><span class="sxs-lookup"><span data-stu-id="005db-107">If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error.</span></span> <span data-ttu-id="005db-108">Wenn Sie einen von Webdiensten generierten Webdienstproxy verwenden, müssen Sie möglicherweise auch eine Validierungsrückruf Methode erstellen, je nachdem, wie der Proxy erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="005db-108">If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.</span></span> 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a><span data-ttu-id="005db-109">Voraussetzungen für das Erstellen einer Validierungsrückruf Methode</span><span class="sxs-lookup"><span data-stu-id="005db-109">Prerequisites for creating a validation callback method</span></span>
<span data-ttu-id="005db-110"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="005db-110"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="005db-111">Um die Überprüfung eines Serverzertifikats einzurichten, stellen Sie sicher, dass Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="005db-111">To set up to validate a server certificate, ensure that the following are true:</span></span> 
  
- <span data-ttu-id="005db-112">Ihr Exchange-Server verwendet ein selbstsigniertes Zertifikat für EWS.</span><span class="sxs-lookup"><span data-stu-id="005db-112">Your Exchange server is using a self-signed certificate for EWS.</span></span> <span data-ttu-id="005db-113">Wenn der Administrator ein gültiges Zertifikat installiert hat, das auf ein Stammzertifikat ablauft, müssen Sie keine Validierungsrückruf Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="005db-113">If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.</span></span> 
    
- <span data-ttu-id="005db-114">Sie erstellen eine verwaltete Anwendung, die einen Verweis auf die folgenden erforderlichen .NET Framework Namespaces enthält:</span><span class="sxs-lookup"><span data-stu-id="005db-114">You are creating a managed application that includes a reference to the following required .NET Framework namespaces:</span></span> 
    
  - <span data-ttu-id="005db-115">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="005db-115">**System.Net**</span></span>
  - <span data-ttu-id="005db-116">**System .net. Security**</span><span class="sxs-lookup"><span data-stu-id="005db-116">**System.Net.Security**</span></span>  
  - <span data-ttu-id="005db-117">**System. Security. Cryptography. X509Certificates**</span><span class="sxs-lookup"><span data-stu-id="005db-117">**System.Security.Cryptography.X509Certificates**</span></span>
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="005db-118">Beispiel: Callback-Methode zum Überprüfen eines Serverzertifikats für den verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="005db-118">Example: Callback method to validate a server certificate for the EWS Managed API</span></span>
<span data-ttu-id="005db-119"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="005db-119"><a name="bk_example"> </a></span></span>

<span data-ttu-id="005db-120">Das folgende Codebeispiel zeigt, wie Sie eine X509-Zertifikat Validierungsrückruf Methode für die verwaltete EWS-API erstellen.</span><span class="sxs-lookup"><span data-stu-id="005db-120">The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API.</span></span> <span data-ttu-id="005db-121">Diese Methode überprüft ein X509-Zertifikat und gibt nur dann true zurück, wenn eines der folgenden Kriterien erfüllt wird:</span><span class="sxs-lookup"><span data-stu-id="005db-121">This method will validate an X509 certificate and only return true when either of the following criteria are met:</span></span> 
  
- <span data-ttu-id="005db-122">Das Zertifikat ist gültig und verfolgt wieder ein gültiges Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="005db-122">The certificate is valid and traces back to a valid root certificate.</span></span>    
- <span data-ttu-id="005db-123">Das Zertifikat ist gültig und wird von dem Server selbst signiert, von dem es zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="005db-123">The certificate is valid and is self-signed by the server that returned it.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="005db-124">Die Rückrufmethode für die Zertifikatüberprüfung in diesem Beispiel bietet ausreichende Sicherheit für die Entwicklung und das Testen von verwaltete EWS-API Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="005db-124">The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications.</span></span> <span data-ttu-id="005db-125">Es stellt jedoch möglicherweise keine ausreichende Sicherheit für die bereitgestellte Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="005db-125">However, it might not provide sufficient security for your deployed application.</span></span> <span data-ttu-id="005db-126">Sie sollten immer sicherstellen, dass die von Ihnen verwendete Rückrufmethode für die Zertifikatüberprüfung die Sicherheitsanforderungen Ihrer Organisation erfüllt.</span><span class="sxs-lookup"><span data-stu-id="005db-126">You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.</span></span> 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

<span data-ttu-id="005db-127">Sie verwenden die **ServicePointManager** -Klasse im .net **System.net** -Namespace, um eine Validierungsrückruf Methode einzubinden, indem Sie die **ServerCertificateValidationCallback** -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="005db-127">You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property.</span></span> <span data-ttu-id="005db-128">Sie können Code wie im folgenden Codebeispiel verwenden, um die **ServerCertificateValidationCallback** -Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="005db-128">You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.</span></span> 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a><span data-ttu-id="005db-129">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="005db-129">Next steps</span></span>
<span data-ttu-id="005db-130"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="005db-130"><a name="bk_example"> </a></span></span>

<span data-ttu-id="005db-131">Nachdem Sie die Validierungsrückruf Methode für die verwaltete EWS-API erstellt haben, können Sie den AutoErmittlungsdienst verwenden, um Verbindungspunkte und Benutzer-und Domäneneinstellungen von einem Exchange-Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="005db-131">After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server.</span></span> <span data-ttu-id="005db-132">Weitere Informationen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="005db-132">For more information, see the following articles:</span></span>
  
- [<span data-ttu-id="005db-133">Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten</span><span class="sxs-lookup"><span data-stu-id="005db-133">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    
- [<span data-ttu-id="005db-134">Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="005db-134">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="005db-135">Abrufen von Domäneneinstellungen von einem Exchange-Server</span><span class="sxs-lookup"><span data-stu-id="005db-135">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a><span data-ttu-id="005db-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="005db-136">See also</span></span>

- [<span data-ttu-id="005db-137">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="005db-137">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)  
- [<span data-ttu-id="005db-138">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="005db-138">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    

