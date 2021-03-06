UPGRADE FROM 3.2 to 3.3
=======================

ClassLoader
-----------

 * The ApcClassLoader, WinCacheClassLoader and XcacheClassLoader classes have been deprecated
   in favor of the `--apcu-autoloader` option introduced in composer 1.3

DependencyInjection
-------------------

 * The `Reference` and `Alias` classes do not make service identifiers lowercase anymore.

 * Case insensitivity of service identifiers is deprecated and will be removed in 4.0.

 * Using the `PhpDumper` with an uncompiled `ContainerBuilder` is deprecated and
   will not be supported anymore in 4.0.

 * The `DefinitionDecorator` class is deprecated and will be removed in 4.0, use
   the `ChildDefinition` class instead.

EventDispatcher
---------------

 * The `ContainerAwareEventDispatcher` class has been deprecated.
   Use `EventDispatcher` with closure-proxy injection instead.

Finder
------

 * The `ExceptionInterface` has been deprecated and will be removed in 4.0.

FrameworkBundle
---------------

 * The `Symfony\Bundle\FrameworkBundle\DependencyInjection\Compiler\AddConsoleCommandPass` has been deprecated. Use `Symfony\Component\Console\DependencyInjection\AddConsoleCommandPass` instead.

HttpKernel
-----------

 * The `Psr6CacheClearer::addPool()` method has been deprecated. Pass an array of pools indexed
   by name to the constructor instead.

Security
--------

 * The `RoleInterface` has been deprecated. Extend the `Symfony\Component\Security\Core\Role\Role`
   class in your custom role implementations instead.

SecurityBundle
--------------

 * The `FirewallContext::getContext()` method has been deprecated and will be removed in 4.0.
   Use the `getListeners()` method instead.

TwigBridge
----------

 * The `TwigRendererEngine::setEnvironment()` method has been deprecated and will be removed
   in 4.0. Pass the Twig Environment as second argument of the constructor instead.
