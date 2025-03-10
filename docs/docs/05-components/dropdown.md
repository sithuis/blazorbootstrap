﻿---
title: Blazor Dropdown Component
description: Dropdowns are toggleable, contextual overlays for displaying lists of links and more. They are toggled by clicking, not by hovering; this is an intentional design decision'by bootstrap.
image: https://i.imgur.com/beAr31J.png

sidebar_label: Dropdown
sidebar_position: 11
---

# Blazor Dropdown

Dropdowns are toggleable, contextual overlays for displaying lists of links and more. 
They are toggled by clicking, not by hovering; this is an intentional design decision'by bootstrap.

<img src="https://i.imgur.com/beAr31J.png" alt="Blazor Bootstrap: Dropdown component" />

## Dropdown Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| AutoClose | bool | Enables or disables the auto close. | | true | 1.10.0 |
| AutoCloseBehavior | `DropdownAutoCloseBehavior` | Gets or sets the auto close behavior of the dropdown. | | `DropdownAutoCloseBehavior.Both` | 1.10.0 |
| ChildContent | RenderFragment | Specifies the content to be rendered inside the Dropdown. | | | 1.10.0 |
| Direction | `DropdownDirection` | Gets or sets the direction of the dropdown menu. | | `DropdownDirection.Dropdown` | 1.10.0 |
| Disabled | bool | Gets or sets whether the dropdown menu is disabled. | | false | 1.10.3 |
| Size | `Size` | Gets or sets the size of the dropdown. | | `Size.None` | 1.10.3 |
| Split | bool | Gets or sets the toggle button split behavior. | | false | 1.10.0 |

## DropdownToggleButton Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| ChildContent | RenderFragment | Specifies the content to be rendered inside the DropdownToggleButton. | | | 1.10.0 |
| Color | `ButtonColor` | Gets or sets the button color. | | | 1.10.0 |
| TabIndex | `int?` | If defined, indicates that its element can be focused and can participates in sequential keyboard navigation. | | | 1.10.0 |

## DropdownActionButton Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| ChildContent | RenderFragment | Specifies the content to be rendered inside the DropdownActionButton. | | | 1.10.0 |
| Color | `ButtonColor` | Gets or sets the button color. | | | 1.10.0 |
| TabIndex | `int?` | If defined, indicates that its element can be focused and can participates in sequential keyboard navigation. | | | 1.10.0 |

## DropdownMenu Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| ChildContent | RenderFragment | Specifies the content to be rendered inside the DropdownMenu. | | | 1.10.0 |
| Position | `DropdownMenuPosition` | Gets or sets the dropdown menu position. | | | 1.10.0 |

## DropdownHeader Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| ChildContent | RenderFragment | Specifies the content to be rendered inside the DropdownHeader. | | | 1.10.0 |

## DropdownItem Parameters

| Name | Type | Description | Required | Default | Added Version |
|:--|:--|:--|:--|:--|:--|
| Active | bool | When set to 'true', places the component in the active state with active styling. | | | 1.10.0 |
| ChildContent | RenderFragment | Specifies the content to be rendered inside the DropdownMenu. | | | 1.10.0 |
| Disabled | bool | When set to 'true', disables the component's functionality and places it in a disabled state. | | | 1.10.0 |
| TabIndex | `int?` | If defined, indicates that its element can be focused and can participates in sequential keyboard navigation. | | | 1.10.0 |
| Target | `Target` | The target attribute specifies where to open the linked document. | | `Target.None` | 1.10.0 |
| To | `string?` | Denotes the target route of the link button. | | | 1.10.0 |
| Type | `ButtonType` | Defines the button type. | | `ButtonType.Button` | 1.10.0 |

## Dropdown Methods

| Name | Description | Added Version |
|:--|:--|:--|
| HideAsync | Hides the dropdown menu of a given navbar or tabbed navigation. | 1.10.0 |
| ShowAsync | Shows the dropdown menu of a given navbar or tabbed navigation. | 1.10.0 |
| ToggleAsync | Toggles the dropdown menu of a given navbar or tabbed navigation. | 1.10.0 |
| UpdateAsync | Updates the position of an element’s dropdown. | 1.10.0 |

## Dropdown Events

| Event Type | Description | Added Version |
|:--|:--|:--|
| OnHiding | This event is fired immediately when the hide method has been called. | 1.10.0 |
| OnHidden | This event is fired when an dropdown element has been hidden from the user (will wait for CSS transitions to complete). | 1.10.0 |
| OnShowing | This event fires immediately when the show instance method is called. | 1.10.0 |
| OnShown | This event is fired when an dropdown element has been made visible to the user (will wait for CSS transitions to complete). | 1.10.0 |

## Examples

### Single button

<img src="https://i.imgur.com/HkqLwlx.png" alt="Blazor Bootstrap: Dropdown Component - Single button" />

```cshtml {} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown button</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#single-button)

### Color

<img src="https://i.imgur.com/cuvBVJu.png" alt="Blazor Bootstrap: Dropdown Component - Color" />

```cshtml {3,11,19,27,35,43} showLineNumbers
<div class="d-flex gap-2 mb-4">
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Primary">Primary</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Secondary">Secondary</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Success">Success</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Info">Info</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Warning">Warning</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown>
        <DropdownToggleButton Color="ButtonColor.Danger">Danger</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#color)

### Split button

<img src="https://i.imgur.com/beAr31J.png" alt="Blazor Bootstrap: Dropdown Component - Split button" />

```cshtml {3-4,12-13,21-22,30-31,39-40,48-49} showLineNumbers
<div class="d-flex gap-2 mb-4">
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Primary">Primary</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Primary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Secondary">Secondary</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Success">Success</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Success" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Info">Info</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Info" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Warning">Warning</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Warning" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Split="true">
        <DropdownActionButton Color="ButtonColor.Danger">Danger</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Danger" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#split-button)

### Sizing

<img src="https://i.imgur.com/fwcMxKb.png" alt="Blazor Bootstrap: Dropdown Component - Sizing - Large" />

```cshtml {2,10} showLineNumbers
<div class="d-flex gap-2 mb-4">
    <Dropdown Size="Size.Large">
        <DropdownToggleButton Color="ButtonColor.Secondary">Large button</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem Size="Size.Large" To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Size="Size.Large" Split="true">
        <DropdownActionButton Color="ButtonColor.Secondary">Large split button</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

<img src="https://i.imgur.com/HOlA6Uw.png" alt="Blazor Bootstrap: Dropdown Component - Sizing - Small" />

```cshtml {2,10} showLineNumbers
<div class="d-flex gap-2 mb-4">
    <Dropdown Size="Size.Small">
        <DropdownToggleButton Color="ButtonColor.Secondary">Small button</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Size="Size.Small" Split="true">
        <DropdownActionButton Color="ButtonColor.Secondary">Small split button</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#sizing)

### Directions

### Dropup

To trigger **DropdownMenu** above elements, add the `Direction="DropdownDirection.Dropup"` to the **Dropdown** component.

<img src="https://i.imgur.com/l90nW3S.png" alt="Blazor Bootstrap: Dropdown Component - Dropup" />

```cshtml {2,10} showLineNumbers
<div class="d-flex gap-2">
    <Dropdown Direction="DropdownDirection.Dropup">
        <DropdownToggleButton Color="ButtonColor.Secondary">Dropup button with text</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Direction="DropdownDirection.Dropup" Split="true">
        <DropdownActionButton Color="ButtonColor.Secondary">Dropup split button</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#dropup)

### Dropup centered

To center the DropdownMenu above the toggle, add the Direction="DropdownDirection.DropupCentered" to the Dropdown component.

<img src="https://i.imgur.com/kc462Yy.png" alt="Blazor Bootstrap: Dropdown Component - Dropup centered" />

```cshtml {2} showLineNumbers
<div class="d-flex gap-2">
    <Dropdown Direction="DropdownDirection.DropupCentered">
        <DropdownToggleButton Color="ButtonColor.Secondary">Centered dropup</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#dropup-centered)

### Dropend

To trigger DropdownMenu at the right of elements, add the Direction="DropdownDirection.Dropend" to the Dropdown component.

<img src="https://i.imgur.com/nSZ6Kdv.png" alt="Blazor Bootstrap: Dropdown Component - Dropend" />

```cshtml {2,10} showLineNumbers
<div class="d-flex gap-2">
    <Dropdown Direction="DropdownDirection.Dropend">
        <DropdownToggleButton Color="ButtonColor.Secondary">Dropend</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Direction="DropdownDirection.Dropend" Split="true">
        <DropdownActionButton Color="ButtonColor.Secondary">Split dropend</DropdownActionButton>
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#dropend)

### Dropstart

To trigger DropdownMenu at the left of elements, you can add the Direction="DropdownDirection.Dropstart" to the Dropdown component.

<img src="https://i.imgur.com/A8ifVaS.png" alt="Blazor Bootstrap: Dropdown Component - Dropstart" />

```cshtml {2,10} showLineNumbers
<div class="d-flex gap-2">
    <Dropdown Direction="DropdownDirection.Dropstart">
        <DropdownToggleButton Color="ButtonColor.Secondary">Dropstart</DropdownToggleButton>
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
    </Dropdown>
    <Dropdown Direction="DropdownDirection.Dropstart" Split="true">
        <DropdownToggleButton Color="ButtonColor.Secondary" />
        <DropdownMenu>
            <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
            <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        </DropdownMenu>
        <DropdownActionButton Color="ButtonColor.Secondary">Split dropstart</DropdownActionButton>
    </Dropdown>
</div>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#dropstart)

### Active

To style DropdownItem as active, add the Active="true" parameter to the DropdownItem element in the DropdownMenu.

<img src="https://i.imgur.com/y95OWSd.png" alt="Blazor Bootstrap: Dropdown Component - Active" />

```cshtml {5} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropstart</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link" Active="true">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#active)

### Disabled

To disable the dropdown, set the <b>Disabled</b> parameter to <b>true</b> on the <b>Dropdown</b> component.

<img src="https://i.imgur.com/jMrshBs.png" alt="Blazor Bootstrap: Dropdown Component - Disabled" />

```cshtml {1} showLineNumbers
<Dropdown Disabled="@isDropdownDisabled">
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropstart</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>

<div class="mt-3">
    <Button Color="ButtonColor.Primary" Size="Size.Small" @onclick="EnableDropdown">Enable</Button>
    <Button Color="ButtonColor.Danger" Size="Size.Small" @onclick="DisableDropdown">Disable</Button>
</div>
@code
{
    private bool isDropdownDisabled = true;
    private void EnableDropdown() => isDropdownDisabled = false;
    private void DisableDropdown() => isDropdownDisabled = true;
}
```

To style a dropdown item as disabled, set the <b>Disabled</b> parameter to <b>true</b> on the <b>DropdownItem</b> element in the <b>DropdownMenu</b> component.

<img src="https://i.imgur.com/C3tUcRn.png" alt="Blazor Bootstrap: Dropdown Component - Disabled (Dropdown Item)" />

```cshtml {5} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropstart</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link" Disabled="true">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#disabled)

### Menu position

By default, a DropdownMenu is automatically positioned at 100% from the top and along the left side of its parent. You can change this with the Position parameter.

To right-align a DropdownMenu, add the Position="DropdownMenuPosition.End" parameter to the DropdownMenu component. Directions are mirrored when using Bootstrap in RTL.

<img src="https://i.imgur.com/dwmK0j3.png" alt="Blazor Bootstrap: Dropdown Component - Menu position" />

```cshtml {3} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Right-aligned menu example</DropdownToggleButton>
    <DropdownMenu Position="DropdownMenuPosition.End">
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#menu-position)

### Menu content

### Header

Add a header to label sections of actions in any dropdown menu.

<img src="https://i.imgur.com/eDvOLvf.png" alt="Blazor Bootstrap: Dropdown Component - Header" />

```cshtml {4} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown</DropdownToggleButton>
    <DropdownMenu>
        <DropdownHeader>Dropdown header</DropdownHeader>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#header)

### Dividers

Separate groups of related menu items with a divider.

<img src="https://i.imgur.com/8zd9Rod.png" alt="Blazor Bootstrap: Dropdown Component - Dividers" />

```cshtml {7} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
        <DropdownDivider>Dropdown header</DropdownDivider>
        <DropdownItem To="#" Type="ButtonType.Link">Separated link</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#dividers)

### Text

Place any freeform text within a dropdown menu with text and use spacing utilities. Note that youll likely need additional sizing styles to constrain the menu width.

<img src="https://i.imgur.com/2G0ozU0.png" alt="Blazor Bootstrap: Dropdown Component - Text" />

```cshtml {3-6} showLineNumbers
<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown</DropdownToggleButton>
    <DropdownMenu Class="p-4 text-muted" Style="width: 320px;">
        <p>Some example text that's free-flowing within the dropdown menu.</p>
        <p class="mb-0">And this is more example text.</p>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#text)

### Forms

Put a form within a dropdown menu, or make it into a dropdown menu, and use margin or padding utilities to give it the negative space you require.

<img src="https://i.imgur.com/q52EBle.png" alt="Blazor Bootstrap: Dropdown Component - Forms" />

```cshtml {4-14,20-47} showLineNumbers
@using System.ComponentModel.DataAnnotations

<style>
    .valid.modified:not([type=checkbox]) {
        outline: 1px solid #26b050;
    }

    .invalid {
        outline: 1px solid red;
    }

    .validation-message {
        color: red;
    }
</style>

<Dropdown>
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown form</DropdownToggleButton>
    <DropdownMenu Class="px-4 py-3" Style="width:480px;">
        <EditForm EditContext="@editContext" OnValidSubmit="HandleOnValidSubmit">
            <DataAnnotationsValidator />

            <div class="mb-3">
                <label class="form-label">Item Price: <span class="text-danger">*</span></label>
                <NumberInput TValue="decimal?" Value="invoice.Price" ValueExpression="() => invoice.Price" ValueChanged="(value) => PriceChanged(value)" Placeholder="Enter price" />
                <ValidationMessage For="@(() => invoice.Price)" />
            </div>

            <div class="mb-3">
                <label class="form-label">Item Discount:</label>
                <NumberInput TValue="decimal?" Value="invoice.Discount" ValueExpression="() => invoice.Discount" ValueChanged="(value) => DiscountChanged(value)" Placeholder="Enter discount" />
                <ValidationMessage For="@(() => invoice.Discount)" />
            </div>

            <div class="mb-3">
                <label class="form-label">Total Amount: <span class="text-danger">*</span></label>
                <NumberInput TValue="decimal?" @bind-Value="invoice.Total" Disabled="true" Placeholder="Enter total" />
                <ValidationMessage For="@(() => invoice.Total)" />
            </div>

            <div class="row">
                <div class="col-md-12 text-right">
                    <Button Type="ButtonType.Button" Color="ButtonColor.Secondary" Class="float-end" @onclick="ResetForm">Reset</Button>
                    <Button Type="ButtonType.Submit" Color="ButtonColor.Success" Class="float-end me-2">Submit</Button>
                </div>
            </div>
        </EditForm>
    </DropdownMenu>
</Dropdown>
```

```cs {} showLineNumbers
@code {
    private Invoice invoice = new();
    private EditContext editContext = default!;

    protected override void OnInitialized()
    {
        editContext = new EditContext(invoice);
        base.OnInitialized();
    }

    protected override void OnParametersSet()
    {
        CalculateToatl();
        base.OnParametersSet();
    }

    private void PriceChanged(decimal? value)
    {
        invoice.Price = value;
        CalculateToatl();
    }

    private void DiscountChanged(decimal? value)
    {
        invoice.Discount = value;
        CalculateToatl();
    }

    private void CalculateToatl()
    {
        var price = invoice.Price.HasValue ? invoice.Price.Value : 0;
        var discount = invoice.Discount.HasValue ? invoice.Discount.Value : 0;
        invoice.Total = price - discount;
    }

    public void HandleOnValidSubmit()
    {
        Console.WriteLine($"Price: {invoice.Price}");
        Console.WriteLine($"Discount: {invoice.Discount}");
        Console.WriteLine($"Total: {invoice.Total}");
    }

    private void ResetForm()
    {
        invoice = new();
        editContext = new EditContext(invoice);
    }

    public class Invoice
    {
        [Required(ErrorMessage = "Price required.")]
        [Range(60, 500, ErrorMessage = "Price should be between 60 and 500.")]
        public decimal? Price { get; set; } = 232M;

        [Range(0, 50, ErrorMessage = "Discount should be between 0 and 50.")]
        public decimal? Discount { get; set; }

        [Required(ErrorMessage = "Amount required.")]
        [Range(10, 500, ErrorMessage = "Total should be between 60 and 500.")]
        public decimal? Total { get; set; }
    }
}
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#forms)

### Auto close behavior

By default, the DropdownMenu is closed when clicking either inside or outside the DropdownMenu. You can use the AutoClose and AutoCloseBehavior parameters to change this behavior of the Dropdown.

<img src="https://i.imgur.com/vq2sgtO.png" alt="Blazor Bootstrap: Dropdown Component - Auto close behavior" />

```cshtml {1,9,17,25} showLineNumbers
<Dropdown AutoClose="true">
    <DropdownToggleButton Color="ButtonColor.Secondary">Default dropdown</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
    </DropdownMenu>
</Dropdown>
<Dropdown AutoClose="true" AutoCloseBehavior="DropdownAutoCloseBehavior.Outside">
    <DropdownToggleButton Color="ButtonColor.Secondary">Clickable outside</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
    </DropdownMenu>
</Dropdown>
<Dropdown AutoClose="true" AutoCloseBehavior="DropdownAutoCloseBehavior.Inside">
    <DropdownToggleButton Color="ButtonColor.Secondary">Clickable inside</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
    </DropdownMenu>
</Dropdown>
<Dropdown AutoClose="false">
    <DropdownToggleButton Color="ButtonColor.Secondary">Manual close</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Menu item</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#auto-close-behavior)

### Methods

<img src="https://i.imgur.com/gaJz8Ar.png" alt="Blazor Bootstrap: Dropdown Component - Methods" />

```cshtml {10-12} showLineNumbers
<Dropdown @ref="dropdown1">
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown button</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>

<Button Color="ButtonColor.Primary" @onclick="ShowAsync">Show</Button>
<Button Color="ButtonColor.Primary" @onclick="HideAsync">Hide</Button>
<Button Color="ButtonColor.Primary" @onclick="ToggleAsync">Toggle</Button>
```

```cs {4-6} showLineNumbers
@code{
    private Dropdown dropdown1 = default!;

    private async Task ShowAsync() => await dropdown1.ShowAsync();
    private async Task HideAsync() => await dropdown1.HideAsync();
    private async Task ToggleAsync() => await dropdown1.ToggleAsync();
}
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#methods)

### Events

All dropdown events are fired at the toggling element and then bubbled up.

<img src="https://i.imgur.com/74NtN1y.png" alt="Blazor Bootstrap: Dropdown Component - Events" />

```cshtml {1-4} showLineNumbers
<Dropdown OnHiding="OnDropdownHidingAsync"
          OnHidden="OnDropdownHiddenAsync"
          OnShowing="OnDropdownShowingAsync"
          OnShown="OnDropdownShownAsync">
    <DropdownToggleButton Color="ButtonColor.Secondary">Dropdown button</DropdownToggleButton>
    <DropdownMenu>
        <DropdownItem To="#" Type="ButtonType.Link">Action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Another action</DropdownItem>
        <DropdownItem To="#" Type="ButtonType.Link">Something else here</DropdownItem>
    </DropdownMenu>
</Dropdown>
```

```cs {4-7} showLineNumbers
@code {
    List<string> messages = new List<string>();

    private void OnDropdownHidingAsync() => messages.Add(new("OnHiding"));
    private void OnDropdownHiddenAsync() => messages.Add(new("OnHidden"));
    private void OnDropdownShowingAsync() => messages.Add(new("OnShowing"));
    private void OnDropdownShownAsync() => messages.Add(new("OnShown"));
}
```

[See the demo here.](https://demos.blazorbootstrap.com/dropdown#events)
