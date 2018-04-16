### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a><span data-ttu-id="6a57b-101">Создание edmx Entity Framework с Visual Studio 2013 может завершиться ошибкой MSB4062 при использовании в EntityDeploySplit или EntityClean задач</span><span class="sxs-lookup"><span data-stu-id="6a57b-101">Building an Entity Framework edmx with Visual Studio 2013 can fail with error MSB4062 if using the EntityDeploySplit or EntityClean tasks</span></span>

|   |   |
|---|---|
|<span data-ttu-id="6a57b-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="6a57b-102">Details</span></span>|<span data-ttu-id="6a57b-103">Средства MSBuild 12.0 (включенный в Visual Studio 2013) изменить расположения файлов MSBuild, вызывают старых файлов целей Entity Framework недопустим.</span><span class="sxs-lookup"><span data-stu-id="6a57b-103">MSBuild 12.0 tools (included in Visual Studio 2013) changed MSBuild file locations, causing older Entity Framework targets files to be invalid.</span></span> <span data-ttu-id="6a57b-104">В результате задачи <code>EntityDeploySplit</code> и <code>EntityClean</code> завершаются ошибкой, так как они не могут найти <code>Microsoft.Data.Entity.Build.Tasks.dll</code>.</span><span class="sxs-lookup"><span data-stu-id="6a57b-104">The result is that <code>EntityDeploySplit</code> and <code>EntityClean</code> tasks fail because they are unable to find <code>Microsoft.Data.Entity.Build.Tasks.dll</code>.</span></span> <span data-ttu-id="6a57b-105">Обратите внимание, что этот разрыв связи с изменениями набор инструментов (MSBuild/VS) из-за изменения .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6a57b-105">Note that this break is because of a toolset (MSBuild/VS) change, not because of a .NET Framework change.</span></span> <span data-ttu-id="6a57b-106">Оно происходит только при обновлении средств разработчика, а не просто при обновлении .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6a57b-106">It will only occur when upgrading developer tools, not when merely upgrading the .NET Framework.</span></span>|
|<span data-ttu-id="6a57b-107">Предложение</span><span class="sxs-lookup"><span data-stu-id="6a57b-107">Suggestion</span></span>|<span data-ttu-id="6a57b-108">Для работы с новой начало макета MSBuild в .NET Framework 4.6 фиксируются Entity Framework целевых файлов.</span><span class="sxs-lookup"><span data-stu-id="6a57b-108">Entity Framework targets files are fixed to work with the new MSBuild layout beginning in the .NET Framework 4.6.</span></span> <span data-ttu-id="6a57b-109">Проблема будет решена после обновления до этой версии.</span><span class="sxs-lookup"><span data-stu-id="6a57b-109">Upgrading to that version of the Framework will fix this issue.</span></span> <span data-ttu-id="6a57b-110">Кроме того, [это](http://stackoverflow.com/a/24249247/131944) решение можно использовать для исправления файлов целей построения напрямую.</span><span class="sxs-lookup"><span data-stu-id="6a57b-110">Alternatively, [this](http://stackoverflow.com/a/24249247/131944) workaround can be used to patch the targets files directly.</span></span>|
|<span data-ttu-id="6a57b-111">Область</span><span class="sxs-lookup"><span data-stu-id="6a57b-111">Scope</span></span>|<span data-ttu-id="6a57b-112">Значительно</span><span class="sxs-lookup"><span data-stu-id="6a57b-112">Major</span></span>|
|<span data-ttu-id="6a57b-113">Версия</span><span class="sxs-lookup"><span data-stu-id="6a57b-113">Version</span></span>|<span data-ttu-id="6a57b-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="6a57b-114">4.5.1</span></span>|
|<span data-ttu-id="6a57b-115">Тип</span><span class="sxs-lookup"><span data-stu-id="6a57b-115">Type</span></span>|<span data-ttu-id="6a57b-116">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="6a57b-116">Retargeting</span></span>|
