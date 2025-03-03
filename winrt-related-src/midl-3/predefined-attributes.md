---
description: There are a number of pre-defined custom attributes that allow you to control the name and IID for compiler-synthesized interfaces.
title: Predefined attributes (MIDL 3.0)
ms.date: 04/23/2018
ms.topic: reference
keywords: windows 10, uwp, winrt, api, reference, idl, midl, 3.0, 3, midl3
ms.localizationpriority: medium
---

# Predefined attributes (MIDL 3.0)
There are a number of pre-defined custom attributes that allow you to control the name and interface identifier (IID) for compiler-synthesized interfaces. These attributes allow you to control the versioning and binary API of your
class at a fine-grained level.

If you're a component developer and/or a library author, then you may wish to use these attributes to ensure that your components remain binary-stable from one version to the next.

If you're an application developer, then in general you won't need to use these attributes because you'll recompile your application after revisioning your types.

## The `[allowforweb]` attribute
For details on the use and purpose of the `allowforweb` attribute, see the [AllowForWebAttribute class](/uwp/api/windows.foundation.metadata.allowforwebattribute).

## The `[constructor_name]` attribute
The `constructor_name` attribute specifies the name and IID of the
factory interface that contains the constructor members. See [Synthesizing interfaces](synthesizing-interfaces.md) for more info about factory interfaces.

> [!NOTE]
> A factory interface is only applicable to a sealed class with non-default constructors, or to an unsealed class with default and/or non-default constructors.

In the example below, the protected **Block** constructor is placed in the
**IBlockFactory** interface, and that interface has the specified IID.

```idl
[constructor_name("Windows.UI.Xaml.Documents.IBlockFactory", 07110532-4f59-4f3b-9ce5-25784c430507)]
...
unsealed runtimeclass Block : Windows.UI.Xaml.Documents.TextElement
{
    ...
    protected Block();
    ...
}
```

As a result, when your class description doesn't otherwise reference an
interface, but when one is needed to implement the class, the MIDL 3.0
compiler synthesizes and adds interfaces, as necessary.

## The `[contract]` attribute
Do not use the `contract` attribute in your own APIs; it only has meaning for built-in Windows APIs.

The `contract` attribute specifies the name and version of the Windows 10 API contract (see [Programming with extension SDKs](../extension-sdks/device-families-overview.md)) in which the attributed type and/or member was first introduced into Windows (hence it is not meaningful for APIs not delivered as part of Windows). The attribute takes the form `[contract(ContractName, ContractVersion)]`, and it appears before the item to which it applies.

## The `[default]` attribute
If you don't specify a default interface, then the MIDL 3.0 compiler chooses the first instance interface. To override this selection, insert The `default` attribute before the interface that you want to be the default interface.

```idl
// Declaring an external interface as the default
runtimeclass C : [default]I { ... }

// Declaring a specific exclusiveto interface as the default.
// This is very unusual.
runtimeclass C
{
    ...

    [default][interface_name(...)]
    {
        ...
    }
}
```

## The `[default_interface]` attribute

The `default_interface` attribute is used to force the generation of a default interface where one wouldn't otherwise be generated. In the example below, **StateTriggerBase** has no need for a default interface (because it has no public nonstatic members), so it's only the presence of the `default_interface` attribute that causes one (named **IStateTriggerBase**) to be generated.

```idl
[default_interface]
unsealed runtimeclass StateTriggerBase
{
    protected void SetActive(Boolean IsActive);
};
```

## The `[default_overload]` attribute

> [!NOTE]
> This attribute is not supported for constructors. If you can't overload your constructors by arity, then you can define overloaded factory methods such as the **CreateFromUri** and **CreateFromStream** examples shown in the last code snippet in this section.

The `default_overload` attribute represents the [**DefaultOverloadAttribute**](/uwp/api/windows.foundation.metadata.defaultoverloadattribute) class, which indicates that a method is the default overload method. This section walks you through the *reason* for, and usage guidelines for, the `[default_overload]` attribute.

You can freely overload Windows Runtime methods by *arity*. That is, you can define multiple methods with the same name, as long as each one takes a different number of arguments. For usability purposes, we recommend that you add new parameters to the end, and that the behavior of the shorter-parameter-list function be equivalent to calling the longer-parameter-list function with (scenario-specific) natural defaults for the missing parameters.

```idl
runtimeclass Widget
{
    void Start();
    void Start(StartMode mode);
    void Start(StartMode mode, Widget parent);
}
```

In the example above, **Start** can be called with two parameters to specify a start mode and a parent widget. If you omit the parent widget, then it defaults to null. And if you omit the mode, then it starts in some scenario-specific default mode.

We use [**DeviceInformation.CreateWatcher**](/uwp/api/windows.devices.enumeration.deviceinformation.createwatcher) in this next example.

```idl
runtimeclass DeviceInformation
{
    static DeviceWatcher CreateWatcher();
    static DeviceWatcher CreateWatcher(DeviceClass deviceClass);
    static DeviceWatcher CreateWatcher(String aqsFilter);
    static DeviceWatcher CreateWatcher(String aqsFilter,
                                       IIterable<String> additionalProperties);
    static DeviceWatcher CreateWatcher(String aqsFilter,
                                       IIterable<String> additionalProperties,
                                       DeviceInformationKind kind);
}
```

In that example there are five overloads, and most of them follow the recommended pattern of having each new overload be an extension of the previous overload.

If you decide to have multiple overloads of a method with the same number of parameters, then you get a compiler error:

  *The 1-parameter overloads of DeviceInformation.CreateWatcher must have exactly one method specified as the default overload by decorating it with Windows.Foundation.Metadata.DefaultOverloadAttribute.*

The reason being that some programming languages are dynamically-typed. JavaScript and Python are two examples. For these languages, the selection of the overload considers only the number of parameters, and not their types. This means that a JavaScript call to `DeviceInformation.createWatcher(v);` is ambiguous&mdash;should *v* be coerced to a **DeviceClass**, or to a **String**?

To resolve the ambiguity, you need to apply the `[default_overload]` attribute to one of the methods. But how do you choose which one?

You should choose the default overload so that the functionality of the non-default overloads is still available by other means, typically by one of the other overloads.

In the **DeviceInformation.CreateWatcher** example, the functionality of the **String** overload can be obtained by calling the **String**, **IIterable\<String>** overload, and passing an empty list of properties. On the other hand, the **DeviceClass** overload is the only way to create a **DeviceWatcher** that is filtered to a **DeviceClass**.

That makes the **DeviceClass** method the clear winner. So you indicate that by applying the `[default_overload]` attribute to that overload.

```idl
runtimeclass DeviceInformation
{
    static DeviceWatcher CreateWatcher();
    [default_overload]
    static DeviceWatcher CreateWatcher(DeviceClass deviceClass);
    static DeviceWatcher CreateWatcher(String aqsFilter);
    static DeviceWatcher CreateWatcher(String aqsFilter,
                                       IIterable<String> additionalProperties);
    static DeviceWatcher CreateWatcher(String aqsFilter,
                                       IIterable<String> additionalProperties,
                                       DeviceInformationKind kind);
}
```

What if there's no winner because all of the conflicting overloads provide unique functionality not available from other overloads?

```idl
runtimeclass Widget
{
    static Widget Create(Uri source);
    static Widget Create(IInputStream source);
}
```

Our hypothetical **Widget** object can be created from a **Uri**, or created from an input stream. If we mark one as the default overload, then dynamically-typed programming languages completely lose access to the other one.

To solve this problem, give the two versions different names so that they aren't overloaded.

```idl
runtimeclass Widget
{
    static Widget CreateFromUri(Uri source);
    static Widget CreateFromStream(IInputStream source);
}
```

Now both creation patterns are available to all languages.

Also see [Method overloading](../winrt-cref/winrt-type-system.md#method-overloading) and [Class-based projection](../winrt-cref/winrt-type-system.md#class-based-projection).

## The `[interface_name]` attribute
The `interface_name` attribute specifies the name and IID of the
interface that contains the instance members of the class. By default, the compiler assigns interface names using the same unique numbering algorithm that it uses for [methods](#the-method_name-attribute).

In the example below, the `interface_name` attribute applied to the
runtimeclass specifies the name and IID of the interface that contains
all instance members of the class that are not otherwise assigned to an
interface. So, **LineHeight**, **LineStackingStrategy**, **Margin**, and **TextAlignment** are members of the **IBlock** interface.

However, **HorizontalTextAlignment** is a member of the **IBlock2** interface,
because of the `interface_name` attribute encompassing that member.

```idl
[interface_name("Windows.UI.Xaml.Documents.IBlock", 4bce0016-dd47-4350-8cb0-e171600ac896)]
...
unsealed runtimeclass Block : Windows.UI.Xaml.Documents.TextElement
{
    ...
    Double LineHeight;
    Windows.UI.Xaml.LineStackingStrategy LineStackingStrategy;
    Windows.UI.Xaml.Thickness Margin;
    Windows.UI.Xaml.TextAlignment TextAlignment;

    [interface_name("Windows.UI.Xaml.Documents.IBlock2", 5ec7bdf3-1333-4a92-8318-6caedc12ef89)]
    {
        Windows.UI.Xaml.TextAlignment HorizontalTextAlignment;
    }
    ...
}
```

You can also use the `interface_name` attribute to force the generation of an interface. In the example below, **StateTriggerBase** has no need for **IStateTriggerBase**, and it's only the presence of the `interface_name` attribute that causes it to be generated.

```idl
[interface_name("Windows.UI.Xaml.IStateTriggerBase", 48b20698-af06-466c-8052-93666dde0e49)]
unsealed runtimeclass StateTriggerBase
{
    protected void SetActive(Boolean IsActive);
};
```

As a result, when your class description doesn't otherwise reference an interface, but when one is needed to implement the class, the MIDL 3.0 compiler synthesizes and adds interfaces, as necessary.

If you use the `default_interface` unnecessarily, then MIDL 3.0 generates an extra *empty* interface, and makes that the default.

## The `[method_name]` attribute
Every Windows Runtime interface has an equivalent Application Binary
Interface (ABI) interface. The ABI interface requires that all members
have unique names. There are two cases in MIDL 3.0 where members either
don't have a name, or don't have a unique name.

- constructors, and
- two or more overloaded methods.

In these cases, the MIDL 3.0 compiler synthesizes a unique
member name, as necessary.

By default, the compiler assigns constructor methods the names &lt;*className*&gt;, &lt;*className*&gt;2, &lt;*className*&gt;3, and so on for the equivalent methods in the ABI interface. In other words, the smallest unused integer numeral suffix (increasing from 2) is added to make the constructor method name unique.

Similarly, for overloaded methods, for the first method in a series of overloads (in lexical order), the compiler uses the original method name for the equivalent ABI interface method. Subsequent overloads are made unique by adding to the original name the smallest unused integer numeral suffix (increasing from 2).

For example, the following IDL declares three overloads of **DoWork**, and two overloads of a different method named **DoWork3**.

```idl
void DoWork(Int32 x);
void DoWork3(Int32 x);
void DoWork(Int32 x, Int32 y);
void DoWork(Int32 x, Int32 y, Int32 z);
void DoWork3(Int32 x, Int32 y);
```

By default (since the name **DoWork3** is already taken), the compiler gives to the three overloads of **DoWork** the names
- **DoWork**
- **DoWork2**
- **DoWork4**.

**DoWork3** is *not* a **DoWork** overload. By default, the compiler gives to the two overloads of **DoWork3** the names
- **DoWork3**
- **DoWork32**.

In vtable order, then, the functions will appear as

- **DoWork**
- **DoWork3**
- **DoWork2**
- **DoWork4**
- **DoWork32**

You can override the compiler's default name assignment using the
`method_name` attribute.

In this next example, we instruct the compiler to use the name
**CreateInstance** for the **Block** default constructor member.

```idl
unsealed runtimeclass Block : Windows.UI.Xaml.Documents.TextElement
{
    ...
    [method_name("CreateInstance")] protected Block();
    ...
}
```

## The `[static_name]` attribute
The `static_name` attribute specifies the name and IID of the interface
that contains static members of the class.

In this next example, the `static_name` attribute applied to the runtimeclass
specifies the name and IID of the interface that contains all static
members of the class that are not otherwise assigned to an interface. So, **LineHeightProperty**, **LineStackingStrategyProperty**, **MarginProperty**, and **TextAlignmentProperty** are members of the
**IBlockStatics** interface.

However, **HorizontalTextAlignmentProperty** is a member of the
**IBlockStatics2** interface, because of the `static_name` attribute
encompassing that member.

```idl
[static_name("Windows.UI.Xaml.Documents.IBlockStatics", f86a8c34-8d18-4c53-aebd-91e610a5e010)]
...
unsealed runtimeclass Block : Windows.UI.Xaml.Documents.TextElement
{
    ...
    static Windows.UI.Xaml.DependencyProperty LineHeightProperty{ get; };
    static Windows.UI.Xaml.DependencyProperty LineStackingStrategyProperty{ get; };
    static Windows.UI.Xaml.DependencyProperty MarginProperty{ get; };
    static Windows.UI.Xaml.DependencyProperty TextAlignmentProperty{ get; };

    [static_name("Windows.UI.Xaml.Documents.IBlockStatics2", af01a4d6-03e3-4cee-9b02-2bfc308b27a9)]
    {
        static Windows.UI.Xaml.DependencyProperty HorizontalTextAlignmentProperty{ get; };
    }
    ...
}
```