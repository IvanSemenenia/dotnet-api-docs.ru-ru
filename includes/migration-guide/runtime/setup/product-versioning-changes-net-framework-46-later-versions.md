### <a name="product-versioning-changes-in-the-net-framework-46-and-later-versions"></a><span data-ttu-id="f820c-101">Изменения управления версиями продукта в .NET Framework 4.6 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="f820c-101">Product versioning changes in the .NET Framework 4.6 and later versions</span></span>

|   |   |
|---|---|
|<span data-ttu-id="f820c-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="f820c-102">Details</span></span>|<span data-ttu-id="f820c-103">Управление версиями продукта отличается от предыдущих версий платформы .NET Framework и особенно с .NET Framework 4, 4.5, 4.5.1, и 4.5.2.The ниже приведены подробные изменения:</span><span class="sxs-lookup"><span data-stu-id="f820c-103">Product versioning has changed from the previous releases of the .NET Framework, and particularly from the .NET Framework 4, 4.5, 4.5.1, and 4.5.2.The following are the detailed changes:</span></span><ul><li><span data-ttu-id="f820c-104">Значение <code>Version</code> входа в <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full</code> ключ был изменен на <code>4.6.xxxxx</code> для .NET Framework 4.6 и ее доработанные выпуски, а также <code>4.7.xxxxx</code> 4.7 .NET Framework и 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="f820c-104">The value of the <code>Version</code> entry in the <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full</code> key has changed to <code>4.6.xxxxx</code> for the .NET Framework 4.6 and its point releases, and to <code>4.7.xxxxx</code> for the .NET Framework 4.7 and 4.7.1.</span></span> <span data-ttu-id="f820c-105">В .NET Framework 4.5, 4.5.1 и 4.5.2 использовался формат <code>4.5.xxxxx</code>.</span><span class="sxs-lookup"><span data-stu-id="f820c-105">In the .NET Framework 4.5, 4.5.1, and 4.5.2, it had the format <code>4.5.xxxxx</code>.</span></span></li><li><span data-ttu-id="f820c-106">Управление версиями файлов и продукта для .NET Framework было изменено с более ранней схемы управления версиями 4.0.30319.x 4.6.X.0 для .NET Framework 4.6 и ее доработанные выпуски, а также 4.7.X.0 для .NET Framework 4.7 и 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="f820c-106">The file and product versioning for .NET Framework files has changed from the earlier versioning scheme of 4.0.30319.x to 4.6.X.0 for the .NET Framework 4.6 and its point releases, and to 4.7.X.0 for the .NET Framework 4.7 and 4.7.1.</span></span> <span data-ttu-id="f820c-107">При просмотре свойств файла после щелчка правой кнопкой мыши файл, можно увидеть эти новые значения.</span><span class="sxs-lookup"><span data-stu-id="f820c-107">You can see these new values when you view the file's Properties after right-clicking on a file.</span></span></li><li><span data-ttu-id="f820c-108"><xref:System.Reflection.AssemblyFileVersionAttribute> И <xref:System.Reflection.AssemblyInformationalVersionAttribute> атрибуты управляемых сборок имеют значения версии в виде 4.6.X.0 для .NET Framework 4.6 и ее доработанные выпуски и 4.7.X.0 4.7 .NET Framework и 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="f820c-108">The <xref:System.Reflection.AssemblyFileVersionAttribute> and <xref:System.Reflection.AssemblyInformationalVersionAttribute> attributes for managed assemblies have Version values in the form 4.6.X.0 for the .NET Framework 4.6 and its point releases, and 4.7.X.0 for the .NET Framework 4.7 and 4.7.1.</span></span></li><li><span data-ttu-id="f820c-109">В платформе .NET Framework 4.6, 4.6.1, 4.6.2, 4.7 и 4.7.1 <xref:System.Environment.Version?displayProperty=nameWithType> свойство возвращает исправленную строку версии <code>4.0.30319.42000</code>.</span><span class="sxs-lookup"><span data-stu-id="f820c-109">In the .NET Framework 4.6, 4.6.1, 4.6.2, 4.7, and 4.7.1, the <xref:System.Environment.Version?displayProperty=nameWithType> property returns the fixed version string <code>4.0.30319.42000</code>.</span></span> <span data-ttu-id="f820c-110">В .NET Framework 4, 4.5, 4.5.1 и 4.5.2 оно возвращает строки версии в формате <code>4.0.30319.xxxxx</code> (например, &quot;4.0.30319.18010&quot;).</span><span class="sxs-lookup"><span data-stu-id="f820c-110">In the .NET Framework 4, 4.5, 4.5.1, and 4.5.2, it returns version strings in the format <code>4.0.30319.xxxxx</code> (for example, &quot;4.0.30319.18010&quot;).</span></span> <span data-ttu-id="f820c-111">Обратите внимание, что не рекомендуется создание новых зависимостей в свойство Environment.Version кода приложения.</span><span class="sxs-lookup"><span data-stu-id="f820c-111">Note that we do not recommend application code taking any new dependency on the Environment.Version property.</span></span></li></ul><span data-ttu-id="f820c-112">Дополнительные сведения см. в разделе [как: определить, какие .NET Framework версий](~/docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md).</span><span class="sxs-lookup"><span data-stu-id="f820c-112">For more information, see [How to: Determine which .NET Framework Versions Are Installed](~/docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md).</span></span>|
|<span data-ttu-id="f820c-113">Предложение</span><span class="sxs-lookup"><span data-stu-id="f820c-113">Suggestion</span></span>|<span data-ttu-id="f820c-114">В общем случае приложения для обнаружения таких сведений, как версия среды выполнения .NET Framework и каталог установки, должны использовать следующие рекомендуемые методы:</span><span class="sxs-lookup"><span data-stu-id="f820c-114">In general, applications should depend on the recommended techniques for detecting such things as the runtime version of the .NET Framework and the installation directory:</span></span><ul><li><span data-ttu-id="f820c-115">Инструкции для определения версии среды выполнения .NET см. в разделе [Практическое руководство. Определение установленных версий платформы .NET Framework](~/docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md).</span><span class="sxs-lookup"><span data-stu-id="f820c-115">To detect the runtime version of the .NET Framework, see [How to: Determine Which .NET Framework Versions Are Installed](~/docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md).</span></span></li><li><span data-ttu-id="f820c-116">Чтобы определить путь установки платформы .NET Framework, используйте значение записи <code>InstallPath</code> в ключе <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full</code>.</span><span class="sxs-lookup"><span data-stu-id="f820c-116">To determine the installation path for the .NET Framework, use the value of the <code>InstallPath</code> entry in the <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\NET Framework Setup\NDP\v4\Full</code> key.</span></span></li></ul> <blockquote> [!IMPORTANT] <span data-ttu-id="f820c-117">Имя подраздела — <code>NET Framework Setup</code>, а не <code>.NET Framework Setup</code>.</span><span class="sxs-lookup"><span data-stu-id="f820c-117">The subkey name is <code>NET Framework Setup</code>, not <code>.NET Framework Setup</code>.</span></span></blockquote> <ul><li><span data-ttu-id="f820c-118">Чтобы определить путь к каталогу общеязыковой среды выполнения .NET Framework, вызовите метод <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetRuntimeDirectory?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f820c-118">To determine the directory path to the .NET Framework common language runtime, call the <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetRuntimeDirectory?displayProperty=nameWithType> method.</span></span></li><li><span data-ttu-id="f820c-119">Чтобы получить версию среды CLR, вызовите метод <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetSystemVersion?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f820c-119">To get the CLR version, call the <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetSystemVersion?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="f820c-120">Для .NET Framework 4 и ее доработанных выпусков (.NET Framework 4.5, 4.5.1, 4.5.2 и .NET Framework 4.6, 4.6.1, 4.6.2 4.7 и 4.7.1), он возвращает строку v4.0.30319.</span><span class="sxs-lookup"><span data-stu-id="f820c-120">For the .NET Framework 4 and its point releases (the .NET Framework 4.5, 4.5.1, 4.5.2, and .NET Framework 4.6, 4.6.1, 4.6.2, 4.7, and 4.7.1), it returns the string v4.0.30319.</span></span></li></ul>|
|<span data-ttu-id="f820c-121">Область</span><span class="sxs-lookup"><span data-stu-id="f820c-121">Scope</span></span>|<span data-ttu-id="f820c-122">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="f820c-122">Minor</span></span>|
|<span data-ttu-id="f820c-123">Версия</span><span class="sxs-lookup"><span data-stu-id="f820c-123">Version</span></span>|<span data-ttu-id="f820c-124">4.6</span><span class="sxs-lookup"><span data-stu-id="f820c-124">4.6</span></span>|
|<span data-ttu-id="f820c-125">Тип</span><span class="sxs-lookup"><span data-stu-id="f820c-125">Type</span></span>|<span data-ttu-id="f820c-126">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="f820c-126">Runtime</span></span>|
