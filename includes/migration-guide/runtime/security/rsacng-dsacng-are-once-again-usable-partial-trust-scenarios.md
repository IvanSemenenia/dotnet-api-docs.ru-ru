### <a name="rsacng-and-dsacng-are-once-again-usable-in-partial-trust-scenarios"></a><span data-ttu-id="460dc-101">RSACng и DSACng еще раз, можно использовать в сценариях частичного доверия</span><span class="sxs-lookup"><span data-stu-id="460dc-101">RSACng and DSACng are once again usable in Partial Trust scenarios</span></span>

|   |   |
|---|---|
|<span data-ttu-id="460dc-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="460dc-102">Details</span></span>|<span data-ttu-id="460dc-103">CngLightup (используется в несколько более высокого уровня crypto API-интерфейсы, такие как <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>) и <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> в некоторых случаях полагаться на полное доверие.</span><span class="sxs-lookup"><span data-stu-id="460dc-103">CngLightup (used in several higher-level crypto apis, such as <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>) and <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> in some cases rely on full trust.</span></span> <span data-ttu-id="460dc-104">К ним относятся методы P/Invoke не гарантируют <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> разрешений и пути кода где <xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType> имеет требования <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="460dc-104">These include P/Invokes without asserting <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> permissions, and code paths where <xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType> has permission demands for <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>.</span></span> <span data-ttu-id="460dc-105">Начиная с .NET Framework 4.6.2, чтобы переключиться в использовался CngLightup <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="460dc-105">Starting with the .NET Framework 4.6.2, CngLightup was used to switch to <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> wherever possible.</span></span> <span data-ttu-id="460dc-106">В результате приложения частичного доверия, которые успешно использовать <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType> началось с ошибкой и выдать <xref:System.Security.SecurityException> исключения. Это изменение добавляет необходимые утверждения, чтобы все функции с помощью CngLightup нет необходимых разрешений.</span><span class="sxs-lookup"><span data-stu-id="460dc-106">As a result, partial trust apps that successfully used <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType> began to fail and throw <xref:System.Security.SecurityException> exceptions.This change adds the required asserts so that all functions using CngLightup have the required permissions.</span></span>|
|<span data-ttu-id="460dc-107">Предложение</span><span class="sxs-lookup"><span data-stu-id="460dc-107">Suggestion</span></span>|<span data-ttu-id="460dc-108">Если это изменение в платформе .NET Framework 4.6.2 негативное влияние на приложения частичного доверия, обновление для .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="460dc-108">If this change in the .NET Framework 4.6.2 has negatively impacted your partial trust apps, upgrade to the .NET Framework 4.7.1.</span></span>|
|<span data-ttu-id="460dc-109">Область</span><span class="sxs-lookup"><span data-stu-id="460dc-109">Scope</span></span>|<span data-ttu-id="460dc-110">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="460dc-110">Edge</span></span>|
|<span data-ttu-id="460dc-111">Версия</span><span class="sxs-lookup"><span data-stu-id="460dc-111">Version</span></span>|<span data-ttu-id="460dc-112">4.6.2</span><span class="sxs-lookup"><span data-stu-id="460dc-112">4.6.2</span></span>|
|<span data-ttu-id="460dc-113">Тип</span><span class="sxs-lookup"><span data-stu-id="460dc-113">Type</span></span>|<span data-ttu-id="460dc-114">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="460dc-114">Runtime</span></span>|
|<span data-ttu-id="460dc-115">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="460dc-115">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.DSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.LegalKeySizes?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.CreateSignature(System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.VerifySignature(System.Byte[],System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Decrypt(System.Byte[],System.Security.Cryptography.RSAEncryptionPadding)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.SignHash(System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|
